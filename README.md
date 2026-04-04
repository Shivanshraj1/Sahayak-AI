# Sahayak-AI

Sahayak is a split-repo demo app with a Vite client in `client/` and an Express plus Socket.IO backend in `server/`.

## What's Included

- Live demo: https://sahayak-ai-mocha.vercel.app/

- Real-time request, heatmap, and stats updates over Socket.IO
- SMS demo flow with OTP simulation
- Analytics dashboard backed by `/api/analytics`
- In-memory backend with optional Claude triage
- Demo seed script in `scripts/seed.js`

## Project Layout

```text
Sahayak-AI/
|-- client/
|   |-- src/
|   |   |-- components/
|   |   |-- hooks/
|   |   |-- pages/
|   |   `-- services/
|   `-- .env.example
|-- server/
|   |-- index.js
|   |-- package.json
|   `-- .env.example
|-- scripts/
|   `-- seed.js
`-- .env.example
```

## Setup

1. Install frontend dependencies:

```bash
cd client
npm install
```

2. Install backend dependencies:

```bash
cd ../server
npm install
```

3. Create environment files:

```bash
cd ../client
cp .env.example .env

cd ../server
cp .env.example .env
```

4. Start frontend + backend together (recommended):

```bash
npm run live
```

Or run them separately:

```bash
cd client
npm run dev
```

```bash
cd server
npm run dev
```

5. Start only the backend:

```bash
cd server
npm start
```

## Key API Endpoints

- `POST /api/triage`
- `POST /api/requests`
- `GET /api/requests`
- `POST /api/match`
- `PATCH /api/requests/:id/status`
- `GET /api/ngos`
- `PATCH /api/ngos/:id/resources`
- `POST /api/sms/simulate`
- `POST /api/sms/verify`
- `GET /api/heatmap`
- `GET /api/analytics`
- `GET /api/stats`
- `GET /health`
