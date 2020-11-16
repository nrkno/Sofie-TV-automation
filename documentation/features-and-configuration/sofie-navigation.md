# Access Levels

By default, a user cannot edit settings, nor play out anything.

If user accounts are enabled \(`enableUserAccounts` in [Core settings](sofie-core-settings.md#settings-file)\), the access levels are set under the user settings. If no user accounts are set, the access level for a browser is set by adding `?theaccessmode=1` to the URL as described below.

The access level is persisted in browser's Local Storage. To disable, visit`?theaccessmode=0`.

| Access area | Basic Mode | Configuration Mode | Studio Mode | Admin Mode |
| :--- | :--- | :--- | :--- | :--- |
| **Rundowns** | View Only | View Only | Yes, playout | Yes, playout |
| **Settings** | No | Yes | No | Yes |

### Access levels

#### Basic mode

The basic mode allows for view only. No playout or access to any settings.

#### Studio mode

Studio Mode gives the user playout-control of the studio, rundowns etc.

Enables rundown actions such as activating/deactivating rundowns, taking parts, ad-libbing, etc.

This mode is accessed by adding  `?studio=1` to the end of the URL.

#### Configuration mode

Configuration mode gives the user full control over the Settings pages and allows full access to the system including the ability to modify Blueprints, Studios, or Show Styles, creating and restoring Snapshots, as well as modifying attached devices.

This mode is accessed by adding  `?configure=1` to the end of the URL.

#### Help Mode

Enables some tooltips that might be useful to new users.

This mode is accessed by adding  `?help=1` to the end of the URL.

#### Admin Mode

This mode will give the user the same access as the Configuration and Studio modes as well as having access to a set of Test Tools and a Manual Control section on the Rundown page.

This mode is enabled when `?admin=1` is added the end of the URL.

#### Testing Mode

Enables the page Test Tools, which contains various tools useful for testing the system during development.

This mode is enabled when `?testing=1` is added the end of the URL.

#### Developer mode

This mode enables various things that might be useful for a developer, such as re-enabling the right-click menu.

This mode is enabled when `?develop=1` is added the end of the URL.

## Language selection

The UI will automatically detect user browser's default matching and select the best match, falling back to English. You can also force the UI language to any language by navigating to a page with `?lng=xx` query string, for example:

`http://localhost:3000/?lng=en`

This choice is persisted in browser's Local Storage, and the same language will be used until a new forced language is chosen using this method.

