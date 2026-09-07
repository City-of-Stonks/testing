# Reference data

Trimmed copies of `cityofstonks.com`'s own public `/app` API responses,
kept here so the City Simulator replica has real reference data to build
and expand its trait engine against — not guesses.

Every file had its rendered SVG art stripped before being committed here.
This replica draws its own procedural buildings; it doesn't redistribute
the real site's generated artwork.

- **`config.json`** — site config: gating flags, the real `regions` and
  `countries` list (used for the Passport panel), wealth milestones.
- **`stats.json`** — site-wide aggregate counts (cities generated, etc).
- **`demo-sequence-traits.json`** — 12 example wallets from empty to
  $1M+ portfolio, each with its raw `stats` (txCount, tokenCount,
  portfolioValueUsd, ...) and the derived `traits` (wealthTier,
  activityLevel, diversityScore, buildingCount, buildingTypeWeights,
  skyMood, ...). This is the actual shape of their trait-derivation
  system — **the primary reference for tuning `deriveTraits()`** in
  `../index.html`. The thresholds this replica uses (wealthTier at
  $100/$1k/$10k/$100k, activityLevel at 10/50/500/5000 tx) were reverse-
  engineered from this file and match it, but `buildingCount` and
  `buildingTypeWeights` are approximations, not exact.
- **`building-types.json`** — the real building/vehicle category names
  (Commercial, Bank, Pagoda Tower, the token-linked ones like "Gigafactory"
  for TSLA, etc.) — labels only, used for the reference gallery and unlock
  naming.
- **`mint.json`** — real Robinhood Chain details (chain ID 4663, RPC URL,
  the City contract address, mint pricing/supply). Not currently used for
  live lookups — this replica's "Generate" is address-seeded and
  deterministic, not a real chain query — but it's here so a future pass
  can wire up real `nativeBalance`/Key-ownership checks the way
  `verify-bot-worker`/`city-raffle-worker` already do.
- **`riddle.json`**, **`wire.json`**, **`claim-status.json`** — snapshots
  of the riddle-game state, community "wire" posts, and partner-collection
  claim pool, kept in case either becomes its own replica later.

Not included (on purpose): `showcase.json`'s and `demo-sequence.json`'s
rendered SVGs, and `flags.json`'s pixel-flag art — those are the real
site's actual generated artwork, not just data.
