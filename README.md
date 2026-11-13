# morte

A prototype package manager based on the Dhall configuration language.

## Development

This project uses Nix flakes to provide GHC and Cabal. In WSL, install Nix
inside your Linux distribution and enable flakes if your Nix installation does
not already enable them. For the best filesystem performance, keep the
repository in the WSL filesystem (for example, under `~/src`) rather than
under `/mnt/c`. To enable flakes, add
`experimental-features = nix-command flakes` to your Nix configuration.

From the repository directory, enter the development shell and run the
executable:

```sh
nix develop
cabal run
```

To build it without running:

```sh
cabal build
```

The first Nix invocation creates `flake.lock`; commit that file to keep the
Nixpkgs version reproducible.
