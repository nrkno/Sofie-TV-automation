---
description: >-
  An application for piping data between the Sofie Server Core and play-out
  devices (such as CasparCG Server, ATEM, Lawo, etc..)
---

# Sofie Playout Gateway

{% hint style="info" %}
Please note that this documentation is being actively developed during Q2 2019, and that the content and links are likely to undergo drastic changes from day to day. 
{% endhint %}

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
| `-id` | Device ID to use | `DEVICE_ID` |

## Installation for dev

* yarn
* yarn build
* yarn test

### Dev dependencies

* yarn [https://yarnpkg.com](https://yarnpkg.com/)
* jest yarn global add jest

