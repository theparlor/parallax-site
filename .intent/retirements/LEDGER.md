---
title: Retirements ledger
type: ledger
maturity: final
created: 2026-10-02
---
# Retirements ledger

| Retired | Name | Kind | Holds it | Tip | Last real commit | Unique commits | Files | Why | Manifest |
|---------|------|------|----------|-----|------------------|----------------|-------|-----|----------|
| 2026-10-02 | core-client-cleanup | redaction | tag archive/pre-client-cleanup-2026-10-02 (local) | 9dcceb3d44574ecb6b8e74609b3ccba0b927cda4 | 9dcceb3d44574ecb6b8e74609b3ccba0b927cda4 | 0 | 2 | WS-DDR-153 client-content neutralization | .intent/retirements/RET-2026-10-02-core-client-cleanup.md |
| 2026-10-31 | parallax-site-wt-2026-10-31-public-render | worktree | tag `archive/agent/claude/2026-10-31-public-render-2026-10-31` | d23c105a | 2026-10-26 | 0 | 0 | Retired, work not on main: leftover of the 2026-10-31 public-render session: its one commit landed as the merged public-render PR, then the name purge rewrote history; nothing beyond main. | [RET-2026-10-31-session-retire-0452.md](RET-2026-10-31-session-retire-0452.md) |
| 2026-10-31 | pre-purge history (two client names in vendored kit comments) | history-rewrite | bundle `parallax-site-pre-name-purge-2026-10-31.bundle` in ~/.local/state/retired-history-bundles/ (sha256 5ddf235ec134, verified) + local tag `archive/pre-name-purge-2026-10-31` (never pushed) | 255f38a | 2026-10-31 | 59 commits rewritten to 57 | 17 kit lines | Two kit provenance comments named a client in this public repo (guard Check 33, 2026-10-31); purged at egress on Brien's 2026-10-31 instruction "address without permanently losing data", bundle first; new main d23c105 | [RET-2026-10-31-name-purge.md](RET-2026-10-31-name-purge.md) |
| 2026-10-31 | pre-purge history (client names in page content) | history-rewrite | bundle `parallax-site-pre-page-purge-2026-10-31.bundle` in ~/.local/state/retired-history-bundles/ (sha256 a18a5094c75f, verified) + local tag `archive/pre-page-purge-2026-10-31` (never pushed) | 687d682 | 2026-10-31 | 90 commits rewritten to 90 | 6 page lines in 2 file(s) | Page provenance wording named a client (fixed forward 2026-10-02; old commits left by the 2026-10-03 ruling); purged at egress on Brien's 2026-10-31 instruction "i want these resolved", bundle first; new main 66937e6 | [RET-2026-10-31-page-purge.md](RET-2026-10-31-page-purge.md) |
