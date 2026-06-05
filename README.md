# parallax-site

Public **published surface** for **Parallax** — the overhead view of a coherence stack.

> **Status: v0 · pressure-test · NOT a public launch.** Published under WS-DDR-106 (a marked,
> non-public, peer-pressure-test surface permitted pre-Phase-3). `noindex` on the page +
> `robots.txt` Disallow keep it out of search; the URL is for sharing with registered peers
> (e.g. architecture review), not for announcement. Full public launch still requires every
> Phase-3 activation-gate condition + Brien's explicit greenlight.

## What this is
A single navigable v0 surface that states the coherence-stack hypothesis and is built to be
*challenged* — it surfaces the open questions, the three articulation gates, and the honest
"serviceable market of one" framing. Source narrative hydrated from
`Core/products/parallax/` + `Core/ECOSYSTEM-MARKETING-NARRATIVE-2026-05-20.md`.

## How it relates
- **Source / internals:** `theparlor/parallax` (private) — specs, decisions, pressure-tests.
- **This repo:** the public published HTML only (no internals).
- **Render layer:** the Foundry type system (`Core/frameworks/design-systems/foundry/`) — a
  future pass re-renders this surface through Foundry's portfolio identity (Playfair/Spectral);
  v0 currently uses Parallax's Turnberry-derived Montserrat scaffold.
- **Front-door role:** Parallax is the overhead index that links the other `*-site` surfaces
  (intent-site, etc.) per the portfolio publishing pattern (WS-DDR-107).

## Deploy
GitHub Pages from `main` / root. `.nojekyll` present.
