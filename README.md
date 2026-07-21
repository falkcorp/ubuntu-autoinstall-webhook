<!-- file: README.md -->
<!-- version: 2.0.0 -->
<!-- guid: 4a7f1c92-3e58-4d0b-9c16-8b2d5e0f7a41 -->
<!-- last-edited: 2026-07-20 -->

# ubuntu-autoinstall-webhook — ARCHIVED

> **This repository is archived and no longer maintained.**
>
> Its functionality has been **superseded by the agent**,
> [`ubuntu-autoinstall-agent`](https://github.com/jdfalk/ubuntu-autoinstall-agent)
> — a comprehensive Ubuntu Server auto-installer with ZFS encryption and error
> recovery that absorbs the auto-install reporting this webhook handled.
>
> Please use `ubuntu-autoinstall-agent` for all new work. This repository remains
> read-only for historical reference only; issues and pull requests are closed.

---

A simple Go application to process Ubuntu auto-install reporting events.
Retained below for historical context.

## Build

```shell
go build -o webhook
./webhook serve
```
