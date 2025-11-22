# Realtime Group Chat (Socket.IO + Vite + React)

This repository contains a simple realtime group chat with a backend Socket.IO server and a Vite + React frontend.

## Prerequisites
- Node.js (v16+ recommended, v18+ preferred)
- npm (bundled with Node.js)

## Repository layout
- `backend/` - Express + Socket.IO server (listens on port `4000`)
- `frontend/` - Vite + React app (development server via `npm run dev`)

## Quick start (Windows / PowerShell)

1. Start the backend

```powershell
cd backend
npm install
node server.js
```

The backend server runs at `http://localhost:4000` (this is the Socket.IO endpoint).

2. Start the frontend (in a separate terminal)

```powershell
cd frontend
npm install
npm run dev
```

Vite will serve the frontend (by default on `http://localhost:5173`). The frontend client connects to the backend at `http://localhost:4000` (see `frontend/src/ws.js`).

## Build & Preview

To build the frontend for production and preview the build:

```powershell
cd frontend
npm run build
npm run preview
```

## Notes & tips
- The backend Socket.IO server enables CORS for all origins, allowing the frontend to connect while running on the Vite dev server.
- If you prefer a `npm start` script for the backend, add the following to `backend/package.json` under `scripts`:

```json
"start": "node server.js"
```

Then you can run the backend with `npm start`.

## Pushing to GitHub

If you haven't already, initialize a git repository at the project root and push:

```powershell
cd "d:\Full Stack Developement\Web Socket\Second"
git init
git add .
git commit -m "Initial commit"
gh repo create <your-repo-name> --public --source . --remote origin
git push -u origin main
```

Replace `https://github.com/naeemcodemaster/Group-Chat-App-like-WhatsApp-WebSocket-` with your repository name. You can also create the repo on GitHub first and then add the remote URL instead of using `gh`.

---

If you want, I can also:

- Add a `start` script to `backend/package.json` (so you can run `npm start`).
- Add `README.md` files inside `frontend/` and `backend/` with service-specific details.
- Create a `.gitignore` (if missing) and a simple `Procfile` or Dockerfile for deployment.

Let me know which of the above you'd like next.
