# Customizing the Rundown View

## 

## Shelf layouts

The Rundown view and the Detached Shelf view UI can have multiple concurrent layouts for any given Show Style. The automatic selection mechanism works as follows:

1. select the first layout of the `RUNDOWN_LAYOUT` type,
2. select the first layout of any type,
3. use the default layout \(no additional filters\), in the style of `RUNDOWN_LAYOUT`.

To use a specific layout in these views, you can use the `?layout=...` query string, providing either the ID of the layout or a part of the name. This string will then be mached against all available layouts for the Show Style, and the first matching will be selected. For example, for a layout called `Stream Deck layout`, to open the currently active rundown's Detached Shelf use:

`http://localhost:3000/activeRundown/studio0/shelf?layout=Stream`

The Detached Shelf view with a custom `DASHBOARD_LAYOUT` allows displaying the Shelf on an auxiliary touch screen, tablet or a Stream Deck device. A specialized Stream Deck view will be used if the view is opened on a device with hardware characteristics matching a Stream Deck device.

The shelf also contains additional elements, not controlled by the Rundown View Layout. These include Buckets and the Inspector. If needed, these components can be displayed or hidden using additional url arguments:

| Query parameter | Description |
| :--- | :--- |
| Default | Display the rundown layout \(as selected\), all buckets and the inspector |
| `?display=layout,buckets,inspector` | A comma-separated list of features to be displayed in the shelf |
| `?buckets=0,1,...` | A comma-separated list of buckets to be displayed |

* `display`: Available values are: `layout` \(for displaying the Rundown Layout\), `buckets` \(for displaying the Buckets\) and `inspector` \(for displaying the Inspector\).
* `buckets`: The buckets can be specified as base-0 indices of the buckets as seen by the user. This means that `?buckets=1` will display the second bucket as seen by the user when not filtering the buckets. This allows the user to decide which bucket is displayed on a secondary attached screen simply by reordering the buckets on their main view.

_Note: the Inspector is limited in scope to a particular browser window/screen, so do not expect the contents of the inspector to sync across multiple screens._

