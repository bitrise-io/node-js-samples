# Node.js Sample Projects

This repository contains Node.js sample projects covering typical combinations of frameworks, package managers, and tool version management setups.

## Samples

| Directory | Framework | Package Manager | Testing | Node Version Management |
|-----------|-----------|-----------------|---------|-------------------------|
| [nextjs-npm](nextjs-npm/) | Next.js | npm | Jest · Testing Library | `.nvmrc` |
| [nextjs-yarn](nextjs-yarn/) | Next.js | Yarn | — | `engines` in package.json |
| [nestjs-cats-app](nestjs-cats-app/) | NestJS | npm | Jest · Supertest (unit + E2E) | `.tool-versions` |
| [nestjs-node-version](nestjs-node-version/) | NestJS | npm | Jest · Supertest (unit + E2E) | `.node-version` |

---

### nextjs-npm

**Stack:** Next.js · React · TypeScript · Jest · Testing Library · npm

**What it demonstrates:**
- Next.js application with TypeScript
- Unit and component testing with Jest and React Testing Library
- Dependency management with npm
- Node version pinned via `.nvmrc` (used by nvm and fnm)

**How to run:**
```bash
cd nextjs-npm
nvm use  # or: fnm use
npm install
npm run lint
npm test
```

---

### nextjs-yarn

**Stack:** Next.js · React · TypeScript · Yarn

**What it demonstrates:**
- Next.js application with TypeScript
- Dependency management with Yarn
- Node version requirement declared via `engines` field in `package.json`

**How to run:**
```bash
corepack enable  # one-time setup, activates yarn via Node.js corepack
cd nextjs-yarn
yarn install
yarn lint
yarn build
```

---

### nestjs-node-version

**Stack:** NestJS · TypeScript · Jest · Supertest · npm

**What it demonstrates:**
- Same NestJS structure as `nestjs-cats-app`
- Node version pinned via `.node-version` (used by nodenv and fnm)

**How to run:**
```bash
cd nestjs-node-version
nodenv install  # or: fnm install
npm install
npm run lint
npm test              # unit tests
npm run test:e2e      # E2E tests
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
npm run lint
npm test              # unit tests
npm run test:e2e      # E2E tests
```
