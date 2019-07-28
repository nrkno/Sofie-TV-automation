---
description: >-
  This library is used in the Sofie TV News Studio Automation System for
  connecting to Blackmagic Design ATEM devices.
---

# Sofie ATEM Connection

{% hint style="info" %}
Please note that this documentation is a work in progress, and that the content and links are likely to undergo drastic changes.
{% endhint %}

## Technology Highlights

* Typescript
* Yarn
* Jest
* standard-version
* codecov

## Installation

For usage by library consumers installation is as easy as:

```text
yarn add atem-connection
```

For library developers installation steps are as following:

```text
git clone https://github.com/nrkno/tv-automation-atem-connection
yarn
yarn build
```

If you want to make a contribution, feel free to open a PR.

## Usage

```javascript
const { Atem } = require('atem-connection')
const myAtem = new Atem({ externalLog: console.log })

myAtem.connect('192.168.168.240')

myAtem.on('connected', () => {
    myAtem.changeProgramInput(3).then((res) => {
        console.log(res)
        // ProgramInputCommand {
        //     flag: 0,
        //     rawName: 'PrgI',
        //     mixEffect: 0,
        //     properties: { source: 3 },
        //     resolve: [Function],
        //     reject: [Function] }
    })
    console.log(myAtem.state)
})

myAtem.on('stateChanged', function(err, state) {
  console.log(state); // catch the ATEM state.
});
```

### Documentation

You can find the generated type docs [here](https://nrkno.github.io/tv-automation-atem-connection/).

### Events

* `connected` This event will be fired once we have connected with the ATEM.
* `disconnected` Whenever the connection to the ATEM fails and does not recover within 5 seconds this is called.
* `stateChanged(state)` Whenever a packet from the ATEM is received that changes the state, this event will be fired.

## Debug

Set `debug=true` config option in order to see raw packets. This is especially useful for library developers.

```text
const myAtem = new Atem({ debug: true, externalLog: console.log })
```

```text
SEND <Buffer 10 14 53 ab 00 00 00 00 00 3a 00 00 01 00 00 00 00 00 00 00>
SEND <Buffer 80 0c 53 ab 00 00 00 00 00 03 00 00>
SEND <Buffer 80 0c 53 ab 00 00 00 00 00 03 00 00>
SEND <Buffer 80 0c 80 0f 00 01 00 00 00 41 00 00>
RECV <Buffer 00 0c 90 60 5f 76 65 72 00 02 00 10>...
```

## Test

This module will run tests by jest \(in the future\).

```text
$ yarn unit
```

