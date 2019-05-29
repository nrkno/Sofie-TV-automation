---
description: >-
  A release specifies a set of versions of the components that make up a Sofie
  system.
---

# Releases

{% hint style="info" %}
Please note that this documentation is being actively developed during Q2 2019, and that the content and links are likely to undergo drastic changes from day to day. 
{% endhint %}

## Release 9 – v0.24.0-0 – 2019-04-12



#### Features

#### **Take from anywhere**

_It is now prossible to start playing from anywhere in a part, not just from the beginning of it_

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

#### 

#### Bug fixes

* fix: a bug where DEFAULT\_DISPLAY\_DURATION would be added to a 0-duration member of a displayDuration \([13f784d](https://github.com/nrkno/tv-automation-server-core/commit/13f784d)\)
* fix: add missing $ne \(not equal\) in mongoWhere \([53c76a8](https://github.com/nrkno/tv-automation-server-core/commit/53c76a8)\)
* fix: Blueprint selection input in studio settings \([fc80da1](https://github.com/nrkno/tv-automation-server-core/commit/fc80da1)\)
* fix: catch scroll events properly in later Chrome versions. \([7396973](https://github.com/nrkno/tv-automation-server-core/commit/7396973)\)
* fix: clip floating inspector values \([d4c7430](https://github.com/nrkno/tv-automation-server-core/commit/d4c7430)\)
* fix: fix an issue where some of the snapshot restores would not be recognized as JSON \([57d31bc](https://github.com/nrkno/tv-automation-server-core/commit/57d31bc)\)
* fix: fix an issue where the message for clip ingested would be "null, Clip is being ingested" \([7ac5672](https://github.com/nrkno/tv-automation-server-core/commit/7ac5672)\)
* fix: fix MOS status indicators in RO header \([c0724cc](https://github.com/nrkno/tv-automation-server-core/commit/c0724cc)\)
* fix: handle take situation better when having invalid segmentLines \([dacd3b0](https://github.com/nrkno/tv-automation-server-core/commit/dacd3b0)\)
* fix: issue with segment context menu \([7a44deb](https://github.com/nrkno/tv-automation-server-core/commit/7a44deb)\)
* fix: Made sure that the typography update for the prompter has a font fallback. \([6f2b20a](https://github.com/nrkno/tv-automation-server-core/commit/6f2b20a)\)
* fix: make segmentLine.invalid optional \([c179e3c](https://github.com/nrkno/tv-automation-server-core/commit/c179e3c)\)
* fix: missing key property \([79fb3e6](https://github.com/nrkno/tv-automation-server-core/commit/79fb3e6)\)
* fix: missing sass import \([f1f10ff](https://github.com/nrkno/tv-automation-server-core/commit/f1f10ff)\)
* fix: more fixes for MOS status indicator in header \([97311b1](https://github.com/nrkno/tv-automation-server-core/commit/97311b1)\)
* fix: on air label position \([00d4e20](https://github.com/nrkno/tv-automation-server-core/commit/00d4e20)\)
* fix: Prompter: keyboard device interface \([540f47a](https://github.com/nrkno/tv-automation-server-core/commit/540f47a)\)
* fix: rehaul of versions, WIP \([93dea2f](https://github.com/nrkno/tv-automation-server-core/commit/93dea2f)\)
* fix: rename "Edit" to "Trim" for clipTrimDialog \([3879a34](https://github.com/nrkno/tv-automation-server-core/commit/3879a34)\)
* fix: rewind all segments when re-enabling follow on air \([a23b84c](https://github.com/nrkno/tv-automation-server-core/commit/a23b84c)\)
* fix: systemStatus versions \([62bfa9a](https://github.com/nrkno/tv-automation-server-core/commit/62bfa9a)\)
* fix: upd query-string dependency & fixed typings issue \([e0d3f12](https://github.com/nrkno/tv-automation-server-core/commit/e0d3f12)\)
* fix: update timeline-visualizer \([8e46981](https://github.com/nrkno/tv-automation-server-core/commit/8e46981)\)
* fix: update typings \([d536ad1](https://github.com/nrkno/tv-automation-server-core/commit/d536ad1)\)
* fix: version handling \([4b9863a](https://github.com/nrkno/tv-automation-server-core/commit/4b9863a)\)
* fix: Update blueprints-integration \([9870256](https://github.com/nrkno/tv-automation-server-core/commit/9870256)\)
* fix: update blueprints-integration depencendy & update getHashId to match \([e1c12d2](https://github.com/nrkno/tv-automation-server-core/commit/e1c12d2)\)
* fix: make sure that expectedMediaItems are purged along with the RO \([0d9dda1](https://github.com/nrkno/tv-automation-server-core/commit/0d9dda1)\)
* fix: solve a problem with viewing recordings \([01c165b](https://github.com/nrkno/tv-automation-server-core/commit/01c165b)\)
* fix: handle when error is thrown in function in makePromise \([b7094dd](https://github.com/nrkno/tv-automation-server-core/commit/b7094dd)\)
* fix: multiply inPoint/duration by timeBase before sending back to MOS \([b576f26](https://github.com/nrkno/tv-automation-server-core/commit/b576f26)\)
* fix: write back TimeBase when changing EditorialStart/Duration \([8012cea](https://github.com/nrkno/tv-automation-server-core/commit/8012cea)\)
* fix: strip blueprint manifest versions of '^' \([54a5ecf](https://github.com/nrkno/tv-automation-server-core/commit/54a5ecf)\)
* fix: solve an issue with content trimmed icon \([461617f](https://github.com/nrkno/tv-automation-server-core/commit/461617f)\)
* fix: wait for response from MOS device until resolving segmentLineItemSetInOutPoints \([2572a11](https://github.com/nrkno/tv-automation-server-core/commit/2572a11)\)
* fix: resolve an issue with dropdown EditAttribute not selecting the undefined option \([9f85845](https://github.com/nrkno/tv-automation-server-core/commit/9f85845)\)
* fix: ensure that VideoEditMonitor is comfortably scrubbable at any window width \([a5e882a](https://github.com/nrkno/tv-automation-server-core/commit/a5e882a)\)
* fix: implement Play from here \([bd79569](https://github.com/nrkno/tv-automation-server-core/commit/bd79569)\)
* fix: backport timing changes for play-from-anywhere from R10 \([5d96b1e](https://github.com/nrkno/tv-automation-server-core/commit/5d96b1e)\)
* fix: hide "Restart playout" from support panel when not in studio mode \([5820b00](https://github.com/nrkno/tv-automation-server-core/commit/5820b00)\)
* fix\(displayDurationGroup\): fix GUI clocks for displayDurationGroups \([76e217e](https://github.com/nrkno/tv-automation-server-core/commit/76e217e)\)
* fix\(displayDurationGroup\): use displayDurationGroup timing in presenter's screen \([9138845](https://github.com/nrkno/tv-automation-server-core/commit/9138845)\)
* fix\(lookahead\): Give lookahead the correct limit when in the next SegmentLine during autonext \([0b20b9e](https://github.com/nrkno/tv-automation-server-core/commit/0b20b9e)\)
* fix\(lookahead\): Produced objects not resolving properly \([7660bf5](https://github.com/nrkno/tv-automation-server-core/commit/7660bf5)\)
* fix\(migrations\): Ensure there are migrations to run before running another batch \([c3d77b5](https://github.com/nrkno/tv-automation-server-core/commit/c3d77b5)\)

#### 

#### Other

* Merge branch 'develop' into feature/prompter2 \([a072747](https://github.com/nrkno/tv-automation-server-core/commit/a072747)\)
* Merge branch 'develop' into feature/prompter2 \([6f17ba8](https://github.com/nrkno/tv-automation-server-core/commit/6f17ba8)\)
* Merge branch 'develop' into feature/takeFromOffset \([39afebf](https://github.com/nrkno/tv-automation-server-core/commit/39afebf)\)
* Merge branch 'master' into release9 \([5cbbf5d](https://github.com/nrkno/tv-automation-server-core/commit/5cbbf5d)\)
* Merge branch 'release8' into develop \([8df5fbb](https://github.com/nrkno/tv-automation-server-core/commit/8df5fbb)\)
* Merge branch 'release8' into develop \([924837f](https://github.com/nrkno/tv-automation-server-core/commit/924837f)\)
* chore: added debug message in case of strange too-quick takes \([5863035](https://github.com/nrkno/tv-automation-server-core/commit/5863035)\)
* chore: bump blueprints integration \([00fc68c](https://github.com/nrkno/tv-automation-server-core/commit/00fc68c)\)
* chore: copy changelog from master \([4570223](https://github.com/nrkno/tv-automation-server-core/commit/4570223)\)
* chore: doc \([ab53256](https://github.com/nrkno/tv-automation-server-core/commit/ab53256)\)
* chore: fix changelog: remove duplicates & categorize commits \[skip-ci\] \([cd53594](https://github.com/nrkno/tv-automation-server-core/commit/cd53594)\)
* chore: improve confirmation dialogs \([dc123ba](https://github.com/nrkno/tv-automation-server-core/commit/dc123ba)\)
* chore: lint & merge runningOrderNotes \([0183d67](https://github.com/nrkno/tv-automation-server-core/commit/0183d67)\)
* chore: linting \([290bb4c](https://github.com/nrkno/tv-automation-server-core/commit/290bb4c)\)
* chore: merge changes from develop \([46b5775](https://github.com/nrkno/tv-automation-server-core/commit/46b5775)\)
* chore: merge changes from develop \([6ecaa62](https://github.com/nrkno/tv-automation-server-core/commit/6ecaa62)\)
* chore: merge latest changes from develop \([fa44fc8](https://github.com/nrkno/tv-automation-server-core/commit/fa44fc8)\)
* chore: merge latest changes from develop \([203ef70](https://github.com/nrkno/tv-automation-server-core/commit/203ef70)\)
* chore: move updateSpeech from render\(\) \([50c6142](https://github.com/nrkno/tv-automation-server-core/commit/50c6142)\)
* chore: refactor SegmentLineNotes; move & rename \([96d0947](https://github.com/nrkno/tv-automation-server-core/commit/96d0947)\)
* chore: Remove all references to the now unused defaultShowStyleVariant \([d49c633](https://github.com/nrkno/tv-automation-server-core/commit/d49c633)\)
* chore: upd TSR types dep \([9c4f339](https://github.com/nrkno/tv-automation-server-core/commit/9c4f339)\)
* chore: update package-lock.json \([eac327c](https://github.com/nrkno/tv-automation-server-core/commit/eac327c)\)
* chore: update to the latest develop changes \([bd2c3ec](https://github.com/nrkno/tv-automation-server-core/commit/bd2c3ec)\)
* chore: Updated prompter with the more legible font "Source Sans Pro" \(uses Open SIL license\) which w \([6a8e459](https://github.com/nrkno/tv-automation-server-core/commit/6a8e459)\)
* chore: use playOffset in RunningOrderTiming \([05756cc](https://github.com/nrkno/tv-automation-server-core/commit/05756cc)\)

## Release 8 – v0.23.0 – 2019-04-08

## Release 7 – v0.22.0 – 2019-03-15

## Release 6 – v0.20.0 – 2019-02-05

## Release 5 – v0.19.0 – 2019-01-11

## Release 4 – v0.18.0 – 2018-12-17

## Release 3 – v0.15.0 – 2018-11-08

## Release 2 – v0.15.0 – 2018-10-16

## Release 1 – v0.11.0 – 2018-09-07

### Changed

* Initial release used live for the first time for three **NRK Sørlandet** shows in Kristiansand, Norway on 2019-09-10.

