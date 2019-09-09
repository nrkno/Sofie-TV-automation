# Dictionary

### Sofie Core

The main application in the Sofie system.  
It is a web-server and serves the Web-GUI.  
It is a [NodeJS](https://nodejs.org) process backed up by a [MongoDB](https://www.mongodb.com/) database and based on the framework [Meteor](http://meteor.com).  
Read more: [_System architecture_](concepts-and-architecture.md#system-architecture)_,_ [_Getting Started_](../getting-started.md)\_\_

### Gateways

Gateways are NodeJS processes that connect to Sofie Core and provide different kinds of functionality.  
Examples of Gateways are the [MOS Gateway](https://github.com/nrkno/tv-automation-mos-gateway), the [Spreadsheet Gateway](https://github.com/SuperFlyTV/spreadsheet-gateway) and the [Playout Gateway](https://github.com/nrkno/tv-automation-playout-gateway).  
All gateways use the [Core-integration library](https://github.com/nrkno/tv-automation-server-core-integration) to communicate with Core.  
Read more: [_System architecture_](concepts-and-architecture.md#system-architecture)\_\_

### Blueprints

Blueprints are plug-ins that run in Sofie Core. They interpret the data coming in from the rundowns and transform them into a rich set of playable elements \(Segments, Parts, AdLibs etc\).

The blueprints are webpacked javascript bundles which is uploaded into Sofie via the GUI.

There are 3 types of Blueprints, and all 3 must be uploaded into Sofie before the system works.

* **System Blueprints** Handle things on the _System level_
* **Studio Blueprints** Handle things on the _Studio level_, like "which showstyle to use for this rundown"
* **Showstyle Blueprints** Handle things on the _Showstyle level_, like generating _Segments_, _Parts_ and _Timelines_ in a rundown.

The blueprints are custom-made and changes depending on the show style, type of input data and the controlled devices. A generic [blueprint based on spreadsheets is available here](https://github.com/SuperFlyTV/sofie-blueprints-spreadsheet).

Read more: [_System architecture_](concepts-and-architecture.md#system-architecture)\_\_

## Playing things

![](../../.gitbook/assets/takenext%20%281%29.png)

### TAKE-point

The Take point is currently playing Part in the rundown, indicated by the "On Air" line in the GUI.  
What's played on air is calculated from the timeline objects in the Pieces in the currently playing part.

### NEXT-point and Lookahead

The Next point is the next queued Part in the rundown. When the user clicks TAKE, the Next Part becomes the currently playing part, and the Next-point is also moved.  
Elements in the Next point \(or beyond\) might be pre-loaded or "put on preview", depending on the blueprints and playout devices used. This feature is called "Lookahead".

## Sofie setup

### System

### Studio

### Showstyle

### Migrations

## Rundown

A Rundown is what starts playing when you start a show. It contains Segments and Parts, which can be selected by the user to be played out.  
A Rundown always has a [showstyle](dictionary.md#showstyle) and is played out in the context of a [Studio](dictionary.md#studio).

Only one \(1\) Rundown can be active at the same time within each studio.

![The Producer&apos;s view and naming conventions of components](../../.gitbook/assets/sofie-naming-conventions.png)

### Segment

The Segment is the horizontal line in the GUI. It is intended to be used as a "chapter" or "subject" in a rundown, where each individual playable element in the Segment is called a [Part](dictionary.md#part).

### Part

### Piece

### Timeline-object

### AdLib

## Timeline

_Read more at_ [_Concepts and Architecture_](concepts-and-architecture.md#timeline)\_\_

