# AGENTS.md

## Project Goal

Build a simple, minimalist personal website for GitHub Pages. The site should be
text-first and easy to maintain, similar in spirit to paulgraham.com and
patrickcollison.com, but with a modern feel.

The desired outcome is not a marketing landing page. It should feel like a
personal home on the web: quiet, fast, readable, and durable.

## Design Direction

- Prefer a sparse, content-led layout with generous whitespace.
- Keep the first screen useful: name, short bio, primary links, and a clear path
  to writing/projects/contact.
- Use modern typography, spacing, and responsive behavior to make the site feel
  current without becoming visually busy.
- Use a quiet system sans-serif font stack across the whole site, favoring San
  Francisco on Apple platforms and Helvetica Neue where available.
- Favor plain HTML links and simple lists over decorative cards.
- Use restrained color. A mostly neutral palette with one accent color is fine.
- Make essays, notes, links, and project pages comfortable to read on mobile and
  desktop.
- Avoid hero marketing sections, stock imagery, large gradients, animations for
  their own sake, and heavy visual effects.

## Technical Direction

- This site is served by GitHub Pages, so prefer static files that work without a
  server-side runtime.
- Keep the stack minimal. Plain HTML, CSS, and small amounts of JavaScript are
  preferred unless there is a clear reason to add tooling.
- Do not introduce a frontend framework, package manager, build pipeline, or CSS
  framework unless the task genuinely requires it.
- If using Jekyll because of GitHub Pages conventions, keep it simple and
  document any local commands added.
- Optimize for long-term maintainability: readable file names, obvious
  structure, and easy manual edits.
- Ensure pages work when served from the repository root on GitHub Pages.

## Content Structure

Recommended initial structure:

- `index.html`: homepage with name, short introduction, and links.
- `style.css`: global styles.
- `writing/`: essays or notes, if/when added.
- `projects/`: project pages or a project index, if/when added.
- `assets/`: images, icons, and other static assets.

Keep content real and concise. Use placeholder text only when necessary, and make
it obvious that it should be replaced.

## Quality Bar

- The site must be responsive and readable on narrow mobile screens.
- Before finishing layout changes, verify `/` and every page in `writing/` at
  320px, 375px, 768px, and desktop widths. There should be no horizontal
  overflow, clipped content, or narrow one-word text columns.
- Prefer broadly supported responsive CSS such as `width: calc(100% - 28px)`
  plus `max-width` for centered content containers.
- Use semantic HTML where possible.
- Maintain good contrast and visible focus states.
- Keep page weight small and loading fast.
- Avoid layout shifts caused by late-loading assets.
- Check links and asset paths before finishing.

## Local Verification

For a static site, verify with a local server from the repository root:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

If a different build or preview command is introduced later, document it in this
file and in `README.md`.
