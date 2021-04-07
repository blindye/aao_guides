## AAO Guide for FlyByWire A320neo

Here you can find how to set up AAO with [FlyByWire's A320neo](https://flybywiresim.com/)

Instructions are for Honeycomb Bravo only. If you want to use some other peripheral you probably need to edit the scripts.

*Please note LORBY-SI - Axis and Oh's is required. It's available in [Simmarket](https://secure.simmarket.com/lorby-si-axis-and-ohs-fsx-p3d-msfs.phtml)*



## Setting up the sim

First we need to unbind and bind some buttons inside the simulator. Check the tips below how to get rid of the altitude/heading increment bug.

- Unbind left and right rotary knobs
- Unbind all AP buttons (HDG, NAV, APR, REV, ALT, VS, IAS)
- Bind Autopilot button to TOGGLE AUTOPILOT MASTER (only in dev / stable. If you are using FBW experimental version, unbind AP also)



## Setting up the AAO

- Launch MSFS 2020 and select FBW Airbus A320 as aircraft and load up in your favorite airport (select runway so all systems are on).

- Launch Axis and Oh's, make sure it recognizes the aircraft, Airbus A320 should be visible on top of the window.

- Click green circle next to Tools menu, it should disconnect Axis and Oh's from the sim (Connect to simulator visible)

- Go to Scripting -> Read HVARs from Sim, wait until it's done.

- Click green circle again to connect to sim.

- Go to Scripting -> Read LVARs from Sim, wait until it's done.

  

## Using Template (recommended)

**Template is only for Honeycomb Bravo**

*If you have already set up profile for earlier versions, delete assignments from AAO shown in "Setting assignmens"*



Download latest release [here](https://github.com/blindye/aao_guides/releases/)

- Extract the zip file

- Import scripts file (xml) to AAO from Scripts -> Import scripts. Open the xml file from downloaded release zip.
- Import template to AAO from Templates -> Import Template. Open the .tmpl file and open. Click Import.
- After import is finished, go to Templates -> Apply template to this aircraft. Select FBW_A32nx_v2 from the list, click Apply.
- Click Merge. AAO should recognize HC Bravo automatically.
- Disconnect AAO from Sim by clicking green circle in AAO, then connect it again. All should be  working now.

*Check Tips below how to change managed / selected mode*



## Assigning buttons manually

You can assign buttons manually by clicking + sign under Assigned buttons. 

For Key Down Event check the table below for correct button and script. For AP Mode buttons enable Long click with 400ms delay.

Then in Assigned button/key press correct button in HC Bravo and it should recognize it.

| Button/knob              | Script                                                       | HC Bravo Button ID |
| ------------------------ | ------------------------------------------------------------ | ------------------ |
| ALT (left rotary knob)   | FBW_A32nx_v2-left_rotary_alt                                 | 20                 |
| VS (left rotary knob)    | FBW_A32nx_v2-left_rotary_vs                                  | 19                 |
| HDG (left rotary knob)   | FBW_A32nx_v2-left_rotary_hdg                                 | 18                 |
| CRS (left rotary knob)   | FBW_A32nx_v2-left_rotary_crs                                 | 17                 |
| IAS (left rotary knob)   | FBW_A32nx_v2-left_rotary_IAS                                 | 16                 |
| HDG (AP button)          | Long click: FBW_A32nx_v2-hdg_mode_pull / Short click: hdg_mode_push | 0                  |
| NAV (AP button)          | Unassigned                                                   | 1                  |
| APR (AP button)          | Long click: FBW_A32nx_v2-appr_btn / Short click: loc_btn     | 2                  |
| REV (AP button)          | Unassigned                                                   |                    |
| ALT (AP button)          | Long click: FBW_A32nx_v2-alt_mode_pull  / Short click: alt_mode_push | 4                  |
| VS (AP button)           | Long click: FBW_A32nx_v2-vs_mode_pull / Short click: vs_mode_push | 5                  |
| IAS (AP button)          | Long click: FBW_A32nx_v2-spd_mode_pull / Short click: spd_mode_push | 6                  |
| DECR (right rotary knob) | FBW_A32nx_v2-right_rotary_dec                                | 13                 |
| INCR (right rotary knob) | FBW_A32nx_v2-right_rotary_inc                                | 12                 |



## Tips

- **Change managed/selected mode by either short pressing AP mode button or by long clicking. Short press is managed mode and long push is selected mode**. **Approach mode is selected by long clicking APR button, Loc mode is selected by short clicking APR button**

- Altitude increment (100 or 1000) can be changed under the ALT knob (ingame).

- MSFS 2020 currently has a bug if some button is assigned inside sim which is pressed on always. Heading and altitude selecting won't work properly when this bug occurs. Heading will go in 10 increments (instead of 1) and altitude in 1000 increments (instead of 100) . In Honeycomb Bravo these are like Gear handle and all on/off switches. To prevent this bug you have to unbind all buttons that are active all time. These buttons will be highlighted as white in Controls settings. Most of these can be assigned through AAO. For example gear handle can be assigned as Key down event: GEAR_UP and GEAR_DOWN.



## Known issues

- When turning knobs via HC Bravo, animation and sound doesn't work for ingame knobs.