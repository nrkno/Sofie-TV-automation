---
description: >-
  This installation allows you to use Sofie in its simplest form. Using Google
  spreadsheets to create rundowns and CasparCG to play videos and graphics, this
  is the quickest way to get started.
---

# Installing Sofie with Google Spreadsheet support

## Installation of Sofie

1. Begin by [installing the Server Core](installing-sofie-server-core.md) ****and start it up.
2. Follow the [Getting started Guide](../getting-started.md) to setup up the basic of the studio and show-styles.
3. Install the [**Spreadsheet gateway**](https://github.com/SuperFlyTV/spreadsheet-gateway) **\(**[instructions](installing-a-gateway.md)\)
4. Install the [**Playout gateway**](https://github.com/nrkno/tv-automation-playout-gateway) \([instructions](installing-a-gateway.md)\)

## Setting up Sofie to support Spreadsheets

{% hint style="info" %}
The Spreadsheet support comes in two halves:  
The **Spreadsheet Gateway;** which reads _spreadsheets_ from Google Drive and inputs them as rundowns into Sofie  
and **Blueprints**; which transforms the rundowns into playable elements.
{% endhint %}

### Blueprints

These [_generic spreadsheet blueprints_](https://github.com/SuperFlyTV/sofie-blueprints-spreadsheet) can handle a generic show and provide basic functionality.  
Begin by buildin these and upload them into Sofie Core.

{% hint style="info" %}
See the README in the blueprints repository for instructions on how to build them, or you can use the pre-built blueprints at [https://github.com/SuperFlyTV/sofie-blueprints-spreadsheet/tree/dist/dist](https://github.com/SuperFlyTV/sofie-blueprints-spreadsheet/tree/dist/dist)
{% endhint %}

There

To upload the blueprints, click the "+" next to "Blueprints" in the settings menu, followed by clicking on the newly created blueprint. Then, click on the "Upload Blueprints" button and select a blueprint to upload.

There are three blueprints for the Spreadsheet Gateway: `system-bundle.js`, `studio0-bundle.js`, and `blueprint0-bundle.js`. Upload each of these in turn and give them a memorable name.

Find the system blueprint in the "Blueprints" list and click the "Assign" button.

Next, navigate to the "Default Showstyle" and set the blueprint to the show style blueprint you just uploaded.

Then navigate to the "Default Studio" and set the blueprint to the studio blueprint you just uploaded.

Finally, click the "Reload Baseline" button.

1. Upload these [_generic spreadsheet blueprints_](https://github.com/SuperFlyTV/sofie-blueprints-spreadsheet) __into Core.
2. **Run migrations again**, the spreadsheet blueprints have now added a few setup steps automatically.

### Spreadsheet Gateway Configuration

After starting the Spreadsheet Gateway, it should appear under "Devices" in the settings menu.

Navigate to this page and enable the Google Drive API for your Google account by clicking on the link provided on the settings page, followed by clicking the "Enable the Drive API" button.

Clicking this button will provide you with several prompts, before presenting you with a button to download your client configuration. Download this file and upload it to Sofie using the "Browse..." button on the Spreadsheet Gateway settings page.

You will then be prompted to click on a link to give Sofie access to your Google Drive. Follow the prompts on the following screens until you reach a screen with a code for you to copy. Copy this into the text field in the Spreadsheet Gateway settings page.

Next, go to your studio settings and click "+" under "Attached Devices". Select the Spreadsheet Gateway.

Go back to the Spreadsheet Gateway settings and enter the name of the folder containing your rundowns in to the "Drive folder name" field.

If the status changes to "Good", you're all set!

### ATEM Mappings

In order for Sofie to control your ATEM, it needs to know how to map inputs and outputs to ATEM ports.

#### Camera Mappings

To create these mappings, open the studio settings page for your studio. Under 'Blueprint Configuration click the '+' button and select 'Camera Mapping' from the menu that appears. By default each numbered camera is mapped one-to-one to ATEM ports, IE, Camera1 is ATEM port 1.

To change this mapping, the following format is used: CAMERA\_NUMBER:ATEM\_PORT

e.g. For Camera3 to be on ATEM port 5, the mapping will be 3:5

#### Remote Mappings

Remote sources can be added through the 'RM Mapping' blueprint setting - following the same format as the camera mappings. Each remote source is mapped to an ATEM input, so Sofie is blind to how your remote source comes into your studio.

#### VTs

To make use of CasparCG for VT playout, you will need to add the 'ATEM Server' mappings.

In the Spreadsheet Gateway blueprints, Server 1 is for VT / full screen graphics.

#### Screen Output

To add output screens \(e.g. a TV in a studio\) you will need to change two settings. First, open your studio settings and check for 'atem\_aux\_screen' under Layer Mappings. If it doesn't exist, you can create it with the following settings:

| Setting | Value |
| :--- | :--- |
| Layer ID | atem\_aux\_screen |
| Device Type | ATEM |
| Device ID | atem0 |
| mappingType | Auxiliary |
| index | 3 |

Changing the value of index with change the AUX output used.

Secondly, open your show style settings and add a new output channel with the 'Internal ID' of 'screen1', any name of your choosing.

## Configuring play-out devices

Depending on what you want to use for playout, you can set up the playout devices a bit differently, but here are some suggestions:

### Video & Graphics

* Use the free and open source application CasparCG. [Installation instructions here](casparcg-server-installation.md).

### Vision mixing

* Use a [Blackmagic ATEM ](https://www.blackmagicdesign.com/products/atem)hardware mixer. Playout Gateway supports em all.
* _\(Support coming soon\)_ Use [VMix ](https://www.vmix.com/)software mixer.

### Audio mixing

* _\(Support coming soon\)_ Use open source [Sisyfos audio controller](https://github.com/olzzon/sisyfos-audio-controller). It provides a nice frontend for a multitude of audio mixers.
* Customize the blueprints to support your own audio device over OSC

### Others

Controlling these devices is possible, but requires blueprint customization.

* Panasonic PTZ cameras
* Light control
* MAM support, transfer files from a MAM or remote file storage.

### 



\_\_

