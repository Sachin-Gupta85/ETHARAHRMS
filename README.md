# HRMS Lite — Simple Employee Management

A compact human-resources management starter kit combining a Django backend with a React frontend. This repository is intended as a practical template you can run locally, modify, and learn from — not a production-ready system.

What this project gives you

- REST API backend built with Django (app: `employees`).
- React-based frontend (lightweight single-page UI) that talks to the API.
- Simple examples for employee CRUD, basic attendance, and a dashboard view.

Repository layout (high level)

- `backend/` — Django project and app code. Key files: `manage.py`, `requirements.txt`, `employees/`.
- `frontend/` — Web UI, contains a small React app under `hrms-lite-frontend/` and shared wrapper files.

Quick start (Windows / PowerShell)

1) Backend

- Create and activate a virtual environment

  python -m venv .venv
  .\.venv\Scripts\Activate.ps1

- Install dependencies and run migrations

  pip install -r backend\requirements.txt
  cd backend
  python manage.py migrate

- Start the dev server

  python manage.py runserver

By default the API will be at http://127.0.0.1:8000/ — check `backend/hrms_project/urls.py` for configured routes.

2) Frontend

- From the repository root:

  cd frontend\hrms-lite-frontend
  npm install
  npm start

The React development server typically runs at http://localhost:3000 and proxies API calls to the Django backend (see `package.json` proxy configuration).

Notes and tips

- If ports collide, change them in the servers' startup commands or configuration files.
- Use the Django admin for quick data inspection; create a superuser with:

  cd backend
  python manage.py createsuperuser

- Static files and production deployment are not covered here—this README focuses on local development.

Customizing the project

- Backend: extend `employees/models.py` and update serializers/views/urls to expose new endpoints.
- Frontend: add components under `frontend/hrms-lite-frontend/src/components` and hook them into `App.js`.



