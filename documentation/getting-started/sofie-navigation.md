# Sofie Access Levels

A variety of access levels can be set via the URL. Some of the access levels provide additional administrative pages or helpful tool tips for new users. These modes are persistent between sessions and will need to be manually disabled by replacing the _1_ with a _0_ in the URL. Below is a quick reference to the modes and what they have access to.

| Ability | Basic Mode | Configuration Mode | Studio Mode | Admin Mode |
| :--- | :--- | :--- | :--- | :--- |
| Access Rundown | View Only | No | Yes | Yes |
| Access Studios | View Only | Yes \( Settings Only \) | Yes | Yes |
| Access Settings | No | Yes | No | Yes |

### Standard Access Levels

#### Basic Usage

Without enabling any additional modes in Sofie, the browser will have minimal access to the system. It will be able to view a rundown but, will not have the ability to manipulate it. This includes activating, deactivating, or resetting the rundown as well as taking the next part, ad-lib, etc.

#### Configuration Mode

If the link to the settings page is not visible in the header of your application, add `?configure=1` to the end of the URL. This mode allows full access to the system including the ability to modify Blueprints, Studios, or Show Styles, creating and restoring Snapshots, as well as modifying attached devices.

#### Studio Mode

Studio Mode gives the current browser full control of the studio and all information associated to it. This includes allowing actions like activating and deactivating rundowns, taking parts, ad-libbing, etc. This mode is accessed by adding a `?studio=1` to the end of the URL.

#### Help Mode

If you would like some tool tips to be displayed on the UI for additional assistance, add `?help=1` to the URL.

#### Change Language

The UI will automatically detect the browser's default language and select the best match, falling back to English. To set a specific language add `?lng=XX` to the end of the URL and replace the XX with your language code of choice.

#### Admin Mode

This mode will give the browser the same access as the Configuration and Studio modes as well as having access to a set of Test Tools and a Manual Control section on the Rundown page. This mode is enabled when `?admin=1` is added the end of the URL.

### Developer Access Levels

#### Develop Mode

This mode will enable the browsers default right click menu to appear and can be accessed by adding `?develop=1` to the URL. It will also reveal the Manual Control section on the Rundown page.

#### Testing Mode

A set of testing tools can be found by adding ?testing=1 to the URL and navigating with the new link called Test Tools.

### Additional Modes & More Details

For more information: [https://github.com/nrkno/tv-automation-server-core\#studio-mode](https://github.com/nrkno/tv-automation-server-core#studio-mode)

