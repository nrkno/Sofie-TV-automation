---
description: >-
  Media file management for pulling new files and deleting expired files on
  play-out devices. It is used by Sofie Server Core.
---

# Sofie Media Manager

The system allows to use local ingest, expected media items based on the Running Order contents, and simple watch folder mirroring workflows. Supported storage handlers include local folders and CIFS shares. Target platform for the system is Windows and the application is expected to be controlled using the Caspar CG Launcher, but the architecture is architecture-agnostic.

## Usage

```text
// Development:
yarn buildstart -host 127.0.0.1 -port 3000 -log "log.log"
// Production:
yarn build-win32
```

### CLI Arguments

| Argument | Description | Environment Value |
| :--- | :--- | :--- |
| `-host` | Hostname or IP of Core | `CORE_HOST` |
| `-port` | Port of Core | `CORE_PORT` |
| `-log` | Path to output log | `CORE_LOG` |
| `-id` | Device ID to use | `DEVICE_ID` |

## Installation for dev

* yarn
* yarn build
* yarn test

### dev Dependencies

* yarn [https://yarnpkg.com](https://yarnpkg.com/)
* jest yarn global add jest

