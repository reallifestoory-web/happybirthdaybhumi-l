# AGENTS.md

## Architecture
Static single-page site. `netlify.toml` publishes the repo root; there is no build step.

## Key files
- `index.html` — the whole card: markup, inline styles, and inline script.
- `img/bhumi.jpg` — original photo. Always reference it through the Image CDN (`/.netlify/images?url=/img/bhumi.jpg&w=<width>&fm=webp`), not directly.

## Conventions / decisions
- Keep everything in `index.html` in the existing compact style; the user supplied this HTML and wants it kept close to the original.
- `object-position: center 25%` keeps the face centered in the circular crop of the portrait photo.
- Clicking the photo lets a visitor swap in a local image preview (client-side only, not saved).
