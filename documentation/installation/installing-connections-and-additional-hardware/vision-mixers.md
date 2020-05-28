# Configuring Vision Mixers for Sofie

## ATEM - Blackmagic Design 

The [Playout Gateway](../installing-a-gateway/playout-gateway.md) supports communicating with the entire line up of Blackmagic ATEM vision mixers.

### Connecting Sofie

Once your ATEM is properly configured on the network, you can add it as a device to the Sofie Core. To begin, navigate to the _Settings page_ and select the _Playout Gateway_ under _Devices_. Under the _Sub Devices_ section, you can add a new device with the _+_ button. Edit it the new device with the pencil \( edit \) icon add the host IP and port for your ATEM. Once complete, you should see your ATEM in the _Attached Sub Devices_ section with a _Good_ status indicator.

### Additional Information

Sofie does not support connecting to a vision mixer hardware panels. All interacts with the vision mixers must be handled within a Rundown.

