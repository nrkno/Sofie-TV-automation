---
description: >-
  A release specifies a set of versions of the components that make up a Sofie
  system.
---

# Releases



{% hint style="info" %}
Please note that this documentation is being actively developed during Q2 2019, and that the content and links are likely to undergo drastic changes from day to day. 
{% endhint %}

Current stable version: [Release 9](releases.md#release-9)

## _Upcoming: Release 12 \(work in progress\)_

See the [tracking issue on github](https://github.com/nrkno/Sofie-TV-automation/issues/5) for details __

## _Release 11 \(work in progress\)_

Status: Currently in testing, expected release date: mid-_August 2019_

### Main Features

 This release is a maintenance release, with only minor features.

* \*\*\*\*

See the [tracking issue on github](https://github.com/nrkno/Sofie-TV-automation/issues/4) for details

### Components

| Component | Version | Changelog |
| :--- | :--- | :--- |
| [Core](https://github.com/nrkno/tv-automation-server-core) | 0.26.0 \(TBD\) | _Changelog_ |
| [Blueprints API \( Core \)](https://www.npmjs.com/package/tv-automation-sofie-blueprints-integration) | TBD |  |
| [Blueprints API \( TSR \)](https://www.npmjs.com/package/timeline-state-resolver-types) | TBD |  |
| [Playout Gateway](https://github.com/nrkno/tv-automation-playout-gateway) | TBD |  |
| [Mos Gateway](https://github.com/nrkno/tv-automation-mos-gateway) | TBD |  |
| [Media Manager](https://github.com/nrkno/tv-automation-media-management) | TBD |  |

## Release 10

Release date: _2019-07-05_

### Main Features

 This release features a BIG refactoring and a lot of renamings. _Therefore, this release is NOT backwards compatible._

* **The Big Renaming** _A big refactoring and renaming of variables and data structures._

  _Some of the most prominent renamings are:_

  * _StudioInstallation -&gt; Studio_
  * _RunningOrder -&gt; Rundown_
  * _Segment \(unchanged\)_
  * _SegmentLine -&gt; Part_
  * _SegmentLineItem -&gt; Piece_

* **New ingest data pipeline** _****This is a step on the way to support different types of sources of input data._
* **New Timeline**  _This release also features the new_ [_Timeline_ ](https://www.npmjs.com/package/superfly-timeline)_\(version 7.0\), which gives better control and performance_
* **Unit tests & CI** _In order to achieve a safer development environment, higher code quality and catching bugs earlier, we've added Jest as test framework._

See the [tracking issue on github](https://github.com/nrkno/Sofie-TV-automation/issues/3) for details

### Components

| Component | Version | Changelog |
| :--- | :--- | :--- |
| [Core](https://github.com/nrkno/tv-automation-server-core) | 0.25.0 | \_\_[_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0250-2019-07-05)\_\_ |
| [Blueprints API \( Core \)](https://www.npmjs.com/package/tv-automation-sofie-blueprints-integration) | 0.23.0 |  |
| [Blueprints API \( TSR \)](https://www.npmjs.com/package/timeline-state-resolver-types) | 3.0.1 |  |
| [Playout Gateway](https://github.com/nrkno/tv-automation-playout-gateway) | 0.20.0 |  |
| [Mos Gateway](https://github.com/nrkno/tv-automation-mos-gateway) | 0.8.0 |  |
| [Media Manager](https://github.com/nrkno/tv-automation-media-management) | 0.2.0 |  |

## Release 9

Release date: 2019-05-16

### Main Features

* **Take from anywhere**  _Start playing from anywhere in a segmentLine, not just from the beginning of it_
* **Set In / Out points**  _UI for editing in & out-points of video clips_
* **Prompter**  _Teleprompter on a separate page \(se documentation in README\)_
* **Invalid SegmentLines**  _If a segmentLine cannot be created proberly by the blueprint, it can no be set as "invalid", which prevents it from being played out_
* **System & studio blueprints**  _The blueprints have now been split into system-, studio- & showStyle- blueprints_

### Components

| Component | Version | Changelog |
| :--- | :--- | :--- |
| [Core](https://github.com/nrkno/tv-automation-server-core) | 0.24.0 | \_\_[_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0240-2019-05-16)\_\_ |
| [Blueprints API \( Core \)](https://www.npmjs.com/package/tv-automation-sofie-blueprints-integration) | 0.19.0 |  |
| [Blueprints API \( TSR \)](https://www.npmjs.com/package/timeline-state-resolver-types) | 2.2.0 |  |
| [Playout Gateway](https://github.com/nrkno/tv-automation-playout-gateway) | 0.19.1 |  |
| [Mos Gateway](https://github.com/nrkno/tv-automation-mos-gateway) | 0.7.0 |  |
| [Media Manager](https://github.com/nrkno/tv-automation-media-management) | 0.1.8 \(no changes\) |  |
| [CasparCG](https://github.com/nrkno/tv-automation-casparcg-server) | [2.1.7\_NRK](https://github.com/nrkno/tv-automation-casparcg-server/releases/tag/v2.1.7_NRK) |  |
| [CasparCG Media-Scanner](https://github.com/nrkno/tv-automation-media-scanner) | [1.5.3\_NRK](https://github.com/nrkno/tv-automation-media-scanner/releases/tag/v1.5.3rc4) |  |

## Release 8

Release date: 2019-04-08

### Main Features

* **Set In / Out points** _\(preliminary implementation\)_
* **Timeline vizualiser**

### Components

| Component | Version | Changelog |
| :--- | :--- | :--- |
| [Core](https://github.com/nrkno/tv-automation-server-core) | 0.23.0 | \_\_[_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0230-2019-04-08)\_\_ |
| [Blueprints API \( Core \)](https://www.npmjs.com/package/tv-automation-sofie-blueprints-integration) | 0.16.0 |  |
| [Blueprints API \( TSR \)](https://www.npmjs.com/package/timeline-state-resolver-types) | 2.0.1 |  |
| [Playout Gateway](https://github.com/nrkno/tv-automation-playout-gateway) | 0.18.0 |  |
| [Mos Gateway](https://github.com/nrkno/tv-automation-mos-gateway) | 0.5.3 |  |
| [Media Manager](https://github.com/nrkno/tv-automation-media-management) | 0.1.8 |  |
| [CasparCG Launcher](https://github.com/nrkno/tv-automation-casparcg-launcher) | [0.6.1](https://github.com/nrkno/tv-automation-casparcg-launcher/releases/tag/v0.6.1) |  |

## Release 7

Release date: 2019-03-15

### Components

| Component | Version | Changelog |
| :--- | :--- | :--- |
| [Core](https://github.com/nrkno/tv-automation-server-core) | 0.22.0 | \_\_[_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0220-2019-03-15)\_\_ |
| [Blueprints API \( Core \)](https://www.npmjs.com/package/tv-automation-sofie-blueprints-integration) | 0.13.0 |  |
| [Blueprints API \( TSR \)](https://www.npmjs.com/package/timeline-state-resolver-types) | 1.6.3 |  |
| [Playout Gateway](https://github.com/nrkno/tv-automation-playout-gateway) | 0.17.0 |  |
| [Mos Gateway](https://github.com/nrkno/tv-automation-mos-gateway) | 0.5.2 |  |
| [Media Manager](https://github.com/nrkno/tv-automation-media-management) | [r7rc1](https://github.com/nrkno/tv-automation-media-management/releases/tag/r7rc1) |  |
| [CasparCG Launcher](https://github.com/nrkno/tv-automation-casparcg-launcher) | [0.6.0](https://github.com/nrkno/tv-automation-casparcg-launcher/releases/tag/v0.6.0) |  |
| [CasparCG](https://github.com/nrkno/tv-automation-casparcg-server) | [2.1.6\_NRK](https://github.com/nrkno/tv-automation-casparcg-server/releases/tag/v2.1.6_NRK) |  |

## Release 6

_---This release was discarded due to stability issues and replaced by Release 7---_

See [Core changelog](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0210-0-2019-02-05) for details

Core version: 0.21.0

## Release 5

Release date: 2019-02-05

See [Core changelog](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0200-2019-02-05) for details

Core version: 0.20.0

## Release 4

Release date: 2018-12-17

See [Core changelog](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0181-2018-12-11) for details

Core version: ~~0.18.1~~ patched by 0.19.0

## Release 3

Release date: 2018-11-15

See [Core changelog](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0160-2018-10-26) for details

Core version: 0.17.0

## Release 2

Release date: 2018-10-26

See [Core changelog](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0150-2018-10-16) for details

Core version: 0.16.0

## Release 1

Release date: 2018-09-07

See [Core changelog](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0110-2018-09-07) for details

Core version: 0.11.0

