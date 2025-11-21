# TinyLink

Tiny URL shortener built with Next.js + Postgres.

## Live demo
https://your-deployment-url.vercel.app

## Endpoints (required for autograder)
- GET `/healthz` — 200 status
- POST `/api/links` — create link (409 if exists)
- GET `/api/links` — list links
- GET `/api/links/:code` — get link
- DELETE `/api/links/:code` — delete link
- GET `/:code` — redirect (302 or 404)

## Setup (local)
1. `npm install`
2. Create Postgres and run `prisma.sql` to create table.
3. Create `.env` from `.env.example`
4. `npm run dev`

## Notes
Codes must match `[A-Za-z0-9]{6,8}`.
