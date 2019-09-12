# Getting Started

## Getting Started

{% hint style="info" %}
Sofie can be installed in many different ways, depending on which platforms, needs and features is desired.

For a quick getting-started setup, we recommend that you begin by [installing Sofie with Google Spreadsheet support](installation/installing-sofie-with-google-spreadsheet-support.md).
{% endhint %}

After having installed the Sofie Server Core, navigate to [`http://localhost:3000`](http://127.0.0.1:3000)

Welcome to Sofie! The first page is the Rundown List, you can get back to it at any time by clicking "Rundowns" on the top navigation bar.

![The front page - Rundown List](../.gitbook/assets/image%20%284%29.png)

{% hint style="info" %}
You might not see the "Settings" link at the top right yet, this is because you haven't set the configure access level to this browser. You can do this simply navigating to [http://localhost:3000?configure=1](http://localhost:3000?configure=1)
{% endhint %}

#### Migrations

The first thing to do after installation \(or after an upgrade\) is to run the _Migrations_, in order to set up the system and database correctly. You can find the migrations under _Settings._

Fill in the relevant fields in the migrations form. All might not required, but will help you to customize your Sofie setup. For example, if you want status messages to be sent to your Slack, enter your slack webhook URL in the appropriate field.

After filling out the form, click "Run Migration Procedure". If you have left fields blank, you may see "Warnings During Migration" at the bottom of the migration page. Click "Force Migration" to continue.

#### Gateways

Sofie Core doesn't play anything out by itself, instead it relies on the _Gateways;_ separate applications that connects to it and do the dirty-work.

It surely will need a [**Playout gateway**](https://github.com/nrkno/tv-automation-playout-gateway) \( [installation instructions](installation/installing-a-gateway.md)\), and some others too.

{% hint style="info" %}
Your exact setup and which Gateways to install depends on the features you want to have.

If you'd like to try out the system and just want something simple, we recommend going for using [Sofie with Spreadsheet support](installation/installing-sofie-with-google-spreadsheet-support.md)
{% endhint %}

#### Blueprints

Blueprints can best be described as plugins to Sofie. They interpret the data coming in from the rundowns and transform them into a rich set of playable elements \(Segments, Parts, AdLibs etc\).

To upload Blueprints, go to the Settings page.

There are 3 types of Blueprints, and all 3 must be uploaded into Sofie before the system works.

* **System Blueprints** Handle things on the _System level_
* **Studio Blueprints** Handle things on the _Studio level_, like "which showstyle to use for this rundown"
* **Showstyle Blueprints** Handle things on the _Showstyle level_, like generating _Segments_, _Parts_ and _Timelines_ in a rundown.

The blueprints consists of separate, webpacked js-files which is uploaded into Sofie via the GUI.

* The System Blueprint is uploaded and assigned to the system.
* The Studio Blueprint is uploaded and assigned to a studio.
* The Showstyle Blueprint is uploaded and assigned to a Showstyle.

## Further reading

{% page-ref page="under-the-hood/libraries.md" %}

{% page-ref page="under-the-hood/concepts-and-architecture.md" %}

{% page-ref page="under-the-hood/dictionary.md" %}





