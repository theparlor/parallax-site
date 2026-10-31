---
title: "History rewrite: two client names in vendored kit comments purged from public history"
type: retirement
maturity: final
created: 2026-10-31
kind: history-rewrite
repo: git@github.com:theparlor/parallax-site.git
repo_visibility: public
holds_it: bundle ~/.local/state/retired-history-bundles/parallax-site-pre-name-purge-2026-10-31.bundle (git bundle verify passed 2026-10-31, sha256 5ddf235ec13402147db108749af705d8b10e81ff0f6be5f03add28b2ddafe84c, 199974 bytes, every ref as of the rewrite); local tag archive/pre-name-purge-2026-10-31 in the primary checkout (never pushed)
tip_before: 255f38a1fe8e6d6ec1244371416c3db647740dff
tip_after: d23c105a39dd820f7326395019be6143e65860f0
commits_before: 59
commits_after: 57
kit_lines_rewritten: 17
paths_changed_at_tip: 0
---

# History rewrite: two client names in vendored kit comments purged from public history

## Why

This public repo carries a vendored copy of the session kit (`.agents/bin/`, `.agents/KIT_VERSION`).
Two provenance comments in the kit, in `.agents/bin/agent_repo_audit.py` (near line 233, kit 26) and
`.agents/bin/retirement.py` (near line 491, kit 31), named the client engagement where a kit bug had
been found. The daily public repo guard (governance audit Check 33) reported them on 2026-10-31 as 2 block
hits in each of 16 public site repos. Five older kit comment lines, reworded in the kit on 2026-10-02
(kit 22), carried the same client name in this repo's earlier commits.

Brien's instruction of 2026-10-31, given in reply to a message naming exactly these two kit comments in all
16 public site repos: "address without permanently losing data". That is the yes for this rewrite and for the merged public-render PR
that fixed the tip first. The 2026-10-03 ruling on the same decision surface (WS-DDR-156) had left the
15 product site repos' old commits in place; this instruction is the later and specific one, and it is
applied with the bundle below so nothing is lost.

The kit source in private Core keeps its wording (KF-05: names are allowed in private Core; KF-01: an
original is never rewritten to redact). What changed is this public copy only, at egress (KF-06). The
kit installer now writes a public render into site repos (org-design-tooling 0c47b81, 2026-10-31), so a
future kit sync carries the same public wording this rewrite leaves.

## What changed

- `git filter-repo --replace-text` over a fresh mirror clone, 2026-10-31: 17 diff line(s) across every
  ref carried one of the seven kit substrings; each became the kit's own public wording ("an engagement
  repo", "one engagement repo", "the largest engagement repo", dates and counts kept). Commit messages,
  authors, dates and every other blob are unchanged.
- Every branch and tag was force-pushed explicitly; `refs/pull/*/head` cannot be pushed and stay as
  GitHub holds them. Remote main confirmed at d23c105a39dd after the push.
- Rulesets at push time: 23693649:no-entire-checkpoint-refs:no; classic branch protection: none.
  Nothing refused the push, so nothing was paused.
- Paths whose blob differs between the old and the new tip: none (the tip already carried the public wording from the merged public-render PR).
- GitHub Pages after the push: built (build of 776bc92cc06a at 2026-10-31T08:52:13Z).

The commit count fell from 59 to 57: the merged public-render PR's squash commit changed only these two lines, so the rewrite emptied it and filter-repo pruned it. Its content is the tip's content; its PR and head ref stay on GitHub.

6 other diff line(s) in this repo's history name a client in page content (not the kit). The 2026-10-03 ruling (WS-DDR-156) left those old page commits in place; they are outside this rewrite and are listed in the run's report for a ruling of their own.

## Recover

Nothing here is gone. The bundle holds every ref of the repo as it stood on GitHub before the rewrite,
outside the repo; the local tag pins the last pre-rewrite main in the primary checkout.

```bash
git bundle verify ~/.local/state/retired-history-bundles/parallax-site-pre-name-purge-2026-10-31.bundle
git clone ~/.local/state/retired-history-bundles/parallax-site-pre-name-purge-2026-10-31.bundle parallax-site-pre-name-purge-2026-10-31
# the last pre-rewrite main in the primary checkout:
git -C <primary> show archive/pre-name-purge-2026-10-31:.agents/bin/retirement.py
```

The bundle and the tag are never pushed. Re-publishing the old history would reintroduce the two
names and needs an explicit ruling.

## Residual, stated plainly

GitHub keeps the old commits reachable by SHA, through cached views and through the `refs/pull/N/head`
refs of every merged PR, until its own garbage collection runs. Forks and third-party caches may hold
copies. Full removal from GitHub needs a support request, and that request is Brien's call.
