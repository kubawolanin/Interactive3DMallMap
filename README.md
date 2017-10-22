# openHAB Floorplan

This project is work in progress.

## Prerequisites

### Your floorplan screenshot

You need a floorplan image (png, jpg, gif) to be used as a temporary background of the SVG file.

### SVG floorplan

Use a online SVG editor to create your floorplan in SVG format. [vectorpaint](http://vectorpaint.yaks.co.nz/) is ideal for the job, as it's free and accessible from the web.
I've also written a nice converter for it so it cleans it up for you.


### openHAB Items preparation

In order to make the floorplan work for you dynamically, you need
to have a group item for each specific room.

```xtend
Group Kitchen  "My fancy kitchen" <kitchen> (Flat)
    Contact  Kitchen_Window     "Window" (Kitchen, Windows)
    Dimmer   Kitchen_Light      "Light" (Kitchen, Lights)
    Switch   Kitchen_Dishwasher "Dishwasher"             <dishwasher>  (Kitchen, Sensors)
    Number   Kitchen_Temp       "Temperature" <temperature> (Kitchen, Thermometers)
    Switch   Kitchen_Motion     "Motion"                    (Kitchen, Motion)
```

Then each of your square should be named *exactly the same*
like the groups you've created.

## Credits

The Map UI is based on tremendous work of [Codrops](http://www.codrops.com) team - 
An interactive 3D mall map concept with a sidebar search and pin indicators for every level.
[Article on Codrops](http://tympanus.net/codrops/?p=26692)

- [List.js](http://www.listjs.com/), the library that adds search, sort, filters and flexibility to plain HTML lists, tables, or anything
- [Font Awesome](https://fortawesome.github.io/Font-Awesome/) created by [Dave Gandy](https://twitter.com/davegandy). License: [Font Awesome license information](http://fontawesome.io/license).
- Other icons from [Flaticon](http://www.flaticon.com/) and [Freepik](http://www.freepik.com/).
- SVG icon system generated with [IcoMoon](https://icomoon.io/app)

