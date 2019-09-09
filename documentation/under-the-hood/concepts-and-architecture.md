# Concepts & Architecture

## System architecture

![](../../.gitbook/assets/frame%20%285%29.png)

\*\*\*\*[**Sofie Core**](dictionary.md#sofie-core) is a web-server and communicates with the web GUI.  
[Gateways](dictionary.md#gateways) are connected to Sofie Core and exchanges data; such as rundown-data for ingest or the [timeline ](dictionary.md#timeline)for play-out.

The rundown-data is fed into Sofie Core via the **Spreadsheet Gateway** \(in this example, it could also be a MOS Gateway or some other ingest-type Gateway\).  
The rundown-data is then interpreted by the Blueprints and stored in the Core database.

The end user controls the show via the web-interface. A show is mainly driven by the user [Take](dictionary.md#take-point):ing the next [Part](dictionary.md#part) in the Rundown.  
Upon a Take, Sofie Core calculates what's going to be played, in the form of a new [timeline](dictionary.md#timeline).

The **Playout Gateway** then picks up the new timeline, and...

* Resolves the timeline
* Calculates new target-states for each relevant point in time
* Maps the target-state to each play-out device.
* Compares the target-states for each device with the currently-tracked-state and..
* ..generates commands to send to each device to account for the change.
* The commands are then put on queue and sent to the devices at the correct time.



## Blueprints

TODO: write a longer explanation about blueprint and how they work.

Also read: [Blueprints in the Dictionary](dictionary.md#blueprints)

## Timeline

### Why a timeline?

### How does it work?



