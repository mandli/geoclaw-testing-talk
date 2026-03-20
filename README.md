# GeoClaw workshop talk (Quarto)

This directory contains a Quarto RevealJS slide deck for the talk:

**From Examples to Experiments: Reproducible workflows in GeoClaw**

## Local use

1. Install Quarto: <https://quarto.org/docs/get-started/>
2. Render the slides:

```bash
quarto render
```

3. Open the rendered deck in `docs/index.html`.

## Project layout

- `index.qmd` — main deck
- `_quarto.yml` — project configuration
- `styles.css` — custom styling on top of the default RevealJS theme
- `assets/` — SVG diagrams used in the slides
- `.github/workflows/publish.yml` — optional GitHub Pages deployment workflow

## Publishing options

### Option 1: simplest manual publish

This project renders to `docs/`, so you can:

```bash
quarto render
git add docs
```

Then set **GitHub Pages** to publish from:

- **Branch:** `main`
- **Folder:** `/docs`

### Option 2: GitHub Actions deployment

A workflow is included at `.github/workflows/publish.yml`.

To use it:

1. Push this project to GitHub.
2. In **Settings → Pages**, set **Source** to **GitHub Actions**.
3. If your default branch is `master` instead of `main`, adjust the workflow trigger.

The workflow will render the Quarto project and deploy the generated `docs/` artifact to GitHub Pages.

## Notes

- The deck is intentionally lightweight for a 15-minute workshop slot.
- Examples are GeoClaw-centered (`bowl_slosh` and `ike`) rather than generic Clawpack examples.
- The main framing is for users and power users: the point is not a developer-only test suite, but a repeatable workflow for runs and comparisons.
