# game-stats-webapp

## Repo Structure

```
game-stats-webapp/
├── backend/               
│   ├── app/
│   │   ├── main.py          # FastAPI app entrypoint
│   │   ├── models.py        # SQLAlchemy models: Session, Player, Game, etc.
│   │   ├── schemas.py       # Pydantic schemas for API requests/responses
│   │   ├── crud.py          # DB logic (CRUD operations)
│   │   ├── api/routes.py    # API endpoints
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

## Tech Stack Overview

- **Backend:** Python, FastAPI, SQLAlchemy, SQLite
- **Frontend:** SvelteKit, Tailwind CSS, Chart.js
- **Testing:** pytest, Playwright?
