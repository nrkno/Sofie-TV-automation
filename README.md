# Sofie: The Modern TV News Studio Automation System

This collection repository allows you to get an overview of the components necessary to assemble the *Sofie* system.


## Applications
* [Sofie Server Core](https://github.com/nrkno/tv-automation-server-core) Main application of the Sofie system.
* [CasparCG Server (NRK fork)](https://github.com/nrkno/tv-automation-casparcg-server) Sofie-specific fork of CasparCG Server 2.1.
* [CasparCG Media Scanner (NRK fork)](https://github.com/nrkno/tv-automation-casparcg-server) Sofie-specific fork of CasparCG Server 2.2 Media Scanner.

## Libraries
* [*Sofie* Server Core Integration](https://github.com/nrkno/tv-automation-server-core-integration) Used to connect to the Server Core (https://github.com/nrkno/tv-automation-server-core) from other Node processes.
* [*Sofie* Lawo State](https://github.com/nrkno/tv-automation-lawo-state/) Simple state model for basic Lawo audio mixer features, designed for Ember+ compliance.
* [*Sofie* ATEM State library](https://github.com/nrkno/tv-automation-atem-state) Compares two ATEM states.
* [*Sofie* ATEM Connection library](https://github.com/nrkno/tv-automation-atem-connection) Library for connecting to BlackmagicDesign ATEM devices.
* [*Sofie* MOS Connection library](https://github.com/nrkno/tv-automation-mos-connection/) Library for connecting to a MOS device.
* [*Sofie* Timeline State Resolver](https://github.com/nrkno/tv-automation-state-timeline-resolver) Orchestrates and controls different devices.
* [CasparCG Connection library](https://github.com/SuperFlyTV/casparcg-connection) Connect and interact with CasparCG Servers via Node.

## Protocols
* [*Sofie* Ember+ Connection](https://github.com/nrkno/tv-automation-emberplus-connection) Lawo's Ember+ control protocol for Node.

##Gateways
* [*Sofie* MOS Gateway](https://github.com/nrkno/tv-automation-mos-gateway) Gateway between *Server Core* and MOS devices.
* [*Sofie* Playout Gateway](https://github.com/nrkno/tv-automation-playout-gateway) Data exchange between *Server Core* and play-out devices.

## Helpers
* [*Sofie* CasparCG Launcher](https://github.com/nrkno/tv-automation-casparcg-launcher) Launcher, controller, and logger for CasparCG Server.
* [SuperFly-Timeline](https://github.com/SuperFlyTV/supertimeline) Resolver and rules for placing objects on a virtual timeline.
* [*Sofie* ]()

---

*The NRK logo is a registered trademark of Norsk rikskringkasting AS. The license does not grant any right to use, in any way, any trademarks, service marks or logos of Norsk rikskringkasting AS.*
