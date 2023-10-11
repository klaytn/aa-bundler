# Getting started

A modular Go implementation of an ERC-4337 Bundler.

This is a fork of [Stackup bundler](https://github.com/stackup-wallet/stackup-bundler) modified for [Klaytn](https://github.com/klaytn/klaytn).

# Running an instance

See the `Bundler` documentation at [docs.stackup.sh](https://docs.stackup.sh/docs/erc-4337-bundler).

# Contributing

## Prerequisites

- Go 1.19 or later
- Access to a node with `debug_traceCall` API enabled for custom JavaScript tracing.

## Setup

```bash
# Installs https://github.com/cosmtrek/air for live reloading.
# Runs go mod tidy.
make install-dev

# Generates base .env file.
# All variables in this file are required and should be filled.
# Running this command WILL override current .env file.
make generate-environment

# Parses private key in .env file and prints public key and address.
make fetch-wallet
```

## Run bundler in `private` mode

Start a local bundler instance:

```bash
make dev-private-mode
```

If you need to reset the embedded database:

```bash
# This will delete the default data directory at /tmp/stackup_bundler
make dev-reset-default-data-dir
```

# License

Distributed under the GPL-3.0 License. See [LICENSE](./LICENSE) for more information.
