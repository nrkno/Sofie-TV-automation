# MOS Gateway

The MOS Gateway communicates with a device that supports the MOS protocol to ingest and remain in sync with a rundown.It can connect to any editorial system that uses version 2.8.1 of the MOS protocol, such as ENPS, and sync their rundowns with the _Sofie Core_. The rundowns will update in real time and any changes made will be seen from within your Playout Timeline. 

The setup for the MOS Gateway is already in the Docker Compose file you downloaded earlier. Remove the _\#_ symbol from the front of the line labeled `image: sofietv/tv-automation-mos-gateway:develop` and add a _\#_ to the other ingest gateway that was being used.

### Further Reading

* [MOS Gateway](https://github.com/nrkno/tv-automation-mos-gateway) GitHub Page for Developers

