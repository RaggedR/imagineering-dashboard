# Imagineering Dashboard

Team activity dashboard for [Imagineering](https://imagineering.cc) — Melbourne build & share meetup.

**Live:** https://raggedr.github.io/imagineering-dashboard/

Pulls GitHub activity for each team member and displays identity cards, an interleaved activity timeline, and commit velocity charts. All data comes directly from the GitHub API — no backend required.

## Adding a team member

Edit the `TEAM` array at the top of `index.html`:

```js
const TEAM = [
  { name: 'Robin',  login: 'RaggedR' },
  { name: 'Nick',   login: 'nickmeinhold' },
  // Add new members here:
  // { name: 'Alice',  login: 'alice-gh' },
];
```

## Based on

This dashboard is adapted from [lyra-claudius-dashboard](https://github.com/RaggedR/lyra-claudius-dashboard) — same design language, same GitHub API approach, generalised from 2 hardcoded agents to N team members.
