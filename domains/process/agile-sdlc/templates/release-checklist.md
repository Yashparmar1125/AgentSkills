# Production Release Checklist Template

## Release Metadata
- **Version**: `vX.Y.Z`
- **Release Date**: `YYYY-MM-DD`
- **Branch**: `main`

---

## 1. Quality Gates
- [ ] Backend tests passing: `npm test` in `backend/` (100% pass rate).
- [ ] Frontend tests passing: `npm test` in `frontend/` (100% pass rate).
- [ ] Production build succeeds: `npm run build` in `frontend/` (zero compile errors).
- [ ] Zero lint/type errors across codebase.

---

## 2. Version Synchronization
- [ ] `backend/package.json` (`version`) matches target release.
- [ ] `backend/src/controllers/health.controller.js` (`version`) matches target release.
- [ ] `frontend/package.json` (`version`) matches target release.
- [ ] `frontend/src/config/app.config.ts` (`version`) matches target release.

---

## 3. Documentation & Governance
- [ ] `backend/CHANGELOG.md` updated under `[X.Y.Z]` with Keep a Changelog format.
- [ ] `frontend/CHANGELOG.md` updated under `[X.Y.Z]` with Keep a Changelog format.
- [ ] Zero emojis anywhere in code, commits, or release notes.

---

## 4. Git & Deployment
- [ ] Release commit authored on `dev`.
- [ ] `dev` merged cleanly into `main`.
- [ ] Annotated git tag created: `git tag -a vX.Y.Z -m "Release vX.Y.Z: ..."`
- [ ] Pushed `main` and tags: `git push origin main --tags`
- [ ] Switched back to active development branch: `git checkout dev`
