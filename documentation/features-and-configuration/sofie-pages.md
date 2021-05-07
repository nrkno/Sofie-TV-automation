# Additional Sofie views

For the purpose of running the system in a studio environment, there are some views that can be used for various purposes:

### Prompter

`/prompter/:studioId`

![](../../.gitbook/assets/zrzut-ekranu-2020-11-17-230954%20%281%29%20%281%29.png)

A fullscreen page which displays the prompter text for the currently active rundown. The prompter can be controlled and configured in various ways, see more at the [Prompter](prompter.md) documentation. If no Rundown is active in a given studio, the [Screensaver](sofie-pages.md#screensaver) will be displayed. 

A full-screen page which displays the prompter text for the currently active rundown. The prompter can be controlled and configured in various ways, see more at the [Prompter](prompter.md) documentation.

### Presenter screen

`/countdowns/:studioId/presenter`

![](../../.gitbook/assets/image%20%2813%29.png)

A full-screen page, intended to be shown to the studio presenter. It displays countdown timers for the current and next items in the rundown. If no Rundown is active in a given studio, the [Screensaver](sofie-pages.md#screensaver) will be shown.

#### Presenter screen overlay

`/countdowns/:studioId/overlay`

![](../../.gitbook/assets/obraz%20%286%29.png)

A full-screen page with transparent background, intended to be shown to the studio presenter as an overlay on top of the produced PGM signal. It displays a reduced amount of the information from the regular [Presenter screen](sofie-pages.md#presenter-screen): the countdown to the end of the current Part, a summary preview \(type and name\) of the next item in the Rundown and the current time of day. If no Rundown is active it will show the name of the Studio.

### Active Rundown

`/activeRundown/:studioId`

![](../../.gitbook/assets/image%20%2811%29.png)

A page which automatically displays the currently active rundown. Can be useful for the producer to have on a secondary screen.

### Active Rundown - Shelf

`/activeRundown/:studioId/shelf`

![](../../.gitbook/assets/image%20%289%29.png)

A page which automatically displays the currently active rundown, and shows the Shelf in full screen. Can be useful for the producer to have on a secondary screen.

A shelf layout can be selected by modifying the query string, see [Shelf layout]().

### Specific rundown - shelf

`/rundown/:rundownId/shelf`

Displays the shelf in fullscreen for a rundown

### Screensaver

When big screen displays \(like Prompter and the Presenter screen\) do not have any meaningful content to show, an animated screensaver showing the current time and the next planned show will be displayed. If no Rundown is upcoming, the Studio name will be displayed.

![A screensaver showing the next scheduled show](../../.gitbook/assets/obraz%20%284%29.png)



