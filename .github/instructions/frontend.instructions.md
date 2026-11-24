---
applyTo: "src/static/**/*.html,src/static/**/*.css,src/static/**/*.js"
---

## Frontend Guidelines

- Use semantic HTML and accessibility attributes, including appropriate alt text and ARIA labels. Maintain sufficient text contrast.
- Use responsive design so pages remain usable on mobile devices as well as wider screens.
- Validate HTML structure and semantic elements when changing markup.
- Keep the frontend framework-free and follow the existing DOM and event-handling patterns.
- Put shared presentation rules in `styles.css`; reuse existing CSS custom properties and component patterns where practical.
- Treat server and user-provided values as untrusted; avoid inserting them as raw HTML.
- Avoid unrelated layout or style changes.
