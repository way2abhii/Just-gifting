# JustGifting

A collaborative gifting platform: a friend creates a gift page for someone, the site suggests suitable gifts ranked by priority, and friends and family choose a gift or chip in. Each gift shows its percent funded. Pledges are simulated, so no real money moves.

**Stack:** React + Vite + Tailwind | Python + FastAPI | Supabase (PostgreSQL, Auth, Storage)

## Folders
| Folder | Contents |
|---|---|
| Page 1 | Create your gifting page (home) |
| Page 2 | Tell us about them (recipient profile) |
| Page 3 | Gift recommendations |
| Page 4 | Contributions dashboard |
| Page 5 | Public gifting page |
| app | App shell: Vite, Tailwind, router, navigation, shared components |
| backend | FastAPI API |
| database | Supabase / PostgreSQL draft schema |
| docs | Design system and the 8-week plan |

## Run
```
cd app
npm install
npm run dev          # http://localhost:5173
```
Backend: `cd backend && pip install -r requirements.txt && python -m pytest && uvicorn app.main:app --reload`

## Status: Week 2 of 8 (about 25%)
- Page 1: home page with hero and how-it-works steps
- Page 2: recipient form (name, age range, occasion, interests, budget, event date)
- Page 3: recipient summary and gift cards with select / deselect and a live total
- Page 4: four summary cards worked out from sample data
- Backend: Supabase connection, `GET /pages/{slug}` and `POST /pages` with validation, 8 tests
- Database: tables and seed data ready to run in Supabase (see `database/README.md`)
Sections still marked "Planned for Week N" on the screens are built in those weeks. See `docs/8_WEEK_PLAN.md`.
