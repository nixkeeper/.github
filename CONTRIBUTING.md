# Contributing

This guide is for every repository in the
[nixkeeper organisation](https://github.com/nixkeeper) without one of its
own; [nixkeeper](https://github.com/nixkeeper/nixkeeper) has
[a fuller one](https://github.com/nixkeeper/nixkeeper/blob/main/CONTRIBUTING.md).

- **Something wrong, or an idea?** Open an issue in the repository it's
  about, or ask in [nixkeeper's Discussions](https://github.com/nixkeeper/nixkeeper/discussions).
  For a bigger change, an issue first saves you work.
- **Pull requests** go to `main`. `nix flake check` runs the tests (which
  never use the network), the linters and the formatting check, as CI
  does; `nix fmt` formats; `nix develop` has the tools. Each repository's
  README says how to run it.
- **Commit messages** follow nixpkgs' style: `<area>: <what changed>`,
  short, no final period (`cli: read the queue once`).
- **AI assistance** is fine, with a person in the loop who understands and
  has tested the change; say so in the commit (`Assisted-by: <tool>`), as
  nixpkgs asks.
- **Never in nixpkgs:** nothing here comments on, closes or merges anything
  in NixOS/nixpkgs, and changes that would aren't accepted.

Everyone taking part follows the [code of conduct](CODE_OF_CONDUCT.md).
Contributions are under each repository's licence (MIT).
