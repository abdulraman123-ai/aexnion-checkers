# Aexnion Checkers

A standalone, installable Checkers app based on the Axion Games arena experience. This app exposes Checkers only; it does not show or link to the original multi-game catalogue.

## Included

- American/English 8×8 checkers rules: forced captures, multi-jumps, kings and game-end detection.
- Six AI strength settings and local two-player play.
- Global Arena: checkers-only matchmaking, live game updates, player search and active matches.
- Swiss tournaments restricted to Checkers, with registration, pairings, match progression and standings.
- Responsive interface and installable PWA.

## Data connection

The app currently uses the existing Axion Games Supabase backend. All live-game queries and tournament discovery in this app are scoped to the `checkers` game type; it does not read chess game rows or alter the original Vercel deployment. Player profiles and the Supabase project are shared with Axion Games.

Client settings use the public Supabase URL and publishable key. No service-role or secret key is placed in this repository.

## Deployment

This repository is a static browser app. Vercel should serve the root directory without a build command. The checked-in `app.*` and `styles.*` files are compressed browser bundles loaded by `index.html`.
