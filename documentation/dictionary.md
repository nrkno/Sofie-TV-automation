# Features

{% hint style="info" %}
Reading tip: [Concepts & Architecture](features-and-configuration/concepts-and-architecture.md)
{% endhint %}

## Lobby



{% hint style="warning" %}
Documentation for this section is yet to be written.
{% endhint %}

In the lobby, all existing rundowns are listed.

## Rundown View

{% hint style="warning" %}
Documentation for this section is yet to be written.
{% endhint %}

The Rundown View is the main view that the producer is working in.

Things that should be covered: 

* What are all the labels, countdowns, colors, signs etc?



![The Rundown view and naming conventions of components](../.gitbook/assets/sofie-naming-conventions.png)

### Shelf

The shelf contains lists of AdLibs that can be played out.

![](../.gitbook/assets/shelf.png)

{% hint style="info" %}
The Shelf can be opened by clicking the handle at the bottom of the screen, or by pressing the TAB key
{% endhint %}

### Side panel

#### Notification center

{% hint style="warning" %}
Documentation for this section is yet to be written.
{% endhint %}

#### Switchboard

![Switchboard](../.gitbook/assets/switchboard.png)

### Playing things

![](../.gitbook/assets/takenext%20%281%29%20%281%29.png)

#### Take Point

The Take point is currently playing [Part](dictionary.md#part) in the rundown, indicated by the "On Air" line in the GUI.  
What's played on air is calculated from the timeline objects in the Pieces in the currently playing part.

The Pieces inside of a Part determines what's going to happen, the could be indicating things like VT:s, cut to cameras, graphics, or what script the host is going to read.

{% hint style="info" %}
You can TAKE the next [Part](dictionary.md#part) by pressing F12 or the Numpad Enter key.
{% endhint %}

#### Next Point

The Next point is the next queued Part in the rundown. When the user clicks _Take_, the Next Part becomes the currently playing part, and the Next point is also moved.

{% hint style="info" %}
Change the Next point by right-clicking in the GUI, or by pressing \(Shift +\) F9 & F10.
{% endhint %}

#### Lookahead

Elements in the [Next point ](dictionary.md#next-point)\(or beyond\) might be pre-loaded or "put on preview", depending on the blueprints and play-out devices used. This feature is called "Lookahead".

## Additional views

Sofie features a few separate views, such as the prompter, [read about them here](features-and-configuration/sofie-pages.md).

![](../.gitbook/assets/image%20%287%29%20%281%29.png)

