### About me

Non-traditional developer and lifelong learner, building things mostly to figure
out how they work. I'll play around with whatever looks fun on GitHub, break
plenty along the way, and always learn something every time.

Most of what's here started as a real problem someone I know actually had — a
restaurant operator buried in vendor invoices, a family coordinating care for a
parent, a group that wanted a better tournament pool. I build the thing, put it
in front of them, and fix what breaks once it meets real data.

### Selected work

- **sousiq** *(private)* — a food-costing and inventory platform for independent
  restaurants. Vendor invoices and bid sheets arrive as PDFs, spreadsheets and
  photos, get parsed into structured line items, and are matched against the
  restaurant's product library through a seven-tier cascade — deterministic
  tiers first, then constrained fuzzy matching, then pgvector semantic retrieval
  with model disambiguation only at the end. Model-derived matches are scored
  below their deterministic equivalents and anything ambiguous goes to a human.
  Accuracy is checked against a ground-truth set nightly in CI.
  *(TypeScript · Postgres + pgvector · Claude and OpenAI APIs · vision and PDF parsing)*

- **prial** *(private)* — a pipeline over SEC investment-adviser filings.
  Nineteen months of Form ADV bulk data resolved into a deduped roster of 25,387
  registered firms, 144,076 named officers from Schedules A and B, and 22,273
  firm websites, enriched across 36 attributes including strategy and
  period-over-period AUM growth. Resolving entities across filing periods is the
  genuinely hard part. *(Python · Postgres · Docker)*

- **[bracketeer](https://github.com/dommango/bracketeer)** — a multi-tenant
  tournament pool platform, running in production. Live scoring against an
  official answer key, real-time updates pushed over Server-Sent Events on
  Postgres `LISTEN/NOTIFY`, Stripe billing, an iOS wrap via Capacitor, and every
  external integration environment-gated so the app builds and runs green with
  no keys configured.
  *(Next.js 16 · React 19 · TypeScript · Prisma · Postgres)*

- **[carelog](https://github.com/dommango/carelog)** — an offline-first PWA where
  a small caregiving team logs the daily care of one patient by text, voice or
  photo. An async pipeline turns messy input into structured records that feed
  adherence tracking, reminders and doctor-visit reports.
  *(Next.js · pg-boss · Prisma · Postgres)*

- **[carecover](https://github.com/dommango/carecover)** — coordinating
  caregiving coverage over SMS. Post a window, family claims blocks, and
  whatever is still open at the deadline escalates to paid caregivers. Taking it
  through A2P 10DLC carrier registration taught me more than the code did.
  *(Next.js · Prisma · Twilio)*

- **[modular-mind](https://github.com/dommango/modular-mind)** — a multi-stage
  pipeline that decodes VCV Rack patch files, builds a corpus of module and
  patch knowledge, learns the structural patterns behind them, and generates new
  valid patches from what it learned. Half machine-learning project, half excuse
  to mess with synths. *(Python)*

- **[vcv-rack-plugin-mcp-server](https://github.com/dommango/vcv-rack-plugin-mcp-server)**
  — driving a live modular synth patch from an MCP client. *(C++)*

- **[agentmats](https://github.com/dommango/agentmats)** — one-page reference
  "placemats" for five CLI coding agents (Claude Code, Codex, Kimi Code, Hermes,
  Antigravity), each kept current by its own daily sync and verified against the
  vendor's docs in CI — a row that isn't on the vendor inventory fails the build.
  Started as a single Claude Code cheatsheet that maintained itself; grew a
  Rosetta table once it turned out every agent has the same eight jobs.
  [Have a look →](https://dommango.github.io/agentmats/)

Happy to walk through either of the private ones, or demo them live, on request.

**Stack:** TypeScript · React / Next.js · Python · Postgres (+ pgvector) ·
Prisma · Claude and OpenAI APIs · Railway
