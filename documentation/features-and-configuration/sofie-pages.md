# Additional Sofie views

For the purpose of running the system in a studio environment, there are some views that can be used for various purposes:

### Prompter

`/prompter/:studioId`

![](../../.gitbook/assets/image%20%287%29%20%281%29%20%281%29.png)

A fullscreen page which displays the prompter text for the currently active rundown. The prompter can be controlled and configured in various ways, see more at the [Prompter](prompter.md) documentation.

### Presenter screen

`/countdowns/:studioId/presenter`

![](../../.gitbook/assets/image%20%2813%29.png)

A full-screen page, intended to be shown to the studio presenter. It displays countdown timers for the current and next items in the rundown.

### Active Rundown

`/activeRundown/:studioId`

![](../../.gitbook/assets/image%20%2811%29.png)

A page which automatically displays the currently active rundown. Can be useful for the producer to have on a secondary screen.

### Active Rundown - Shelf

`/activeRundown/:studioId/shelf`

![](../../.gitbook/assets/image%20%289%29.png)

A page which automatically displays the currently active rundown, and shows the Shelf in full screen. Can be useful for the producer to have on a secondary screen.

A shelf layout can be selected by modifying the query string, see [Shelf layout](rundown-view.md#shelf-layouts).

### Specific rundown - shelf

`/rundown/:rundownId/shelf`

Displays the shelf in fullscreen for a rundown



