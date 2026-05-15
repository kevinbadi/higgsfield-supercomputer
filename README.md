# Higgsfield Supercomputer

A personal command center for [Higgsfield AI](https://higgsfield.ai) generations — a single-file HTML dashboard paired with a pre-loaded bundle of Higgsfield Claude Skills. Fork it, hook up your Higgsfield API key, and you're running.

## What's in this repo

- **`dashboard.html`** — Self-contained dashboard. No build step, no dependencies. Open it in a browser.
- **`.agents/skills/`** — Four Higgsfield Claude Skills, pre-installed:
  - `higgsfield-generate` — image/video generation across the full Higgsfield model catalog (Soul, Nano Banana, Seedance, Kling, Marketing Studio, etc.)
  - `higgsfield-soul-id` — Soul Character (face/identity) training
  - `higgsfield-marketplace-cards` — listing card generation
  - `higgsfield-product-photoshoot` — product photography
- **`skills-lock.json`** — version manifest pinning the four skills above to [`higgsfield-ai/skills`](https://github.com/higgsfield-ai/skills) on GitHub.

## Quick setup

### 1. Clone the repo

```bash
git clone https://github.com/kevinbadi/higgsfield-supercomputer.git
cd higgsfield-supercomputer
```

### 2. Install the Higgsfield CLI

```bash
curl -fsSL https://raw.githubusercontent.com/higgsfield-ai/cli/main/install.sh | sh
```

### 3. Authenticate

Get a Higgsfield account at [higgsfield.ai](https://higgsfield.ai), then:

```bash
higgsfield auth login
```

Verify with `higgsfield account status`.

### 4. Skills

If you're using a runtime that picks up project-level skills from `.agents/skills/` (e.g. Claude Code in this directory), the four Higgsfield skills load automatically. Otherwise, install them via your skills manager using `skills-lock.json` as the manifest.

### 5. Open the dashboard

```bash
open dashboard.html
```

## Customizing the dashboard

`dashboard.html` ships with all media `src=""` attributes intentionally blank — your fork starts clean. Drop your own generation URLs (videos, image thumbnails, hero clips) into the `src` attributes to populate the gallery.

Layout is fully responsive (mobile / tablet / desktop) and the visual system is defined as CSS variables at the top of the `<style>` block if you want to retheme.

## License

No license file ships with this repo by default — add one (MIT is a safe pick) if you plan to distribute beyond personal use.
