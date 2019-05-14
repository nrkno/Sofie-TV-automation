---
description: >-
  An application for piping data between Sofie Server Core and MOS devices using
  the MOS Protocol.
---

# Sofie MOS Gateway

## MOS Protocol

Read more about the MOS Protocol at [www.mosprotocol.com](http://mosprotocol.com/). Sofie MOS Gateway uses MOS Protocol v2.8.4.

## Usage

```text
// Development:
npm run start -host 127.0.0.1 -port 3000 -log "log.log"
// Production:
npm run start
```

### CLI Arguments

| Argument | Description | Environment Variable |
| :--- | :--- | :--- |
| `-host` | Hostname or IP of Core | `CORE_HOST` |
| `-port` | Port of Core | `CORE_PORT` |
| `-log` | Path to output log | `CORE_LOG` |

## Installation for dev

* yarn
* yarn build

#### dev Dependencies

* yarn [https://yarnpkg.com](https://yarnpkg.com/)
* jest yarn global add jest
