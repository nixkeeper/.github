# <picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/nixkeeper/nixkeeper/main/assets/brand/nixkeeper-lockup-dark.svg"><img src="https://raw.githubusercontent.com/nixkeeper/nixkeeper/main/assets/brand/nixkeeper-lockup.svg" alt="nixkeeper" height="64"></picture>

Health dashboard for nixpkgs packages: new releases, build and update
failures, and vulnerabilities, in one place.

[**nixkeeper.com**](https://nixkeeper.com/) (every nixpkgs package) ·
[demo](https://demo.nixkeeper.com/) (one maintainer's lists) ·
[status](https://status.nixkeeper.com/) ·
[how it works](https://github.com/nixkeeper/nixkeeper/blob/main/docs/how-it-works.md)

## Repositories

| Repository | What it is |
|---|---|
| [**nixkeeper**](https://github.com/nixkeeper/nixkeeper) | The dashboard: joins the digests into one page, every 3 hours. Fork it for a dashboard of your own lists |
| [**nixkeeper-mcp**](https://github.com/nixkeeper/nixkeeper-mcp) | MCP server, so an AI assistant can answer questions about nixpkgs packages from nixkeeper's data |
| [**status**](https://github.com/nixkeeper/status) | Whether every sync, digest, test and token is on time, with an issue when one needs attention |

The digests: each reads one public source for all of nixpkgs and publishes
what it finds, for nixkeeper and anyone else.

| Digest | Reads | Every |
|---|---|---|
| [**digest-builds**](https://github.com/nixkeeper/digest-builds) | Hydra's latest evaluation of nixpkgs master (and staging-next, haskell-updates) | hour |
| [**digest-versions**](https://github.com/nixkeeper/digest-versions) | Repology, GitHub releases and per-ecosystem indexes (CRAN, Emacs, Stackage, Typst) | 12 hours |
| [**digest-update-bot**](https://github.com/nixkeeper/digest-update-bot) | nixpkgs-update's latest attempt at every package, and its queue | 3 hours |
| [**digest-vulnerabilities**](https://github.com/nixkeeper/digest-vulnerabilities) | The NixOS security tracker and OSV | hour |
| [**digest-prs**](https://github.com/nixkeeper/digest-prs) | nixpkgs' open PRs and issues, sorted by what they change | hour |

## Get started

- [Find your packages](https://nixkeeper.com/) on nixkeeper.com, by name
  or maintainer.
- [A dashboard of your own](https://github.com/nixkeeper/nixkeeper/blob/main/docs/your-own-instance.md):
  a fork with your package lists, about 15 minutes in GitHub's web pages.
- [Get notified](https://github.com/nixkeeper/nixkeeper/blob/main/docs/notifications.md)
  when your packages need attention.
- [Ask an assistant](https://github.com/nixkeeper/nixkeeper-mcp#using-it)
  with nixkeeper-mcp.

## AI & automation disclosure

nixkeeper's code and documentation are written with the assistance of an AI
(Claude, by Anthropic), with a person in the loop: its maintainer decides
what to build, and reviews and tests every change before it's merged. The
digests and syncs are automation that read public data. None of it ever
comments on, closes or merges anything in nixpkgs.

nixkeeper is an independent community project, not affiliated with or
endorsed by the NixOS Foundation. Everything here is MIT licensed.
