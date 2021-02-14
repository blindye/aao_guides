## AAO Guide for WorkingTitle CJ4

I have AAO template available for Honeycomb Bravo. You can also assign buttons manually.



## Setting up the sim

First we need to unbind and bind some buttons inside the simulator. Check the tips below how to get rid of the altitude/heading increment bug.

I'm using Honeycomb Bravo as an example but if you are using different peripheral try to figure out correct buttons.

- First unbind HDG, NAV, APR, REV, ALT, VS, IAS and left rotary knob.

- Right rotary knob should be assigned as PLUS for right and MINUS for left.

- Bind Autopilot button to TOGGLE AUTOPILOT MASTER




## Using Template

Download template [here](https://raw.githubusercontent.com/blindye/aao_guides/main/wt_cj4/WorkingTitle_CJ4.tmpl). (Right click -> Save As)

- Launch MSFS 2020 and select CJ4 as aircraft and load up in your favorite airport (select runway so all systems are on).

- Launch Axis and Oh's, make sure it recognizes the aircraft, Cessna CJ4 Citation Asobo should be visible on top of the window.

- Click green circle next to Tools menu, it should disconnect Axis and Oh's from the sim (Connect to simulator visible)

- Go to Scripting -> Read HVARs from Sim, wait until it's done.

- Click green circle again to connect to sim.

- Go to Scripting -> Read LVARs from Sim, wait until it's done.

- Go to Templates -> Import template and find the WorkingTitle_CJ4.tmpl file you downloaded.

- Assign correct buttons for variables.  <code>&ast;</code>_BUG_SELECT are meant for left rotary knob, WT_CJ4_<code>&ast;</code>_PRESSED are for AP buttons.


If buttons are not working in simulator, try to restart Axis and Oh's.



## Assigning buttons manually

You can assign buttons manually by clicking + sign under Assigned buttons. 

For Key Down Event check the table below for correct button and event. You can write part of the event in input box and click Apply filter, then finding correct event is easier.

Then in Assigned button/key press correct button in HC Bravo and it should recognize it.

| Button                 | Key down event      |
| ---------------------- | ------------------- |
| ALT (left rotary knob) | ALTITUDE_BUG_SELECT |
| VS (left rotary knob)  | VSI_BUG_SELECT      |
| HDG (left rotary knob) | HEADING_BUG_SELECT  |
| IAS (left rotary knob) | AIRSPEED_BUG_SELECT |
| HDG (AP Panel)         | WT_CJ4_HDG_PRESSED  |
| NAV (AP Panel)         | WT_CJ4_NAV_PRESSED  |
| REV (AP Panel)         | WT_CJ4_VNAV_PRESSED |
| ALT (AP Panel)         | AP_ALT_HOLD         |
| VS (AP Panel)          | WT_CJ4_VS_PRESSED   |
| IAS (AP Panel)         | WT_CJ4_FLC_PRESSED  |



## Tips

MSFS 2020 currently has a bug if some button is assigned inside sim which is pressed on always. Heading and altitude selecting won't work properly when this bug occurs. Heading will go in 10 increments (instead of 1) and altitude in 1000 increments (instead of 100) . In Honeycomb Bravo these are like Gear handle and all on/off switches. To prevent this bug you have to unbind all buttons that are active all time. These buttons will be highlighted as white in Controls settings. 

Most of these can be assigned through AAO.

For example gear handle can be assigned as Key down event: GEAR_UP and GEAR_DOWN.



## Known issues

- In LNAV mode when turning heading knob plane will turn little bit but should come back to correct track

