# Installing a Gateway

{% hint style="info" %}
Note: These instructions are written with the Playout Gateway in mind, but all of the [Gateways ](../under-the-hood/libraries.md#gateways)are installed in mostly the same fashion.
{% endhint %}

## Installation

_\(TODO: write installation instructions, using docker\)_

## Manual installation \(for developers\)

1. Clone the [tv-automation-playout-gateway](https://github.com/nrkno/tv-automation-playout-gateway) repository
2. `cd` into the `tv-automation-playout-gateway` directory
3. Run `yarn` to install all dependencies
4. Run `yarn buildstart -host localhost -port 3000`  to build and start the application. Note: set the host and port to your Server Core application.

The Gateway will now connect to Sever Core and register itself there.  
It should show up in the list of devices under settings \([http://localhost:3000/settings](http://localhost:3000/settings)\), so head over there to set the settings of the device.

