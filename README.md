# morte

A prototype package manager based on the Dhall configuration language.

## Development

This project uses Nix flakes to provide Rust. In WSL, install Nix
inside your Linux distribution and enable flakes if your Nix installation does
not already enable them. For the best filesystem performance, keep the
repository in the WSL filesystem (for example, under `~/src`) rather than
under `/mnt/c`. To enable flakes, add
`experimental-features = nix-command flakes` to your Nix configuration.

From the repository directory, enter the development shell and run the
executable:

```sh
nix develop
cargo run
```

To build it without running:

```sh
cargo build
```

Cargo creates `Cargo.lock` during the first build; commit it to keep
dependencies reproducible.
