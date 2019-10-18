---
description: >-
  A release is made up from a collection of components and their versions that
  together make up the Sofie system.
---

# Releases

| Release | Status |
| :--- | :--- |
| [Release 15](releases.md#in-planning-release-15) | _In Planning_ |
| [Release 14](releases.md#in-planning-release-14) | _In development_ |
| [Release 13](releases.md#in-development-release-13) | _Released 2019-10-17 **Current stable version**_ |
| [Release 12](releases.md#release-12) | _Released 2019-09-11_ |
| [Release 11](releases.md#release-11-in-development) | _Released 2019-08-19_  |
| [Release 10](releases.md#release-10) | Released 2019-07-05 |
| [Release 9](releases.md#release-9) | Released 2019-05-16  |
| [Release 8](releases.md#release-8) | Released 2019-04-08 |
| [Release 7](releases.md#release-7) | Released 2019-03-15 |

## _In planning: Release 15_

See the [tracking issue on github](https://github.com/nrkno/Sofie-TV-automation/issues/10) for details 

## _In development: Release 14_

See the [tracking issue on github](https://github.com/nrkno/Sofie-TV-automation/issues/8) for details 

## _Release 13_

Release date: 2019-10-17

### Main Features

This release features several bug fixes and a few features:

* Support for remote system messages management
* Preview of HTML-graphics in the hover-scrub in GUI

See the [tracking issue on github](https://github.com/nrkno/Sofie-TV-automation/issues/6) for details 

### Components

| Component | Version | Changelog |
| :--- | :--- | :--- |
| [Core](https://github.com/nrkno/tv-automation-server-core) | 1.1.0 | \_\_[_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md)\_\_ |
| [Blueprints API \( Core \)](https://www.npmjs.com/package/tv-automation-sofie-blueprints-integration) | 1.1.0 |  |
| [Blueprints API \( TSR \)](https://www.npmjs.com/package/timeline-state-resolver-types) | 3.12.0 |  |
| [Playout Gateway](https://github.com/nrkno/tv-automation-playout-gateway) | 1.1.0 |  |
| [Mos Gateway](https://github.com/nrkno/tv-automation-mos-gateway) | 1.0.0 |  |
| [Media Manager](https://github.com/nrkno/tv-automation-media-management) | 1.0.0 |  |

## _Release 12_

Release date: 2019-09-11

### Main Features

This release features many bug fixes and support for a few new playout devoces:

* Playout-gateway: Support for the Quantel video server, via the [Quantel Gateway](https://github.com/nrkno/tv-automation-quantel-gateway)
* Playout-gateway: Support for the [Sisyfos audio controller](https://github.com/olzzon/sisyfos-audio-controller)
* Playout-gateway: Generic TCP-controlled device
* Playout-gateway: Hyperdeck monitoring disk usage, and be able to format slots
* Core: Support for shotbox-like buttons in the shelf
* ..and fixes for many, many bugs introduced in R10 and R11.



See the [tracking issue on github](https://github.com/nrkno/Sofie-TV-automation/issues/5) for details

### Components

| Component | Version | Changelog |
| :--- | :--- | :--- |
| [Core](https://github.com/nrkno/tv-automation-server-core) | 1.0.0 | \_\_[_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#100-2019-09-11)\_\_ |
| [Blueprints API \( Core \)](https://www.npmjs.com/package/tv-automation-sofie-blueprints-integration) | 0.24.0 |  |
| [Blueprints API \( TSR \)](https://www.npmjs.com/package/timeline-state-resolver-types) | 3.8.3 |  |
| [Playout Gateway](https://github.com/nrkno/tv-automation-playout-gateway) | 1.0.0 |  |
| [Mos Gateway](https://github.com/nrkno/tv-automation-mos-gateway) | 1.0.0 |  |
| [Media Manager](https://github.com/nrkno/tv-automation-media-management) | 1.0.0 |  |

## 

## _Release 11_

Release date: _2019-08-19_

### Main Features

This release is a maintenance release, with only minor features.

* Core: Blueprint.onGenerateTimeline improvements
* Core: REST API, a first version, allowing basic control of playout
* Playout-gateway: CommandError callback: report to Core when a command fails



See the [tracking issue on github](https://github.com/nrkno/Sofie-TV-automation/issues/4) for details

### Components

| Component | Version | Changelog |
| :--- | :--- | :--- |
| [Core](https://github.com/nrkno/tv-automation-server-core) | 0.26.0 | \_\_[_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0260-2019-08-19)\_\_ |
| [Blueprints API \( Core \)](https://www.npmjs.com/package/tv-automation-sofie-blueprints-integration) | 0.24.1 |  |
| [Blueprints API \( TSR \)](https://www.npmjs.com/package/timeline-state-resolver-types) | 3.1.1 |  |
| [Playout Gateway](https://github.com/nrkno/tv-automation-playout-gateway) | 0.21.0 |  |
| [Mos Gateway](https://github.com/nrkno/tv-automation-mos-gateway) | 0.8.0 |  |
| [Media Manager](https://github.com/nrkno/tv-automation-media-management) | 0.2.1 |  |

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

* **New ingest data pipeline** _\*\*This is a step on the way to support different types of sources of input data._
* **New Timeline**  _This release also features the new_ [_Timeline_ ](https://www.npmjs.com/package/superfly-timeline)_\(version 7.0\), which gives better control and performance_
* **Unit tests & CI** _In order to achieve a safer development environment, higher code quality and catching bugs earlier, we've added Jest as test framework._

See the [tracking issue on github](https://github.com/nrkno/Sofie-TV-automation/issues/3) for details

### Components

| Component | Version | Changelog |
| :--- | :--- | :--- |
| [Core](https://github.com/nrkno/tv-automation-server-core) | 0.25.0 | [_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0250-2019-07-05) |
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
| [Core](https://github.com/nrkno/tv-automation-server-core) | 0.24.0 | [_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0240-2019-05-16) |
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
| [Core](https://github.com/nrkno/tv-automation-server-core) | 0.23.0 | [_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0230-2019-04-08) |
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
| [Core](https://github.com/nrkno/tv-automation-server-core) | 0.22.0 | [_Changelog_](https://github.com/nrkno/tv-automation-server-core/blob/master/meteor/CHANGELOG.md#0220-2019-03-15) |
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

