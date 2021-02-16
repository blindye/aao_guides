## AAO Guide for Working Title CJ4

Here you can find AAO template for Honeycomb Bravo. You can also assign buttons manually. Make sure you have [Working Title CJ4](https://github.com/Working-Title-MSFS-Mods/fspackages) installed.

*Please note LORBY-SI - Axis and Oh's is required. It's available in [Simmarket](https://secure.simmarket.com/lorby-si-axis-and-ohs-fsx-p3d-msfs.phtml)*



## Setting up the sim

First we need to unbind and bind some buttons inside the simulator. Check the tips below how to get rid of the altitude/heading increment bug.

I'm using Honeycomb Bravo as an example but if you are using different peripheral try to figure out correct buttons.

- First unbind HDG, NAV, APR, REV, ALT, VS, IAS, left and right rotary knob.

- Bind Autopilot button to TOGGLE AUTOPILOT MASTER



## Setting up the AAO Scripts

Download scripts [here](https://github.com/blindye/aao_guides/raw/main/wt_cj4/wt_cj4_scripts.xml) 

- Import scripts to AAO from Scripting -> Import Scripts. Find the downloaded .XML file and import it




## Using Template (outdated, do not use)

Will update soon

- Launch MSFS 2020 and select CJ4 as aircraft and load up in your favorite airport (select runway so all systems are on).

- Launch Axis and Oh's, make sure it recognizes the aircraft, Cessna CJ4 Citation Asobo should be visible on top of the window.

- Click green circle next to Tools menu, it should disconnect Axis and Oh's from the sim (Connect to simulator visible)

- Go to Scripting -> Read HVARs from Sim, wait until it's done.

- Click green circle again to connect to sim.

- Go to Scripting -> Read LVARs from Sim, wait until it's done.

- Go to Templates -> Import template and find the WorkingTitle_CJ4.tmpl file you downloaded.

- Assign correct buttons for variables.  <code>&ast;</code>_BUG_SELECT are meant for left rotary knob, WT_CJ4_<code>&ast;</code>_PRESSED are for AP buttons.

If buttons are not working in simulator, try to restart Axis and Oh's.



## Tips

MSFS 2020 currently has a bug if some button is assigned inside sim which is pressed on always. Heading and altitude selecting won't work properly when this bug occurs. Heading will go in 10 increments (instead of 1) and altitude in 1000 increments (instead of 100) . In Honeycomb Bravo these are like Gear handle and all on/off switches. To prevent this bug you have to unbind all buttons that are active all time. These buttons will be highlighted as white in Controls settings. 

Most of these can be assigned through AAO.

For example gear handle can be assigned as Key down event: GEAR_UP and GEAR_DOWN.



## Known issues

- Clicking sounds doesn't play

