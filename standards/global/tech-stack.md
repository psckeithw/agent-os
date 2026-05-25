# Tech Stack

## Frontend
- React 18 + TypeScript (Vite)
- Tailwind CSS v4
- Responsive design & accessibility
- Server‑Sent Events for AI streaming

## Backend
- Node.js 18 + Express
- TypeScript (strict)
- Local JSON storage via `storageAdapter`
- Azure OpenAI (free tier) for AI analysis
- Future migration: Azure Blob JSON / Cosmos DB (Core API)

## AI & Analytics
- AI‑analysis module (`services/aiAnalysis.js`)
- In‑process LRU cache (TTL 24 h)
- New API: `/api/ai/analysis`, `/api/ai/trends`, `/api/ai/summary`

## Testing
- Playwright (E2E, API & UI)
- Unit & integration tests (Jest/Mocha)

## Other
- Demo telemetry endpoint (`GET /api/demo/telemetry`)
