# AI Cart Manager

AI Cart Manager is a full-stack cart application with:

- `AI-Cart-Frontend`: React + Vite UI
- `AI-Cart-Backend`: Express API

The frontend runs on `http://localhost:5173` and proxies API calls to the backend on `http://localhost:3001`.

## Repository Links

- Frontend: [AI-Cart-Frontend](https://github.com/Khaled-Anika/AI-Cart-Frontend)
- Backend: [AI-Cart-Backend](https://github.com/Khaled-Anika/AI-Cart-Backend)

## Prerequisites

- Node.js 18+ (Node.js 20 LTS recommended)
- npm 9+ (comes with Node.js)

## Project Structure

```text
AI-Cart-Manger/
├── AI-Cart-Frontend/
├── AI-Cart-Backend/
├── context/
└── chat-logs/
```

## 1) Install Dependencies

Open two terminals (one for backend, one for frontend), then run:

### Backend

```bash
cd AI-Cart-Backend
npm install
```

### Frontend

```bash
cd AI-Cart-Frontend
npm install
```

## 2) Start the App

### Start backend API

From `AI-Cart-Backend`:

```bash
npm run dev
```

Expected output includes:

`Cart API listening on http://localhost:3001`

### Start frontend app

From `AI-Cart-Frontend`:

```bash
npm run dev
```

Then open:

`http://localhost:5173`

## 3) Run Tests

### Backend unit/integration tests (Jest)

From `AI-Cart-Backend`:

```bash
npm test
```

### Frontend end-to-end tests (Playwright)

From `AI-Cart-Frontend`:

```bash
npm run test:e2e
```

To run E2E tests with coverage:

```bash
npm run test:e2e:coverage
```

## 4) Build for Production

### Frontend build

From `AI-Cart-Frontend`:

```bash
npm run build
```

## API Endpoints

Backend cart endpoints:

- `GET /health`
- `GET /api/cart`
- `POST /api/cart/items`
- `PATCH /api/cart/items/:sku`
- `DELETE /api/cart/items/:sku`

## Troubleshooting

- If port `3001` is busy, start backend with another port:
  - `PORT=3002 npm run dev`
  - Update frontend proxy in `AI-Cart-Frontend/vite.config.js` to match.
- If Playwright browsers are missing, run from `AI-Cart-Frontend`:
  - `npx playwright install`
- If dependencies fail to install, remove `node_modules` and reinstall:
  - `rm -rf node_modules package-lock.json && npm install`

