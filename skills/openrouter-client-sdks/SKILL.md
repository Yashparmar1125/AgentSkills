---
name: openrouter-client-sdks
description: >-
  Comprehensive guide, recipes, and type-safe patterns for OpenRouter Client SDKs
  (@openrouter/sdk in TypeScript, openrouter in Python, and go-sdk in Go). Use when
  implementing LLM inference across 400+ models, real-time streaming, tool/function
  calling, structured JSON outputs, model fallback cascades, provider routing, multi-key
  rotation, embeddings, and API key management.
license: MIT
---

# OpenRouter Client SDKs Guide & Reference

The OpenRouter Client SDKs provide lightweight, auto-generated, type-safe clients over the OpenRouter unified API. They enable calling 400+ AI models from OpenAI, Anthropic, Google, Meta, Mistral, DeepSeek, and NVIDIA with zero boilerplate, standard schema compliance, and provider routing optimizations.

---

## 1. Quick Installation & Runtime Support

| Runtime / Language | Package Name | Command |
| :--- | :--- | :--- |
| **TypeScript / Node.js** | `@openrouter/sdk` | `npm install @openrouter/sdk` / `pnpm add @openrouter/sdk` / `bun add @openrouter/sdk` |
| **Deno** | `@openrouter/sdk` | `deno add npm:@openrouter/sdk` |
| **Python** | `openrouter` | `pip install openrouter` / `uv add openrouter` |
| **Go** | `github.com/OpenRouterTeam/go-sdk` | `go get github.com/OpenRouterTeam/go-sdk` |

> **Note on TypeScript Module Format**: `@openrouter/sdk` is distributed as native ES Modules (ESM). In CommonJS environments, dynamically import using `const { OpenRouter } = await import('@openrouter/sdk');`.

---

## 2. Client Initialization & Authentication

### TypeScript Client
```typescript
import { OpenRouter } from '@openrouter/sdk';

const client = new OpenRouter({
  apiKey: process.env.OPENROUTER_API_KEY, // Defaults to OPENROUTER_API_KEY if omitted
  // Optional attribution headers for OpenRouter rankings & analytics
  siteUrl: 'https://myapp.domain.com',
  siteName: 'My Academic App',
});
```

### Python Client (Sync & Async)
```python
import os
from openrouter import OpenRouter

# Synchronous context manager
with OpenRouter(
    api_key=os.getenv("OPENROUTER_API_KEY"),
    headers={
        "HTTP-Referer": "https://myapp.domain.com",
        "X-Title": "My Academic App"
    }
) as client:
    response = client.chat.send(
        model="openai/gpt-4o",
        messages=[{"role": "user", "content": "Hello OpenRouter!"}]
    )
    print(response.choices[0].message.content)
```

### Go Client
```go
package main

import (
    "context"
    "fmt"
    "os"
    openrouter "github.com/OpenRouterTeam/go-sdk"
)

func main() {
    client := openrouter.NewClient(
        openrouter.WithAPIKey(os.Getenv("OPENROUTER_API_KEY")),
        openrouter.WithReferer("https://myapp.domain.com"),
        openrouter.WithTitle("My Academic App"),
    )
    
    // Call client endpoints
}
```

---

## 3. Core Capabilities & Code Recipes

### A. Non-Streaming Chat Completions
```typescript
import { OpenRouter } from '@openrouter/sdk';

const client = new OpenRouter();

const response = await client.chat.send({
  model: 'anthropic/claude-3.7-sonnet',
  messages: [
    { role: 'system', content: 'You are an expert diagnostic tutor.' },
    { role: 'user', content: 'Explain why student attendance impacts exam performance.' }
  ],
  temperature: 0.2,
  max_tokens: 1500
});

console.log(response.choices[0].message.content);
```

### B. Real-Time Token Streaming
```typescript
import { OpenRouter } from '@openrouter/sdk';

const client = new OpenRouter();

const stream = await client.chat.send({
  model: 'google/gemini-2.0-flash-exp:free',
  messages: [
    { role: 'user', content: 'Draft a 3-step intervention plan for an at-risk student.' }
  ],
  stream: true
});

for await (const chunk of stream) {
  const token = chunk.choices[0]?.delta?.content ?? '';
  process.stdout.write(token);
}
```

### C. Provider Routing & Optimization Parameters
OpenRouter allows precise control over data routing, zero data retention (ZDR), throughput sorting, and provider priority:

```typescript
const response = await client.chat.send({
  model: 'meta-llama/llama-3.3-70b-instruct',
  messages: [{ role: 'user', content: 'Generate code analysis.' }],
  provider: {
    zdr: true,                     // Zero Data Retention compliance
    sort: 'throughput',           // 'price' | 'throughput' | 'latency'
    order: ['Fireworks', 'Together', 'DeepInfra'], // Preferred provider fallback order
    allow_fallbacks: true
  }
});
```

### D. Structured JSON Outputs & Schema Enforcement
Enforce typed JSON schema outputs across supported models:

```typescript
import { OpenRouter } from '@openrouter/sdk';

const client = new OpenRouter();

const response = await client.chat.send({
  model: 'openai/gpt-4o-mini',
  messages: [
    { role: 'user', content: 'Analyze student risk data and return metrics.' }
  ],
  response_format: {
    type: 'json_schema',
    json_schema: {
      name: 'academic_risk_analysis',
      strict: true,
      schema: {
        type: 'object',
        properties: {
          riskScore: { type: 'number' },
          tier: { type: 'string', enum: ['HEALTHY', 'WATCH', 'HIGH_RISK', 'CRITICAL'] },
          interventions: {
            type: 'array',
            items: { type: 'string' }
          }
        },
        required: ['riskScore', 'tier', 'interventions'],
        additionalProperties: false
      }
    }
  }
});

const parsed = JSON.parse(response.choices[0].message.content);
console.log(parsed.tier, parsed.riskScore);
```

### E. Tool Calling / Function Calling
```typescript
import { OpenRouter } from '@openrouter/sdk';

const client = new OpenRouter();

const tools = [
  {
    type: 'function' as const,
    function: {
      name: 'getStudentAttendance',
      description: 'Fetch the 30-day attendance rate and missed lecture count for a student.',
      parameters: {
        type: 'object',
        properties: {
          studentId: { type: 'number', description: 'The unique ID of the student' }
        },
        required: ['studentId']
      }
    }
  }
];

const response = await client.chat.send({
  model: 'google/gemini-2.0-flash-exp:free',
  messages: [{ role: 'user', content: 'What is the attendance status of student ID 104?' }],
  tools,
  tool_choice: 'auto'
});

const toolCalls = response.choices[0].message.tool_calls;
if (toolCalls && toolCalls.length > 0) {
  for (const call of toolCalls) {
    console.log('Tool to execute:', call.function.name, call.function.arguments);
  }
}
```

### F. Embeddings Generation
```typescript
import { OpenRouter } from '@openrouter/sdk';

const client = new OpenRouter();

const embeddingRes = await client.embeddings.create({
  model: 'openai/text-embedding-3-small',
  input: ['Diagnostic assessment rubric', 'Student cognitive growth matrix']
});

console.log('Vector dimension:', embeddingRes.data[0].embedding.length);
```

---

## 4. Production Architectural Patterns

### Pattern 1: Dynamic Model Fallback Cascade
Always implement a fallback cascade to protect against upstream outages or regional rate limits:

```typescript
async function generateWithFallback(prompt: string, primaryModel = 'anthropic/claude-3.7-sonnet') {
  const client = new OpenRouter();
  const modelsToTry = [primaryModel, 'openrouter/free', 'google/gemini-2.0-flash-exp:free'];

  for (const model of modelsToTry) {
    try {
      const res = await client.chat.send({
        model,
        messages: [{ role: 'user', content: prompt }],
        max_tokens: 2000
      });
      return { success: true, model, content: res.choices[0].message.content };
    } catch (err: any) {
      console.warn(`[OpenRouter] Failed on model ${model}:`, err.message);
      if (model === modelsToTry[modelsToTry.length - 1]) throw err;
    }
  }
}
```

### Pattern 2: Multi-Key Pool & Rate-Limit Cooldown (429 Handling)
Maintain a pool of API keys with automatic round-robin rotation and cooldown on 429 status codes:

```typescript
class OpenRouterKeyPool {
  private keys: string[];
  private cooldowns: Map<string, number> = new Map();
  private cursor = 0;

  constructor(keys: string[]) {
    this.keys = keys.filter(Boolean);
  }

  getActiveKey(): string {
    const now = Date.now();
    for (let i = 0; i < this.keys.length; i++) {
      const idx = (this.cursor + i) % this.keys.length;
      const key = this.keys[idx];
      const expiry = this.cooldowns.get(key) || 0;
      if (now > expiry) {
        this.cursor = (idx + 1) % this.keys.length;
        return key;
      }
    }
    return this.keys[0]; // Fallback to first if all on cooldown
  }

  markCooldown(key: string, cooldownSec = 60) {
    this.cooldowns.set(key, Date.now() + cooldownSec * 1000);
  }
}
```

---

## 5. Client SDK vs Agent SDK

| Dimension | Client SDK (`@openrouter/sdk`) | Agent SDK (`@openrouter/agent`) |
| :--- | :--- | :--- |
| **Core Focus** | Lean, 1:1 typed API client over OpenRouter REST | High-level agentic primitives & runtime |
| **Conversation State** | Manually managed by application | Automated turn-by-turn memory |
| **Tool Execution** | Dispatches `tool_calls` for manual handling | Automatically runs registered tools |
| **Use When** | Direct inference, custom pipelines, low latency | Building multi-step autonomous assistants |

---

## 6. Official Resources & References
- **Official Documentation**: https://openrouter.ai/docs/client-sdks/overview
- **TypeScript Reference**: https://openrouter.ai/docs/client-sdks/typescript
- **Python Reference**: https://openrouter.ai/docs/client-sdks/python
- **Agent Skill Repository**: https://github.com/OpenRouterTeam/skills
- **Models Catalog**: https://openrouter.ai/models
