## AAO Guide for FlyByWire A320neo

Here you can find how to set up AAO with [FlyByWire's A320neo](https://flybywiresim.com/)

Instructions are for Honeycomb Bravo only. If you want to use some other peripheral you probably need to edit the scripts.



## Setting up the sim

First we need to unbind and bind some buttons inside the simulator. Check the tips below how to get rid of the altitude/heading increment bug.

- Unbind left and right rotary knobs
- Unbind all AP buttons (HDG, NAV, APR, REV, ALT, VS, IAS)
- Bind Autopilot button to TOGGLE AUTOPILOT MASTER



## Setting up the AAO

- Download scripts for AAO [here](https://raw.githubusercontent.com/blindye/aao_guides/main/fbw_a32nx/FBW_A32nx_scripts.xml). (Right click -> Save as.)
- Import scripts to AAO by clicking Scripting menu and choose Import Scripts. Find the FBW_A32nx_scripts.xml. Select all FBW_A32nx scripts and click Import.



## Using Template

- Download template [here](https://raw.githubusercontent.com/blindye/aao_guides/main/fbw_a32nx/FBW_A32nx.tmpl). (Right click -> Save as.)
- Launch MSFS 2020 and select Airbus A320neo as aircraft and load up in your favorite airport (select runway so all systems are on).
- Launch Axis and Oh's, make sure it recognizes the aircraft, Airbus A320 Neo Asobo should be visible on top of the window.
- Click green circle next to Tools menu, it should disconnect Axis and Oh's from the sim (Connect to simulator visible)

- Go to Scripting -> Read HVARs from Sim, wait until it's done.

- Click green circle again to connect to sim.

- Go to Scripting -> Read LVARs from Sim, wait until it's done.

- Go to Templates -> Import template and find the FBW_A32nx.tmpl file you downloaded.
- Assign correct buttons for scripts.  FBW_A32nx-<code>&ast;</code>-mode scripts is for AP mode selector buttons, FBW_A32nx-left_rotary_<code>&ast;</code> scripts are for left rotary knob, FBW_A32nx_right_rotary_dec is assigned to minus for right rotary, FBW_A32nx_right_rotary_inc is assigned to plus.
- If buttons are not working in simulator, try to restart Axis and Oh's.



## Assigning buttons manually

You can assign buttons manually by clicking + sign under Assigned buttons. 

For Key Down Event check the table below for correct button and script.

Then in Assigned button/key press correct button in HC Bravo and it should recognize it.

| Button/knob              | Script                     | Honeycomb Bravo Button ID |
| ------------------------ | -------------------------- | ------------------------- |
| ALT (left rotary knob)   | FBW_A32nx-left_rotary_alt  | 20                        |
| VS (left rotary knob)    | FBW_A32nx-left_rotary_vs   | 19                        |
| HDG (left rotary knob)   | FBW_A32nx-left_rotary_hdg  | 18                        |
| CRS (left rotary knob)   | FBW_A32nx-left_rotary_crs  | 17                        |
| IAS (left rotary knob)   | FBW_A32nx-left_rotary_IAS  | 16                        |
| HDG (AP button)          | FBW_A32nx-hdg_mode         | 0                         |
| NAV (AP button)          | FBW_A32nx-loc_btn          | 1                         |
| APR (AP button)          | FBW_A32nx-appr_btn         | 2                         |
| REV (AP button)          | Unassigned                 |                           |
| ALT (AP button)          | FBW_A32nx-alt_mode         | 4                         |
| VS (AP button)           | FBW_A32nx-vs_mode          | 5                         |
| IAS (AP button)          | FBW_A32nx-spd_mode         | 6                         |
| DECR (right rotary knob) | FBW_A32nx-right_rotary_dec | 13                        |
| INCR (right rotary knob) | FBW_A32nx-right_rotary_inc | 12                        |



## Tips

- NAV button is assigned as LOC capture

- VS button logic is that when pressed first time it will go to LVL OFF mode, second time it will go to VS mode and you can increase/decrease it with right knob (left knob has to be in VS position), and when pressed third time it will disable VS mode.
- Altitude increment (100 or 1000) can be changed under the ALT knob (ingame).

- MSFS 2020 currently has a bug if some button is assigned inside sim which is pressed on always. Heading and altitude selecting won't work properly when this bug occurs. Heading will go in 10 increments (instead of 1) and altitude in 1000 increments (instead of 100) . In Honeycomb Bravo these are like Gear handle and all on/off switches. To prevent this bug you have to unbind all buttons that are active all time. These buttons will be highlighted as white in Controls settings. Most of these can be assigned through AAO. For example gear handle can be assigned as Key down event: GEAR_UP and GEAR_DOWN.



## Known issues

- When turning knobs via HC Bravo, animation and sound doesn't work for ingame knobs.