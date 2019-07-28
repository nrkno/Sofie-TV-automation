---
description: >-
  This library is used to connect to the Sofie Server Core from other Node
  processes.
---

# Sofie Server Core Integration

{% hint style="info" %}
Please note that this documentation is a work in progress, and that the content and links are likely to undergo drastic changes.
{% endhint %}

## Getting Started

### Typescript

```javascript
import { CoreConnection, PeripheralDeviceAPI } from 'tv-automation-server-core-integration'

// Set up our basic credentials:
let core = new CoreConnection({
    deviceId: 'device01',             // Unique id
    deviceToken: 'mySecretToken',    // secret token, used to authenticate this device
    deviceType: PeripheralDeviceAPI.DeviceType.PLAYOUT,
    deviceName: 'My peripheral device'
})
core.on('error', console.log)
// Initiate connection to Core:
core.init({
    host: '127.0.0.1',
    port: 3000
}).then(() => {
    // Connection has been established
    console.log('Connected!')
    // Set device status:
    return core.setStatus({
        statusCode: PeripheralDeviceAPI.StatusCode.GOOD,
        messages: ['Everything is awesome!']
    })
})
.catch((err) => {
    console.log(err)
})
```

## Development

### Installation

* Install Yarn from [https://yarnpkg.com](https://yarnpkg.com/)
* Install Jest, `yarn global add jest`
* Install npm dependencies, `yarn`

### Build

* Build, `yarn build`

### Testing

* Run tests, `yarn test`
* Run tests & watch, `yarn watch`

