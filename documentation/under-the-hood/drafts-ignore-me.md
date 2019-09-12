# Drafts \(ignore this\)

{% hint style="danger" %}
This page contains loose notes, which will be refactored, rewritten, removed or relocated to other parts in the documentation.

Please ignore this page, or \(t\)read carefully :\)
{% endhint %}



## On front page:

_TODO: add examples of the GUI:_

* _Producer's view_
* _Details in the GUI_
  * _Next and Current line as gif / webm_
  * _hover-scrub as animated gif / webm_
  * _media-details, such as end-of-file and freeze-frames_
  * _Warnings from blueprints_
  * \_\_
* _Prompter_
* _Host-view_

## System Overview and the Current Integrations

_TODO: make new overview_

## ![Sofie System Overview](https://raw.githubusercontent.com/nrkno/Sofie-TV-automation/master/images/Sofie_NRK_May_10_2019.png)

## User Interface

All interaction with Sofie is currently done via a web. This makes the system very flexible as you can quickly spin up another session in case a machine goes down, you can have multiple operators working on the same show at the same time or you can give a single operator multiple interfaces  \(f.g. a traditional keyboard and screen plus a touchscreen tablet for a ShotBox\). Utilizing modern web technologies allows all these sessions to stay in sync in real time.

### Producers view

The producer gets the overview of the entire show. This view also lets them control the entire show as well as see all relevant timing information and warnings about media or playback. The producers view consist of a vertical list of _Segments_, representing large chunks of the show \(f.g. a story\), each of which contains a horizontal list of _Parts_, each being a small part of the _Segment_ - a single clip, a piece to camera or an interview. Every part contains items, such as cameras, media items, graphics objects, audio ques etc. They are intended to be stacked similar to how layers of an NLE would work, the background at the bottom and foreground items on top.



![The Producer&apos;s view and naming conventions of components](../../.gitbook/assets/sofie-naming-conventions.png)

#### Media status

We have a few tools that help the producer check if everything will play out correctly. Sofie can currently check for freeze frames and black frames, the correct format of the media \(resolution, frame-rate and interlacing\) and lastly we give the producer the possibility of previewing the media straight from the UI using something we call _hover-scrub_. Sofie also allows you to start playing from anywhere, so you don’t need to sit through the whole clip to see the last graphics item.

### Other views

Sofie also has pages for status monitoring and configuration. The status page gives information about the state of all the connected devices and is especially useful for support crew. The configuration pages are intended for installation and allow extensive configuration of the studio installation, layers and devices as well upgrading the database after a system update and uploading [blueprints](concepts-and-architecture.md#blueprints). For the presenter we offer a special screen containing information about the current and next Part, for example which camera is currently live or how long the current media item will be playing for. We also offer a teleprompter view that displays the script and can automatically scroll to the right Segments and Parts while the show progresses. This auto scrolling is especially useful during rehearsal when you might not play back through the show in a linear manner.

## During the show 

While producing the show, we give the producer what we call the “next” screen on the multiviewer. This essentially always shows the producer what source they are going to switch to next. But it is not limited to just the mixer: for example, it can also show the next item for playback. And in theory, this could be extended to any part of the show, for example scripts or camera robotics. Another tool the producer has available are _Ad-Libs_, from the latin ad libitum. _Global Ad-Libs_ are available throughout the entire show, this could be cameras and remote inputs. Other _Ad-Libs_ are context aware and may only become available when the producer is in a _Part_ where they can be used. During the whole show Sofie can send metadata to external systems, such as indexing and timing information.



## Blueprints 

The _blueprints_ are a key part of a Sofie installation, giving the system it's flexibility. _Blueprints_ are a set of JavaScript scripts that take any input rundown data, from for example ENPS, and transform it into elements that can be played back by Sofie. This is a really powerful concept, because the _blueprint programmer_ is free to put in any logic they see fit, relieving duties from journalists and producers that can be automated. Using web-standard JavaScript means that there is no custom scripting language to learn and there is a large pool of developers available. Additional tools are available to make Sofie _blueprint_ development quick and easy in an _Integrated Development Environment_, like [Visual Studio Code](https://code.visualstudio.com/) or [Atom](https://atom.io/), with features such as auto-complete or being able to see how changes in the blueprints affect the output in real time!

## Device support 

We currently \(August 2019\) support the Blackmagic Atem range, CasparCG and Quantel for playback, HyperDeck for recording and can control Pharos lighting systems and Panasonic PTZ cameras. Through the Sisyfos controller application we have support for Behringer, Midas and MIDI-compatible sound mixers. We also have support for the Ember+, OSC, HTTP and TCP protocols that allows us to control many more devices: audio mixers, lightning systems, tally lights, etc.

## Architecture 

The spine of a Sofie installation is the server-core: it serves the React-based UI to the user, connects to the Database and processes incoming and outgoing data using _Blueprints_. The server-core is built using [Meteor](https://www.meteor.com/).

In addition to the server-core, we use _gateways_ to connect to services and devices. Most notably we have the _MOS Gateway_ for connecting to ENPS and the _Playout Gateway_ for resolving the _Timeline_ and controlling playout devices.

The _Timeline_ is an abstraction level for playout, it allows us to tie objects \(a camera source, or a vt\) with timing information. The commands are generated from this timeline on the fly by comparing the next and the current state at a time and calculating what commands are needed to reach the next state.

The objects on the _Timeline_ are put there by server-core and based on the rundown. But before these objects can be put on the timeline they need to be created. This is one of the tasks of the _Blueprints_. The _Blueprints_ take data from a change in the input data \(f.g. ENPS\) and process it into objects that can be used to drive the UI as well as be put on the timeline.

