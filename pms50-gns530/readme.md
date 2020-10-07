# Documentation for the GNS530 MOD Package

This package corrects some bugs of the built-in GNS530 GPS.


First release features:

- Better logic for approach loading and activation
- Correcting the crazy U-turn bug
- Activate leg now works on approach waypoints
- Better DirectTo management and possibility to Direct to an approach icao waypoint
- Bug correction when direct to an airport: it was then impossible to select an approach
- Remove approach is now working
- Activate approach is not selectable if not relevant (ex already activated or no approach)
- Display screen more readable
- Airport list: Correcting flicking bug and enhancing the view
- Adding a declutter level

Installation: unzip the file in your Community directory.

## Approach loading and activation
The original logic for the loading and activating an approach has been changed. This is how it works now:

Loading

If you choose an approach and just loading it, it's added to the fly plan but not activated. It's then up to the pilot to activate it or not (activate approach in procs menu).

Activating

If you activate the approach before the last enroute waypoint, the autopilot continue to follow the route and automaticatically activate the approach after the last enroute waypoint. If you want to bypass the next enroute waypoint, do a direct to the first waypoint approach and then activate the approach.

If you activate the approach after the last enroute waypoint, the autopilot goes directly to the first approach waypoint (without U-turn!!!).

Note: If you set a Direct To, this automatically de-activate the approach.

Note: If you preset an approach from the FS2020 map, this one will be automatically activated.

## U-turn bug
This FS2020 bug probably made many of us crazy. It occurs when you select/activate an approach after the last enroute waypoint. Then the autopilot comes back to the last enroute waypoint before reaching the first approach waypoint.

The workarround to this bug implemented here is to remove all enroute waypoints in this situation. This is not a real problem since you already flew these waypoints.

## Activate leg
Activate leg now works also in approach.

## Direct to
The Direct To know works correctly and you can direct to an approach icao waypoint. These lasts are available without having to manually type them in the DirectTo FPL element list.

A DirectTo automatically de-activate the approach if there is one.

A direct to an airport removes all the waypoints of the fly plan except origin and (new) destination. When doing that it's now possible to select an approach for the new destination (bug correction).

## Remove approach
This fearure was not working in the original fs2020 GNS530. Now it does.

## Graphical enhancements
The display screen is more readable. The fonts weight has been turned to "normal" instead of "bold".

The nearest airport list doesn't flick any more and a separation line has been added between airports for better reading. I don't know if this works like this in the real GNS530 but I took the responsability to do it (sorry for the purists if it's not exactly like in real life).

A third declutter level has been added (declutter works by clicking the CLR button while in map view). I really don't understand how the declutter works in fs2020 but it seems that there are 3 declutter levels depending of the zoom level. Sometimes it works, sometimes not.

Activate approach is not selectable if not relevant (ex already activated or no approach).