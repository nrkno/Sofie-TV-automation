# Sofie Documentation

{% hint style="info" %}
Please note that this documentation is being actively developed during Q3 2019, the content and links are likely to undergo drastic changes from day to day.
{% endhint %}

## Contents

{% page-ref page="getting-started.md" %}

{% page-ref page="faq.md" %}

{% page-ref page="releases.md" %}

{% page-ref page="installation/" %}

{% page-ref page="under-the-hood/" %}

## Key features

### Web based GUI

![Producer&apos;s view](https://raw.githubusercontent.com/nrkno/Sofie-TV-automation/master/images/Sofie_GUI_example.jpg)

_TODO: add examples of the GUI here:_

* _Producer's view_
* _Details in the GUI_
  * _Next and Current line as gif / webm_
  * _hover-scrub as animated gif / webm_
  * _media-details, such as end-of-file and freeze-frames_
  * _Warnings from blueprints_
  * \_\_
* _Prompter_
* _Host-view_

![Warnings and notes are displayed to the user in the GUI](../.gitbook/assets/image%20%283%29.png)

![The Host view, displaying time information and countdowns](../.gitbook/assets/image%20%285%29.png)

![The prompter view](../.gitbook/assets/image%20%282%29.png)

{% hint style="info" %}
The different web-views \(such as the host-view and the prompter\) can easily be transmitted over an SDI-signal using html-producer in [CasparCG](installation/casparcg-server-installation.md)
{% endhint %}

### Modular device control

Sofie controls play-out devices \(such as vision and audio mixers, graphics and video playback\) via the Playout Gateway.   
Playout Gateway controls the devices and keeps track of their state and statuses, and lets the user know via the GUI if something's wrong that can affect the show.

### _State-based play-out_

Sofie is using a state-based architecture to control play-out. This means that each element in the show can be programmed independently - there's no need to take into account what has happened previously in the show; Sofie will make sure that the video is loaded, that the audio fader is tuned into the correct position, no matter what was loaded previously.  
This allows the producer to skip ahead or move backwards in a show, without any fear of things going wrong on air.

### Modular data ingest

Sofie sports a modular ingest data-flow, allowing multiple types of input data to be used to base rundowns on. Currently there is support for [MOS-based](http://mosprotocol.com) systems and Google Spreadsheets, but more are in development.

### Blueprints

The Blueprints are plugins to Sofie, which allows for customization and tailor-made show designs.  
The blueprints are made different depending on how the input data \(rundowns\) look like, how the show-design look like, and what devices to control.

## System Overview and the Current Integrations

_TODO: make new overview_

## ![Sofie System Overview](https://raw.githubusercontent.com/nrkno/Sofie-TV-automation/master/images/Sofie_NRK_May_10_2019.png)

