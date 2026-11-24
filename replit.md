# JEEVAN SAATHI AI

A multilingual support and guidance app for students, job seekers, women, senior citizens, and the general public.

## Run & Operate

- `pnpm --filter @workspace/jeevan-saathi-ai run dev` — run the JEEVAN SAATHI AI web app
- `pnpm --filter @workspace/api-server run dev` — run the API server (port 5000)
- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from the OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- Required env: `DATABASE_URL` — Postgres connection string

## Stack

- pnpm workspaces, Node.js 24, TypeScript 5.9
- API: Express 5
- DB: PostgreSQL + Drizzle ORM
- Validation: Zod (`zod/v4`), `drizzle-zod`
- API codegen: Orval (from OpenAPI spec)
- Build: esbuild (CJS bundle)

## Where things live

- `artifacts/jeevan-saathi-ai/` — responsive web app and its client-side pages.
- `artifacts/api-server/` — shared API service.
- `lib/api-spec/openapi.yaml` — source of truth for API contracts.
- `lib/db/src/schema/` — shared database schema.

## Architecture decisions

- The initial JEEVAN SAATHI AI experience is frontend-first and uses clearly labeled sample data.

## Product

JEEVAN SAATHI AI provides a dashboard, AI assistant interface, government-scheme discovery and eligibility checks, career guidance, study planning, language settings, and account screens. Sample content is for demonstration and should not be treated as live government or job information.

## User preferences

_Populate as you build — explicit user instructions worth remembering across sessions._

## Gotchas

_Populate as you build — sharp edges, "always run X before Y" rules._

## Pointers

- See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details
