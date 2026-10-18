# Security policy

This is the policy of every repository in the
[nixkeeper organisation](https://github.com/nixkeeper) without one of its
own ([nixkeeper](https://github.com/nixkeeper/nixkeeper) has
[its own](https://github.com/nixkeeper/nixkeeper/blob/main/SECURITY.md)).

## Supported versions

Only the latest release (where there are releases) and `main` get security
fixes.

## Reporting a vulnerability

Please report it privately, through GitHub's private vulnerability
reporting: the repository's Security tab → "Report a vulnerability". Not
in a public issue.

Say what's affected and how to reproduce it, if you can.

## What's in scope

- the repository's code
- its GitHub Actions workflows: for example, anything that could misuse
  their token, or write to its `data` branch or open issues unintentionally
- what it publishes (a digest's data, the status page): for example, script
  injection through data a page shows

## What's not

- Vulnerabilities in a nixpkgs package: report them to that project, or to
  nixpkgs through [its security process](https://github.com/NixOS/nixpkgs/security).
- Issues in the services the digests read (Hydra, Repology, the
  nixpkgs-update logs, the NixOS security tracker, OSV, GitHub): report
  them to those projects.

## What to expect

nixkeeper is a small volunteer project, maintained on a best-effort basis.
Expect an acknowledgement within about a week, and a fix or an explanation
after that. There's no bug bounty. Once fixed, the report is credited,
unless you'd rather not be named.
