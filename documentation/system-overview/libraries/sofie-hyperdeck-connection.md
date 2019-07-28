---
description: >-
  This library is used in the Sofie TV News Studio Automation System for
  connecting to Blackmagic Design Hyperdeck devices.
---

# Sofie Hyperdeck Connection

{% hint style="info" %}
Please note that this documentation is a work in progress, and that the content and links are likely to undergo drastic changes.
{% endhint %}

## Technology highlights

* Typescript
* Yarn
* Jest
* standard-version
* codecov

## Installation

For usage by library consumers installation is as easy as:

```text
yarn add hyperdeck-connection
```

For library developers installation steps are as following:

```text
git clone https://github.com/nrkno/tv-automation-hyperdeck-connection
yarn
yarn build
```

If you want to make a contribution, feel free to open a PR.

## Usage

```javascript
const { Hyperdeck, Commands } = require('hyperdeck-connection')
const myHyperdeck = new Hyperdeck()

myHyperdeck.connect('192.168.168.100')

myHyperdeck.on('connected', (info) => {
    console.log(info)
    // ConnectionInfoResponse {
    //  protocolVersion: 1.6,
    //  model: 
    // }

    myHyperdeck.sendCommand(new Commands.RecordCommand('some_filename')).then(() => {
        console.log('recording')
    })

    myHyperdeck.sendCommand(new Commands.TransportInfoCommand()).then((transportInfo) => {
        console.log(transportInfo)
    })
})

myHyperdeck.on('notify.slot', function(err, state) {
  console.log(state); // catch the slot state change.
});
myHyperdeck.on('notify.transport', function(err, state) {
  console.log(state); // catch the transport state change.
});
```

### Events

* `connected` This event will be fired once we have connected with the hyperdeck.
* `disconnected` Whenever the connection is lost. connected may be fired against shortly after if the connection is restored

## Test

This module will run tests by jest.

```text
$ yarn unit
```

