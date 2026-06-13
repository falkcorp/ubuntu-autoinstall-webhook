<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [ubuntu-autoinstall-webhook — Additional Context](#ubuntu-autoinstall-webhook--additional-context)
  - [Project overview](#project-overview)
  - [Key directories](#key-directories)
  - [Critical constraints](#critical-constraints)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

<!-- file: .github/copilot-instructions.md -->
<!-- version: 2.4.0 -->
<!-- guid: 4d5e6f7a-8b9c-0d1e-2f3a-4b5c6d7e8f9a -->
<!-- last-edited: 2026-06-13 -->

# ubuntu-autoinstall-webhook — Additional Context

Org-wide coding standards (file headers, language rules, commit format) are at
**https://github.com/falkcorp/.github** and apply automatically to this repo.

For full project context: **CLAUDE.md** at the repo root.

## Project overview

Webhook server for Ubuntu autoinstall automation. Language: Go/Shell.

## Key directories

| Directory | Purpose |
|---|---|
| `cmd/` | Cobra subcommands (webserver, cert-issuer, dnsmasq-watcher, etc.) |
| `internal/` | Domain packages (certadmin, certissuer, configuration, database, webserver, etc.) |
| `pkg/proto/` | Protobuf-generated types |
| `docs/` | Project documentation |

## Critical constraints

- Uses buf for protobuf generation — run `buf generate` (not manual `protoc`) when changing `.proto` files.
- Config is loaded from `config.yaml` (see `config.yaml.example` for structure).
