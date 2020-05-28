# Installing Blueprints

#### Prerequisites

* [Installed and running Sofie Core](installing-sofie-server-core.md)
* [Initial Sofie Core Setup](initial-sofie-core-setup.md)

Blueprints are little plug-in programs that runs inside _Sofie_. They are the logic that determines how _Sofie_ interacts with rundowns, hardware, and media.

Blueprints are custom scripts that you create yourself \(or download an existing one\). There are a set of example Blueprints for the Spreadsheet Gateway available for use here: [https://github.com/SuperFlyTV/sofie-blueprints-spreadsheet](https://github.com/SuperFlyTV/sofie-blueprints-spreadsheet).

To begin installing any Blueprint, navigate to the _Settings page_. Getting there is covered in the [Sofie Access Levels](../getting-started/sofie-navigation.md) page.

![The Settings Page](../../.gitbook/assets/settings-page.jpg)

To upload a new blueprint, click the _+_ icon next to Blueprints menu option. Select the newly created Blueprint and upload the local blueprint JS file. You will get a confirmation if the installation was successful.

There are 3 types of blueprints: System, Studio and Show Style:

### System Blueprint

_System Blueprints handles some basic functionality on how the Sofie system will operate._

After you've uploaded the your system-blueprint js-file, click _Assign_ in the blueprint-page to assign it as system-blueprint.

### Studio Blueprint

_Studio Blueprints determine how Sofie will interact with the hardware in your studio._

After you've uploaded the your studio-blueprint js-file, navigate to a Studio in the settings and assign the new Blueprint to it \(under the label _Blueprint_ \).

After having installed the Blueprint, the Studio's baseline will need to be reloaded. On the Studio page, click the button _Reload Baseline_. This will also be needed whenever you have changed any settings.

### Show Style Blueprint

_Show Style Blueprints determine how your show will look / feel._

After you've uploaded the your show-style-blueprint js-file, navigate to a Show Style in the settings and assign the new Blueprint to it \(under the label _Blueprint_ \).

### Further Reading

* [Blueprints Supporting the Spreadsheet Gateway](https://github.com/SuperFlyTV/sofie-blueprints-spreadsheet)

