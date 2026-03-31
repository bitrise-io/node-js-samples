# Node.js Sample Projects

This repository contains Node.js sample projects covering typical combinations of frameworks, package managers, and tool version management setups.

## Samples

| Directory | Framework | Package Manager | Testing | Node Version Management |
|-----------|-----------|-----------------|---------|-------------------------|
| [next-js-npm](next-js-npm/) | Next.js | npm | Jest · Testing Library | `.nvmrc` |
| [next-js-yarn](next-js-yarn/) | Next.js | Yarn | — | `engines` in package.json |
| [nestjs-cats-app](nestjs-cats-app/) | NestJS | npm | Jest · Supertest (unit + E2E) | `.tool-versions` |

---

### next-js-npm

**Stack:** Next.js · React · TypeScript · Jest · Testing Library · npm

**What it demonstrates:**
- Next.js application with TypeScript
- Unit and component testing with Jest and React Testing Library
- Dependency management with npm
- Node version pinned via `.nvmrc` (used by nvm and fnm)

**How to run:**
```bash
cd next-js-npm
nvm use  # or: fnm use
npm install
npm test
```

---

### next-js-yarn

**Stack:** Next.js · React · TypeScript · Yarn

**What it demonstrates:**
- Next.js application with TypeScript
- Dependency management with Yarn
- Node version requirement declared via `engines` field in `package.json`

**How to run:**
```bash
corepack enable  # one-time setup, activates yarn via Node.js corepack
cd next-js-yarn
yarn install
yarn build
```

---

### nestjs-cats-app

**Stack:** NestJS · TypeScript · Jest · Supertest · npm

**What it demonstrates:**
- Backend REST API (no frontend) with NestJS module/controller/service architecture
- Dependency injection, guards, pipes, interceptors, and middleware
- DTO validation with `class-validator`
- Unit tests for controllers and services with `@nestjs/testing`
- E2E HTTP tests with Supertest (separate test suite and Jest config)
- Dependency management with npm
- Node version pinned via `.tool-versions` (used by asdf and mise)

**How to run:**
```bash
cd nestjs-cats-app
asdf install  # or: mise install
npm install
npm test              # unit tests
npm run test:e2e      # E2E tests
```
