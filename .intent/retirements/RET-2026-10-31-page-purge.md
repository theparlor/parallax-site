---
title: "History rewrite: client names in page content purged from public history"
type: retirement
maturity: final
created: 2026-10-31
kind: history-rewrite
repo: git@github.com:theparlor/parallax-site.git
repo_visibility: public
holds_it: bundle ~/.local/state/retired-history-bundles/parallax-site-pre-page-purge-2026-10-31.bundle (git bundle verify passed 2026-10-31, sha256 a18a5094c75f3ad05d18541ef563e155d5c301496457afd9ebb99b944bdcafea, 316503 bytes, every ref as of the rewrite); local tag archive/pre-page-purge-2026-10-31 in the primary checkout (never pushed)
tip_before: 687d68284f55fb874a3ad6604d72a75bc2c79b9e
tip_after: 66937e6dc77980ff78e19adb6f6107b2fc17ca12
commits_before: 90
commits_after: 90
page_lines_rewritten: 6
paths: README.md, index.html
---

# History rewrite: client names in page content purged from public history

## Why

Page content in this public repo (`README.md`, `index.html`) named a client engagement in its provenance wording from
2026-06-05. The wording was fixed going forward on 2026-10-02 ("Neutralize client names" commit), and the
2026-10-03 ruling on the history-purge decision surface (WS-DDR-156) left the old public commits in place:
"forward-fix the other 15 site repos". The 2026-10-31 purge of the vendored kit's comments
(`RET-2026-10-31-name-purge.md`, Brien: "address without permanently losing data") left these page lines as the only client names in this
repo's published history, and said so.

Brien, 2026-10-31, told that older names remain in page history in this repo and one other, which the
2026-10-03 forward-fix-only ruling had left alone: "i want these resolved". That supersedes the 2026-10-03 ruling for these
two repos. The private sources keep their wording (KF-01, KF-05); this is redaction at egress (KF-06) on a
public repo, with the bundle below so nothing is lost (KF-02).

## What changed

- `git filter-repo --replace-text` over a fresh mirror clone, 2026-10-31: 6 diff line(s) across branches and
  tags carried the old provenance phrase; each became the exact forward-fixed wording main already carries,
  so the tip's tree is unchanged. Commit messages, authors, dates and every other blob are unchanged.
- Every branch and tag was force-pushed explicitly; `refs/pull/*/head` cannot be pushed and stay as GitHub
  holds them. Remote main confirmed at 66937e6dc779 after the push.
- Rulesets at push time: 23693649:no-entire-checkpoint-refs:no; classic branch protection: none.
  Nothing refused the push, so nothing was paused.
- GitHub Pages after the push: built (build of 66937e6dc779 at 2026-10-31T14:44:44Z).

## Recover

Nothing here is gone. The bundle holds every ref of the repo as it stood on GitHub before this rewrite
(after the kit-comment rewrite earlier the same day), outside the repo; the local tag pins the last
pre-rewrite main in the primary checkout.

```bash
git bundle verify ~/.local/state/retired-history-bundles/parallax-site-pre-page-purge-2026-10-31.bundle
git clone ~/.local/state/retired-history-bundles/parallax-site-pre-page-purge-2026-10-31.bundle parallax-site-pre-page-purge-2026-10-31
git -C <primary> show archive/pre-page-purge-2026-10-31:README.md
```

The bundle and the tag are never pushed. Re-publishing the old history would reintroduce the names and
needs an explicit ruling.

## Residual, stated plainly

GitHub keeps the old commits reachable by SHA, through cached views and through the `refs/pull/N/head`
refs of every merged PR, until its own garbage collection runs. Forks and third-party caches may hold
copies. Full removal from GitHub needs a support request, and that request is Brien's call.
