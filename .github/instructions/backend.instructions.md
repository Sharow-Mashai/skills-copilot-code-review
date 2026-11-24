---
applyTo: "src/backend/**/*.py,src/app.py"
---

## Backend Guidelines

- Define API endpoints in `src/backend/routers/` and keep route modules focused.
- Load example database content from `src/backend/database.py`.
- Log internal failure details server-side when appropriate. Return explicit HTTP status codes and safe error messages; do not expose stack traces, secrets, or sensitive database details to the frontend.
- Ensure API endpoints, parameters, and response behavior are explained in the project documentation.
- Verify that backend contract changes are reflected in `src/static/`. Call out potentially breaking changes to the developer.
- Validate untrusted input and use structured PyMongo queries and updates.
