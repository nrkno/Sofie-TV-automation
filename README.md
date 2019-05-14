# NRK Sofie TV Automation

This is the documentation for the state-based studio automation system **Sofie**, used in live TV news production by the Norwegian public service broadcaster **NRK** since September 2018.

The documentation for the latest release of _Sofie_ is intended to be browsed at [https://sofie.gitbook.io/sofie-tv-automation](https://sofie.gitbook.io/sofie-tv-automation) while documentation for older releases can be found at [https://github.com/nrkno/Sofie-TV-automation/releases](https://github.com/nrkno/Sofie-TV-automation/releases)

[5-minute presentation from the EBU booth at IBC 2018](https://www.youtube.com/watch?v=LeJxtTA3zms).

![Sofie User Interface example](https://raw.githubusercontent.com/nrkno/Sofie-TV-automation/master/images/Sofie_GUI_example.jpg)

## Applications

* [**Sofie Server Core**](https://github.com/nrkno/tv-automation-server-core) Main application of the Sofie system.
* [**CasparCG Server** \(NRK fork\)](https://github.com/nrkno/tv-automation-casparcg-server) Sofie-specific fork of CasparCG Server 2.1.
* [**CasparCG Media Scanner** \(NRK fork\)](https://github.com/nrkno/tv-automation-casparcg-server) Sofie-specific fork of CasparCG Server 2.2 Media Scanner.
* [**Sofie Media Manager**](https://github.com/nrkno/tv-automation-media-management) Media file management for pulling new files and deleting expired files on play-out devices.

## Gateways

* [**Sofie MOS Gateway**](https://github.com/nrkno/tv-automation-mos-gateway) A [MOS protocol](http://mosprotocol.com/) gateway between _Server Core_ and MOS devices.
* [**Sofie Playout Gateway**](https://github.com/nrkno/tv-automation-playout-gateway) Data exchange between _Server Core_ and play-out devices.

## Libraries

* [**Sofie MOS Connection**](https://github.com/nrkno/tv-automation-mos-connection/) A [MOS protocol](http://mosprotocol.com/) library for connecting to a MOS device.
* [**Sofie Timeline State Resolver**](https://github.com/nrkno/tv-automation-state-timeline-resolver) Orchestrates and controls different devices.
* [**Sofie Server Core Integration**](https://github.com/nrkno/tv-automation-server-core-integration) Used to connect to the [Sofie Server Core](https://github.com/nrkno/tv-automation-server-core) from other Node processes.
* [**Sofie Blueprints Integration**](https://github.com/nrkno/tv-automation-sofie-blueprints-integration) Common types and interfaces used by both server-core and the user defined blueprints.
* [**SuperFly.tv CasparCG Connection**](https://github.com/SuperFlyTV/casparcg-connection) Connect and interact with CasparCG Servers via Node.
* [**SuperFly.tv CasparCG State**](https://github.com/superflytv/casparcg-state) Tracks the state of CasparCG Servers.
* [**Sofie ATEM State**](https://github.com/nrkno/tv-automation-atem-state) Compares two ATEM states.
* [**Sofie ATEM Connection**](https://github.com/nrkno/tv-automation-atem-connection) Library for connecting to BlackmagicDesign ATEM devices.
* [**Sofie Lawo State**](https://github.com/nrkno/tv-automation-lawo-state/) Simple state model for basic Lawo audio mixer features, designed for Ember+ compliance. _Not used at the moment._
* [**Sofie Ember+ Connection**](https://github.com/nrkno/tv-automation-emberplus-connection) Lawo's _Ember+_ control protocol for Node.
* [**Sofie HyperDeck Connection**](https://github.com/nrkno/tv-automation-hyperdeck-connection) Library for connecting to BlackmagicDesign Hyperdeck devices.

## Helpers

* [**Sofie CasparCG Launcher**](https://github.com/nrkno/tv-automation-casparcg-launcher) Launcher, controller, and logger for CasparCG Server.
* [**SuperFly.tv SuperFly-Timeline**](https://github.com/SuperFlyTV/supertimeline) Resolver and rules for placing objects on a virtual timeline.

## System Overview and the Current Integrations

## ![Sofie System Overview](https://raw.githubusercontent.com/nrkno/Sofie-TV-automation/master/images/Sofie_NRK_May_10_2019.png)

_The NRK logo is a registered trademark of Norsk rikskringkasting AS. The license does not grant any right to use, in any way, any trademarks, service marks or logos of Norsk rikskringkasting AS._

