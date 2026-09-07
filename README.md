# testing

Source for the [Control Room](https://city-of-stonks.github.io/testing/) —
a live dashboard for the City of Stonks GitHub org. It lists every repo and,
for anything with GitHub Pages enabled, an inline preview so you can view
the site without leaving the dashboard.

- **Public repos and Pages status** are fetched live from the GitHub REST
  API (`api.github.com/orgs/City-of-Stonks/repos`) — no token involved, so
  it only ever sees what's already public.
- **Private repos** (bot workers with no Pages) get a small hand-maintained
  card instead, since a public page can't safely hold a token to query them
  for real.

This repo used to also stage the next version of
[Building Designer](https://github.com/City-of-Stonks/building-designer)
before that work was folded into `building-designer`'s `main` — this repo
is now just the dashboard.

No build step — open `index.html` directly, or use the
[live version](https://city-of-stonks.github.io/testing/).
