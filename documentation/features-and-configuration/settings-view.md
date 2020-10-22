# Settings

{% hint style="warning" %}
The settings pages are only visible to users with the right [access level](sofie-navigation.md)!
{% endhint %}

Recommended read before diving into the settings: [System, \(Organization\), Studio & Show Style](concepts-and-architecture.md#system-organization-studio-and-show-style).

## System

The _System_ settings are settings for this installation of Sofie. In here goes the settings that are applicable system-wide.

{% hint style="warning" %}
Documentation for this section is yet to be written.
{% endhint %}

## Studio

A _Studio_ in Sofie-terms is a physical location, with a specific set of devices and equipment. Only one show can be on air in a studio at the same time.  
The _studio_ settings are settings for that specific studio, and contains settings related to hardware and play-out, such as:

* **Attached devices** - the Gateways related to this studio
* **Blueprint configuration** - ****custom config option defined by the blueprints
* **Layer Mappings** - Maps the logical _timeline layers_ to physical devices and outputs

The Studio uses a studio-blueprint, which handles things like mapping up an incoming rundown to a Showstyle.

## Show style

A _Showstyle_ is related to the looks and logic of a _show_, which in contrast to the _studio_ is not directly related to the hardware.  
The Showstyle contains settings like

* **Source Layers -** Groups different types of content in the GUI
* **Output Channels** - Indicates different output targets \(such as the _Program_ or _back-screen in the studio_\)
* **Blueprint configuration** - ****custom config option defined by the blueprints

{% hint style="warning" %}
Please note the difference between S_ource Layers_ and _timeline-layers:_

[Pieces ](../dictionary.md#piece)are put onto _Source layers_, to group different types of content \(such as a VT or Camera\), they are therefore intended only as something to indicate to the user what is going to be played, not what is actually going to happen on the technical level.

[Timeline-objects](../dictionary.md#timeline-object) \(inside of the [Pieces](../dictionary.md#piece)\) are put onto timeline-layers, which are \(through the Mappings in the studio\) mapped to physical devices and outputs.  
The exact timeline-layer is never exposed to the user, but instead used on the technical level to control play-out.

An example of the difference could be when playing a VT \(that's a Source Layer\), which could involve all of the timeline-layers _video\_player0_, _audio\_fader\_video_, _audio\_fader\_host_ and _mixer\_pgm._
{% endhint %}



## Migrations

The migrations are automatic setup-scripts that help you during initial setup and system upgrades.

There are system-migrations that comes directly from the version of Sofie Core you're running, and there are also migrations added by the different blueprints.

It is mandatory to run migrations when you've upgraded Sofie Core to a new version, or upgraded your blueprints.

