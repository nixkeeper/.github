# nixkeeper/.github

The [nixkeeper](https://github.com/nixkeeper) organisation's profile, and
the defaults its repositories use.

- [`profile/README.md`](profile/README.md): what GitHub shows on the
  organisation's page.
- The defaults, for every repository here that doesn't have its own (GitHub
  uses these instead; [nixkeeper](https://github.com/nixkeeper/nixkeeper)
  has its own of each):
  - [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md): the NixOS community's code
    of conduct, and how to report.
  - [`SECURITY.md`](SECURITY.md): reporting a vulnerability privately.
  - [`CONTRIBUTING.md`](CONTRIBUTING.md): issues, pull requests, commit
    messages, AI assistance.
  - [`SUPPORT.md`](SUPPORT.md): where to ask.
  - [`ACCESSIBILITY.md`](ACCESSIBILITY.md): what the pages do for
    accessibility, what falls short, and how to report a barrier.
  - [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/): the "Something
    looks wrong" form and links to Discussions, the status page and the
    security policy.
  - [`.github/pull_request_template.md`](.github/pull_request_template.md):
    the checklist.
- [`rulesets/`](rulesets/): the rulesets every repository has, as JSON to
  import (a repository's Settings → Rules → Rulesets → New ruleset → Import
  a ruleset); GitHub only enforces organisation rulesets on its paid plans.
  - [`main.json`](rulesets/main.json), in every repository but this one:
    `main` changes only through a pull request, squash-merged once
    `tests-and-lint` (GitHub Actions) passes on it as it is with today's
    `main`, and its review threads are resolved; no force pushes, no
    deleting it. The same as nixkeeper's (exported from it).
  - [`data.json`](rulesets/data.json), in the repositories that publish a
    `data` branch (nixkeeper, the digests, status): it can't be deleted,
    as it holds what the runs carry over (a build's last success, the
    attempts read so far). Their runs replace it with force pushes, which
    this allows.
  - [`release-tags.json`](rulesets/release-tags.json), in the repositories
    with releases (nixkeeper, nixkeeper-mcp): a `v*` tag can't be moved or
    deleted once pushed.

MIT, like the rest of nixkeeper.
