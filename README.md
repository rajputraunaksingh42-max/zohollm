# Zoho LLM Dashboard — Complete MVP

This is a client-ready MVP rebuilt from the dashboard requirements/screenshots.

## Included
- React + TypeScript dashboard
- Express API
- Persistent SQLite database
- Create / edit-ready report model
- Search and category filtering
- Favorites and delete
- Report detail view
- CSV / XLS / XLSX upload and parsing
- Saved tabular data preview
- Dashboard KPI cards and category distribution
- Local AI assistant fallback using stored report data
- Settings screen
- Responsive desktop/mobile layout

## Start

Install Node.js 18+.

```bash
npm install
npm run dev
```

Open http://localhost:5173

API runs on http://localhost:4000.

## Data persistence

SQLite is automatically created at:

`server/data/dashboard.db`

Uploaded files are parsed and their table data is stored in SQLite. The original temporary upload is removed after parsing.

## Production work

For a real Zoho deployment, add:
1. Zoho OAuth and the required Zoho API scopes.
2. A real LLM provider on the server using environment variables.
3. Authentication / user roles.
4. Audit logs.
5. Report permissions.
6. Background jobs for large files.
7. PDF parsing if PDF reports are required.

Do not put LLM or Zoho secrets in React/browser code.
