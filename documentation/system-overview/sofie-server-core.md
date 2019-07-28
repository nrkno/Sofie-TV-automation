---
description: The main application of the Sofie system
---

# Sofie Server Core

{% hint style="info" %}
Please note that this documentation is a work in progress, and that the content and links are likely to undergo drastic changes. 
{% endhint %}

### Local Development

First, install Meteor: [Meteor Installation Guide](https://www.meteor.com/install)

Then, clone the repository and install all dependencies:

{% hint style="danger" %}
Make sure your NODE\_ENV is NOT set to production!
{% endhint %}

```text
git clone -b master https://github.com/nrkno/tv-automation-server-core.git
cd tv-automation-server-core/meteor
meteor npm install
meteor
```

If you run into any issues while installing the dependencies, clone any offending packages from Git and link them using `npm link`. For example, for `tv-automation-mos-connection` library:

```text
git clone -b master https://github.com/nrkno/tv-automation-mos-connection.git
cd tv-automation-mos-connection
npm run build
npm link
cd ../tv-automation-server-core/meteor
npm link mos-connection
```

## System Settings

In order for the system to work properly, it may be neccessary to set up several system properties. These can be set through environement variables - if not present, default values will be used.

| Setting | Use | Default value |
| :--- | :--- | :--- |
| `NTP_SERVERS` | Comma separated list of time servers to sync the system to | `0.se.pool.ntp.org` |
| `FRAME_RATE` | Framerate to be used when displaying time with frame accuracy | `25` |

## Additional Views

For the purpose of running the system in a studio environment, there are additional endpoints, unavailable from the menu structure.

| Path | Function |
| :--- | :--- |
| `/countdowns/:studioId/presenter` | Countdown clocks for a given studio, to be shown to the studio presenter |
| `/activeRo/:studioId` | Redirects to the running order currently active in a given studio |
| `/prompter/:studioId` | A simple prompter for the studio presenter |

## Modes

### Studio Mode

In the default mode, the Settings page will be unavailable from main navigation. If you want access to the Settings page on a given client station, append `?configure=1` to any query string.

`http://localhost:3000/?configure=1`

This setting is persisted in browser's Local Storage. To disable studio mode in a given client, append `?studio=0`.

### Configuration Mode

In the default mode, the Settings page will be unavailable from main navigation. If you want access to the Settings page on a given client station, append `?configure=1` to any query string.

`http://localhost:3000/?configure=1`

### Developer Mode

In developer mode, right click is not disabled.

`http://localhost:3000/?develop=1`

## Operating the Prompter Screen

The prompter can be operated using pressing & holding keyboard arrow keys: `Up` & `Down`. Press `Home` to enable auto-scroll mode. `Shift+Up` and `Shift+Down` scrolls in 3x speed. If the studio setup requries a mirrored-image prompter, you can append `?mirror=1` to enable mirror mode. This setting is not persisted in browser.

## Language

### Language Selection

The UI will automatically detect user browser's default matching and select the best match, falling back to english. You can also force the UI language to any language by navigating to a page with `?lng=xx` query string, for example:

`http://localhost:3000/?lng=xx`

This choice is persisted in browser's Local Storage, and the same language will be used until a new forced language is chosen using this method.

### Translating Sofie

For support of various languages in the User Interface, Sofie uses the i18next framework. It uses JSON-based translation files to store UI strings. In order to build a new translation file, first extract a PO template file from Sofie UI source code:

```text
cd meteor
npm run i18n-extract-pot
```

Find the created `template.pot` file in `meteor/i18n` folder. Create a new PO file based on that template using a PO editor of your choice. Save it in the `meteor/i18n` folder using your ISO 639-1 language code of choice as the filename.

Next, modify the `package.json` scripts and create a new language compilations script:

```text
"i18n-compile-json": "npm run i18n-compile-json-nb & npm run i18n-compile-json-sv & npm run i18n-compile-json-xx",
"i18n-compile-json-xx": "i18next-conv -l nb -s i18n/xx.po -t public/locales/xx/translations.json",
```

Then, run the compilation script:

```text
npm run i18n-compile-json
```

The resulting JSON file will be placed in `meteor/public/locales/xx`, where it will be available to the Sofie UI for use and autodetection.

