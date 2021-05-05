# MOS Gateway

The MOS Gateway communicates with a device that supports the [MOS protoco](http://mosprotocol.com/wp-content/MOS-Protocol-Documents/MOS-Protocol-2.8.4-Current.htm)l to ingest and remain in sync with a rundown. It can connect to any editorial system \(NCS\) that uses version 2.8.4 of the MOS protocol, such as ENPS, and sync their rundowns with the _Sofie Core_. The rundowns are kept updated in real time and any changes made will be seen in the Sofie GUI.

The setup for the MOS Gateway is handled in the Docker Compose in the [Quick Install](../../installing-sofie-server-core.md) page.

One thing to note if managing the mos-gateway manually: It needs a few ports open \(10540, 10541\) for MOS-messages to be pushed to it from the NCS.

### Further Reading

* [MOS Gateway](https://github.com/nrkno/tv-automation-mos-gateway) GitHub Page for Developers

