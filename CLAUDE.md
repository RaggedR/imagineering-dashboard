# CLAUDE.md

## What This Is

Team activity dashboard for [Imagineering](https://imagineering.cc) — Melbourne build & share meetup. Displays identity cards, interleaved activity timeline, and commit velocity charts for team members.

**Live:** https://raggedr.github.io/imagineering-dashboard/

## Stack

Single-file vanilla HTML/CSS/JavaScript. GitHub REST API v3. No build step, no dependencies.

## Running

```bash
open index.html   # Just open in a browser
```

## Architecture

- `index.html` — Everything: styles, markup, and JavaScript
- Pulls GitHub activity for each team member via public API
- `TEAM` array at top of file defines members (name + GitHub login)
- localStorage caching (5-min TTL) to minimize API usage
- Optional GitHub token for 5,000 req/hr (vs 60 unauthenticated)

## Adding a Team Member

Edit the `TEAM` array at the top of `index.html`.
