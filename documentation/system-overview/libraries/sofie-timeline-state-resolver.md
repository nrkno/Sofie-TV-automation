# Sofie Timeline State Resolver

{% hint style="info" %}
Please note that this documentation is a work in progress, and that the content and links are likely to undergo drastic changes.
{% endhint %}

## Abstract

This library orchestrates and controls different devices. Its input is a [supertimeline](../helpers/superfly.tv-superfly-timeline.md) data structure and a layer-to-device-map. Using the input, it resolves the expected state, diffs the state against current state and sends commands where necessary.

## Supported Devices

* [CasparCG](http://casparcg.com/) - using the [casparcg-connection](superfly.tv-casparcg-connection.md) library
* ATEM vision mixers - using the [atem-connection](sofie-atem-connection.md) library
* Hyperdeck record/playback - using the [hyperdeck-connection](sofie-hyperdeck-connection.md) library
* Lawo sound mixers - using the [emberplus](sofie-ember+-connection.md) library
* Panasoniz PTZ cameras
* Pharos devices
* Arbitrary HTTP-interfaces

## Development

### Installation

* Install yarn [https://yarnpkg.com](https://yarnpkg.com/)
* Install jest `yarn global add jest`
* Install dependencies `yarn` or `yarn install`

### Build

* Build: `yarn build`

### Testing

* run test `jest`
* watch `yarn watch`

