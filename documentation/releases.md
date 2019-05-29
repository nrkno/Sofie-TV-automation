---
description: >-
  A release specifies a set of versions of the components that make up a Sofie
  system.
---

# Releases

{% hint style="info" %}
Please note that this documentation is being actively developed during Q2 2019, and that the content and links are likely to undergo drastic changes from day to day. 
{% endhint %}

## Release 10

## Release 9 – v0.24.0-0 – 2019-05-16

### Features

#### **Take from anywhere**

_It is now possible to start playing from anywhere in a part, not just from the beginning of it_

* Merge branch 'feature/takeFromOffset' into develop \([e50c0cf](https://github.com/nrkno/tv-automation-server-core/commit/e50c0cf)\)
* feat: initial implementation of Take with Offset functionality \([9c860ca](https://github.com/nrkno/tv-automation-server-core/commit/9c860ca)\)
* fix: fix set offset working from UI \([91bc80d](https://github.com/nrkno/tv-automation-server-core/commit/91bc80d)\)
* fix: show full timecode for set with of offset \([0954ce6](https://github.com/nrkno/tv-automation-server-core/commit/0954ce6)\)

#### **Set In / Out points**

_UI for editing in & out-points of video clips_

* feat: clip trim panel WIP \([36e79dc](https://github.com/nrkno/tv-automation-server-core/commit/36e79dc)\)
* feat: clip trim panel WIP \([9d01c2b](https://github.com/nrkno/tv-automation-server-core/commit/9d01c2b)\)
* feat: clip trim panel working, hide video monitor under a flag \([72ee490](https://github.com/nrkno/tv-automation-server-core/commit/72ee490)\)
* feat\(clip trim dialog\): add an icon to mark a trimmed clip \([371ddb8](https://github.com/nrkno/tv-automation-server-core/commit/371ddb8)\)
* feat\(clip trim dialog\): implement timecode encoder \([32e8f89](https://github.com/nrkno/tv-automation-server-core/commit/32e8f89)\)
* feat\(clip trim panel\): more WIP on components \([05daa8f](https://github.com/nrkno/tv-automation-server-core/commit/05daa8f)\)
* feat\(clip trim\): WIP on styling Clip trimmer components \([1af8ff4](https://github.com/nrkno/tv-automation-server-core/commit/1af8ff4)\)

**Prompter**

_Teleprompter on a separate page \(see documentation in README\)_

* Merge branch 'feature/prompter2' into develop \([fc7c038](https://github.com/nrkno/tv-automation-server-core/commit/fc7c038)\)
* feat: prompter: add ^ and v indicators to where current take & next point is \([5c545e5](https://github.com/nrkno/tv-automation-server-core/commit/5c545e5)\)
* feat: prompter: continued implementation, url parameters etc \([785d0c0](https://github.com/nrkno/tv-automation-server-core/commit/785d0c0)\)
* feat: Prompter: New scroll mode: Smooth scrolling, which allows the user to use scroll wheel natural \([e25ae40](https://github.com/nrkno/tv-automation-server-core/commit/e25ae40)\)
* feat: refactor prompter view, prepare for modular controllers \([eb1ac27](https://github.com/nrkno/tv-automation-server-core/commit/eb1ac27)\)
* feat\(prompter\): add anchor points & movement tweaks \([c4ababe](https://github.com/nrkno/tv-automation-server-core/commit/c4ababe)\)
* feat\(prompter\): Add keyboard-controller, for control by keyboard-like devices \([c6e307d](https://github.com/nrkno/tv-automation-server-core/commit/c6e307d)\)
* feat\(prompter\): add mouse-ish controller, for control by mouse-like devices \([00a924f](https://github.com/nrkno/tv-automation-server-core/commit/00a924f)\)

#### **Invalid parts**

_If a part cannot be created properly by the blueprint, it can no be set as "invalid", which prevents it from being played out_

* Merge branch 'feature/invalid' into develop \([fc10b8c](https://github.com/nrkno/tv-automation-server-core/commit/fc10b8c)\)
* Merge remote-tracking branch 'origin/feature/invalidSegmentLine' into develop \([6ce8c04](https://github.com/nrkno/tv-automation-server-core/commit/6ce8c04)\)
* feat: implementation of invalid segmentLine & invalid segmentLineItem \(adLib\) \([7ddcede](https://github.com/nrkno/tv-automation-server-core/commit/7ddcede)\)
* feat: mark segmentline as invalid \([bd1f20c](https://github.com/nrkno/tv-automation-server-core/commit/bd1f20c)\)

#### **System & studio blueprints**

_The blueprints have now been split into system-, studio- & showStyle- blueprints_

* Merge pull request \#79 from nrkno/feature/system-studio-blueprints \([f3a67e2](https://github.com/nrkno/tv-automation-server-core/commit/f3a67e2)\), closes [\#79](https://github.com/nrkno/tv-automation-server-core/issues/79)
* feat: Batch uploading of blueprints in one http request \([5a707e1](https://github.com/nrkno/tv-automation-server-core/commit/5a707e1)\)
* feat: studio and system blueprints \([5ed64cf](https://github.com/nrkno/tv-automation-server-core/commit/5ed64cf)\)
* feat: Show assignment in blueprint settings \([2816d45](https://github.com/nrkno/tv-automation-server-core/commit/2816d45)\)
* feat: Studio blueprint now selects variant to use for ROs \([6131057](https://github.com/nrkno/tv-automation-server-core/commit/6131057)\)
* fix: Add migration to set type on existing blueprints \([f1b4f3c](https://github.com/nrkno/tv-automation-server-core/commit/f1b4f3c)\)
* fix: Creating blueprints in UI \([8419ecf](https://github.com/nrkno/tv-automation-server-core/commit/8419ecf)\)
* feat: Use studio baseline when no ro is active \([8353615](https://github.com/nrkno/tv-automation-server-core/commit/8353615)\)

#### **Other**

* Merge branch 'feature/rehaulVersions' into develop \([0e655f5](https://github.com/nrkno/tv-automation-server-core/commit/0e655f5)\)
* feat: add a user-definable CoreSystem.name that is displayed in the header and title bar \([493568e](https://github.com/nrkno/tv-automation-server-core/commit/493568e)\)
* feat: add notes to RunningOrder \([6100b0c](https://github.com/nrkno/tv-automation-server-core/commit/6100b0c)\)
* feat: Button to assign/unassign system blueprint \([edef22a](https://github.com/nrkno/tv-automation-server-core/commit/edef22a)\)
* feat: Crude UI to rerun studio baseline \([25b2395](https://github.com/nrkno/tv-automation-server-core/commit/25b2395)\)
* feat: log ClientResonseErrors as errors in userActionLog \([4bc10b5](https://github.com/nrkno/tv-automation-server-core/commit/4bc10b5)\)
* feat: bump blueprints-integration version \([6f2c46d](https://github.com/nrkno/tv-automation-server-core/commit/6f2c46d)\)
* feat: show RO notes as notifications \([0ebc3fe](https://github.com/nrkno/tv-automation-server-core/commit/0ebc3fe)\)
* feat: show timecodes in SegmentLineContextMenus \([5df6e15](https://github.com/nrkno/tv-automation-server-core/commit/5df6e15)\)
* feat: specific implementation: append Note on RunningOrder if segmentLine is not found \([a2ff6a2](https://github.com/nrkno/tv-automation-server-core/commit/a2ff6a2)\)
* feat: take from here UI item \([ca26660](https://github.com/nrkno/tv-automation-server-core/commit/ca26660)\)
* feat: change VideoEditMonitors behavior from hoverScrub to click-and-drag \([77327fe](https://github.com/nrkno/tv-automation-server-core/commit/77327fe)\)
* feat: Change styling for video monitors \([a01de7d](https://github.com/nrkno/tv-automation-server-core/commit/a01de7d)\)

### 

## Release 8 – v0.23.0 – 2019-04-08

### Features

**Set In / Out points \(preliminary implementation\)**

* stub of setting in & out points \([0852b42](https://github.com/nrkno/tv-automation-server-core/commit/0852b42)\)
* set in/out points through itemReplace \([4d31d70](https://github.com/nrkno/tv-automation-server-core/commit/4d31d70)\)

**GUI**

* SH-121-Double-clicking zoom-scrubber should mean "zoom to show everything in this segment" \([aeadc46](https://github.com/nrkno/tv-automation-server-core/commit/aeadc46)\)
* Add warning to rundown when config changed \(\#69\) \([4f5e6a9](https://github.com/nrkno/tv-automation-server-core/commit/4f5e6a9)\), closes [\#69](https://github.com/nrkno/tv-automation-server-core/issues/69)
* add httpWatcher settings \([fbb91d9](https://github.com/nrkno/tv-automation-server-core/commit/fbb91d9)\)
* add checkbox for debugLogging in media manager \([64b80e9](https://github.com/nrkno/tv-automation-server-core/commit/64b80e9)\)
* add option to input data into a ModalDialogue \([ef54b74](https://github.com/nrkno/tv-automation-server-core/commit/ef54b74)\)
* change labeled buttons to icons with tooltips in Media Transfer Status \([c5e582b](https://github.com/nrkno/tv-automation-server-core/commit/c5e582b)\)
* show user activity log for timeslot of recording \([5c75305](https://github.com/nrkno/tv-automation-server-core/commit/5c75305)\)
* speech synthesis \([eb9643a](https://github.com/nrkno/tv-automation-server-core/commit/eb9643a)\)
* support displayDurationGroups in rundown view \([460df8d](https://github.com/nrkno/tv-automation-server-core/commit/460df8d)\)
* feat\(countdowns\): display autonext \([1405a89](https://github.com/nrkno/tv-automation-server-core/commit/1405a89)\)
* add a user-definable CoreSystem.name that is displayed in the header and title bar \([717ee45](https://github.com/nrkno/tv-automation-server-core/commit/717ee45)\)

**Timeline vizualiser**

* implement timeline-visualizer view \([e725618](https://github.com/nrkno/tv-automation-server-core/commit/e725618)\)
* timeline-visualizer: add details-on-click \([c81243c](https://github.com/nrkno/tv-automation-server-core/commit/c81243c)\)
* move new timeline visualizer to replace the old broken one \([174dd7e](https://github.com/nrkno/tv-automation-server-core/commit/174dd7e)\)

**Evaluations**

* adds logging of evaluation level to keep statistics \([5da33a0](https://github.com/nrkno/tv-automation-server-core/commit/5da33a0)\)
* sends positive evaluations too \([d6c0bff](https://github.com/nrkno/tv-automation-server-core/commit/d6c0bff)\)

**Other**

* **playout:** Block take during transitions \([d0628a2](https://github.com/nrkno/tv-automation-server-core/commit/d0628a2)\)
* **blueprints:** Allow the post-process blueprint to modify a select few properties on the segmentL \([ee02813](https://github.com/nrkno/tv-automation-server-core/commit/ee02813)\)
* **config:** Add support for enum config entries \([b4ae4b5](https://github.com/nrkno/tv-automation-server-core/commit/b4ae4b5)\)
* **lookahead:** Delay lookahead after an object by 1s if it is labelled by a class \([2c595fb](https://github.com/nrkno/tv-automation-server-core/commit/2c595fb)\)
* log WorkFlow success or failure \([8e7d9d7](https://github.com/nrkno/tv-automation-server-core/commit/8e7d9d7)\)
* allow admins to delete non-unsynced rundowns \([190ca36](https://github.com/nrkno/tv-automation-server-core/commit/190ca36)\)

## Release 7 – v0.22.0 – 2019-03-15

### [Changes](https://github.com/nrkno/tv-automation-server-core/blob/develop/meteor/CHANGELOG.md#0220-0-2019-03-01)

## Release 6 – v0.20.0 – 2019-02-05

### Changes

## Release 5 – v0.19.0 – 2019-01-11

### Changes

## Release 4 – v0.18.0 – 2018-12-17

## Release 3 – v0.15.0 – 2018-11-08

## Release 2 – v0.15.0 – 2018-10-16

## Release 1 – v0.11.0 – 2018-09-07

### Changed

* Initial release used live for the first time for three **NRK Sørlandet** shows in Kristiansand, Norway on 2019-09-10.

