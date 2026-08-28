# Release Management & Version Governance Guide

## Purpose
This guide defines standards for semantic version bumping, multi-file version synchronization, changelog authoring, git release tagging, and zero-downtime branch synchronization.

---

## 1. Semantic Versioning Standard

Releases follow [SemVer (v2.0.0)](https://semver.org/):
- **MAJOR (`X.0.0`)**: Breaking API changes, major platform rewrites, incompatible database migrations.
- **MINOR (`x.Y.0`)**: New backward-compatible features, new domain modules, analytics engines.
- **PATCH (`x.y.Z`)**: Backward-compatible bug fixes, hotfixes, styling repairs, performance tweaks.

---

## 2. Synchronized Version Identifiers

When bumping versions, all canonical project version files MUST be synchronized in lockstep:
- `backend/package.json` (`version`)
- `backend/src/controllers/health.controller.js` (`version`)
- `frontend/package.json` (`version`)
- `frontend/src/config/app.config.ts` (`version`)

---

## 3. Keep a Changelog Standard

Changelogs (`backend/CHANGELOG.md` and `frontend/CHANGELOG.md`) must categorize changes under standard sections:
- `### Added`: New user-facing features, API endpoints, components.
- `### Changed`: Changes in existing functionality or UI improvements.
- `### Fixed`: Bug fixes and defect resolutions.
- `### Security`: Vulnerability fixes, authentication hardening, compliance updates.

---

## 4. Release Execution Workflow

```bash
# 1. Run full test suites and production build
npm test (backend)
npm test (frontend)
npm run build (frontend)

# 2. Bump version files and changelogs on dev
git add -A
git commit -m "chore(release): bump version to vX.Y.Z and update changelogs"
git push origin dev

# 3. Merge dev to main, tag release, and push
git checkout main
git pull origin main
git merge dev -m "Release vX.Y.Z: [Summary]"
git tag -a vX.Y.Z -m "Release vX.Y.Z: [Summary]"
git push origin main --tags

# 4. Switch back to active development branch
git checkout dev
```
