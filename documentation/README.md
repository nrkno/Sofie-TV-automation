# Sofie Documentation

## Key Features

### Web-based GUI

![Producer&apos;s / Director&apos;s  View](https://raw.githubusercontent.com/nrkno/Sofie-TV-automation/master/images/Sofie_GUI_example.jpg)

![Warnings and notifications are displayed to the user in the GUI](../.gitbook/assets/image%20%283%29.png)

![The Host view, displaying time information and countdowns](../.gitbook/assets/image%20%285%29.png)

![The prompter view](../.gitbook/assets/image%20%282%29.png)

{% hint style="info" %}
Tip: The different web views \(such as the host view and the prompter\) can easily be transmitted over an SDI signal using the HTML producer in [CasparCG](installation/installing-connections-and-additional-hardware/casparcg-server-installation.md).
{% endhint %}

### Modular Device Control

Sofie controls play-out devices \(such as vision and audio mixers, graphics and video playback\) via the Playout Gateway, using the [timeline](under-the-hood/dictionary.md#timeline).  
The Playout Gateway controls the devices and keeps track of their state and statuses, and lets the user know via the GUI if something's wrong that can affect the show.

### _State-based Play-out_

Sofie is using a state-based architecture to control play-out. This means that each element in the show can be programmed independently - there's no need to take into account what has happened previously in the show; Sofie will make sure that the video is loaded and that the audio fader is tuned to the correct position, no matter what was played out previously.  
This allows the producer to skip ahead or move backwards in a show, without the fear of things going wrong on air.

### Modular Data Ingest

Sofie features a modular ingest data-flow, allowing multiple types of input data to base rundowns on. Currently there is support for [MOS-based](http://mosprotocol.com) systems, iNews, and [Google Spreadsheets](installation/installing-a-gateway/rundown-or-newsroom-system-connection/installing-sofie-with-google-spreadsheet-support.md), and more is in development.

### Blueprints

The [Blueprints ](under-the-hood/concepts-and-architecture.md#blueprints)are plugins to Sofie, which allows for customization and tailor-made show designs.  
The blueprints are made different depending on how the input data \(rundowns\) look like, how the show-design look like, and what devices to control.

## Documentation

{% page-ref page="getting-started/" %}

{% page-ref page="faq.md" %}

{% page-ref page="releases.md" %}

{% page-ref page="installation/" %}

{% page-ref page="under-the-hood/" %}

