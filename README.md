# game-stats-webapp

Web app to record, view, and analyze game sessions (only MTG for now).

## Dev Setup (Docker Compose + Live Reload)

1. **Requirements:**  
   - Docker + Docker Compose

2. **Start dev servers:**  
   ```bash
   docker compose up --build
   ```
   - backend: [localhost:8000](http://localhost:8000)
   - frontend: [localhost:5173](http://localhost:5173)

3. **Edit code locally:**  
   - Changes in `backend/app/` or `frontend/src/` reload automatically.

4. **Stop servers:**  
   ```bash
   docker compose down
   ```

All dependencies/tools run inside containers—no need for local Python/Node setup.

## Tech Stack Overview

- **Backend:** Python, FastAPI, SQLAlchemy, SQLite
- **Frontend:** SvelteKit, Tailwind CSS, Chart.js
- **Testing:** pytest, Playwright?
- **Deployment:** docker, docker compose, traefik

## Repo Structure

```
game-stats-webapp/
├── backend/               
│   ├── app/
│   │   ├── main.py          # FastAPI app entrypoint
│   │   ├── models.py        # SQLAlchemy models: Session, Player, Game, etc.
│   │   ├── schemas.py       # Pydantic schemas for API requests/responses
│   │   ├── crud.py          # DB logic (CRUD operations)
│   │   ├── routes.py        # API endpoints
│   │   └── db.py            # DB session/connection utilities
│   ├── requirements.txt     # Dependencies
│   └── Dockerfile
├── frontend/                
│   ├── src/
│   │   ├── App.svelte       # Root Svelte component
│   │   ├── components/      # Reusable UI pieces (SessionForm, StatsChart, etc.)
│   │   ├── routes/          # Page views (Home, AddSession, Stats)
│   │   └── assets/          # Imgs, styles, etc.
│   ├── static/              # Public files (favicon, global img)
│   ├── package.json         # Dependencies
│   └── Dockerfile
```
