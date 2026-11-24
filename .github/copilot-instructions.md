# Repository instructions

## Project context

- This repository contains a FastAPI application in `src/app.py`, with API routers and MongoDB access under `src/backend/`.
- The browser interface is a static, framework-free HTML, CSS, and JavaScript application under `src/static/`.
- MongoDB is accessed through PyMongo. Do not assume application data is stored only in process memory.

## Security

- Validate and sanitize untrusted input at system boundaries.
- Check for risks that could expose user data. Keep credentials and secrets out of source, logs, and responses; preserve Argon2 password hashing and never return stored password hashes.
- Prefer loading configuration and content from the database instead of hard-coding it. If external configuration is necessary, use environment variables or a non-committed config file.
- Use structured PyMongo queries and updates. Do not build database operators from untrusted input.
- Do not describe the current teacher identity or authorization flow as secure unless the implementation actually enforces it.

## Code quality

- Use consistent naming conventions and follow existing formatting and module boundaries.
- Make the smallest focused change that solves the requested problem.
- Preserve existing API and browser behavior unless the task explicitly asks to change it.
- Prefer existing dependencies and helpers. Do not add a framework or dependency for a small feature.
- Reduce code duplication and prefer maintainability and readability over optimization.
- Consider optimizing methods that are used frequently or are performance-sensitive; avoid speculative optimization.
- Handle errors explicitly and return appropriate FastAPI errors. Do not hide failures behind broad exception handling or success-shaped fallbacks.

## Review guidance

- Prioritize correctness, security, data integrity, accessibility, and user-visible regressions.
- Report actionable issues introduced by the change; distinguish them from pre-existing behavior.
- For each finding, explain the affected scenario and impact, and point to the relevant code. Avoid speculative claims and style-only comments.
- If no actionable issue is found, say so rather than inventing findings.

## Validation

- Run the smallest relevant check for the change and report what was and was not verified.
- The application uses MongoDB; account for that dependency when running or testing API code.
- Do not claim tests passed unless they were actually run.
