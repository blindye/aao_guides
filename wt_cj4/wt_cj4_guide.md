## AAO Guide for Working Title CJ4

Here you can find AAO template for Honeycomb Bravo. You can also assign buttons manually. Make sure you have [Working Title CJ4](https://github.com/Working-Title-MSFS-Mods/fspackages) installed.

*Please note LORBY-SI - Axis and Oh's is required. It's available in [Simmarket](https://secure.simmarket.com/lorby-si-axis-and-ohs-fsx-p3d-msfs.phtml)*



## Setting up the sim

First we need to unbind and bind some buttons inside the simulator. Check the tips below how to get rid of the altitude/heading increment bug.

I'm using Honeycomb Bravo as an example but if you are using different peripheral try to figure out correct buttons.

- First unbind HDG, NAV, APR, REV, ALT, VS, IAS, left and right rotary knob.

- Bind Autopilot button to TOGGLE AUTOPILOT MASTER



## Setting up the AAO

Download scripts [here](https://github.com/blindye/aao_guides/raw/main/wt_cj4/wt_cj4_scripts.xml) (Right Click -> Save file as.)

- Import scripts to AAO from Scripting -> Import Scripts. Find the downloaded .XML file and import it

- Launch MSFS 2020 and select CJ4 as aircraft and load up in your favorite airport (select runway so all systems are on).

- Launch Axis and Oh's, make sure it recognizes the aircraft, CJ4 should be visible on top of the window.

- Click green circle next to Tools menu, it should disconnect Axis and Oh's from the sim (Connect to simulator visible)

- Go to Scripting -> Read HVARs from Sim, wait until it's done.

- Click green circle again to connect to sim.

- Go to Scripting -> Read LVARs from Sim, wait until it's done.




## Setting assignments

| Left rotary knob | Script                 |
| ---------------- | ---------------------- |
| ALT              | WT_CJ4-left_rotary_alt |
| VS               | WT_CJ4-left_rotary_vs  |
| HDG              | WT_CJ4-left_rotary_hdg |
| CRS              | WT_CJ4-left_rotary_crs |
| IAS              | WT_CJ4-left_rotary_ias |

| Right rotary knob     | Script                  |
| --------------------- | ----------------------- |
| Turn left (decrease)  | WT_CJ4-right_rotary_dec |
| Turn right (increase) | WT_CJ4-right_rotary_dec |

| AP button | Variable               |
| --------- | ---------------------- |
| HDG       | WT_CJ4_AP_HDG_PRESSED  |
| NAV       | WT_CJ4_AP_NAV_PRESSED  |
| APR       | WT_CJ4_AP_APPR_PRESSED |
| REV       | WT_CJ4_AP_VNAV_PRESSED |
| ALT       | AP_ALT_HOLD            |
| VS        | WT_CJ4_AP_VS_PRESSED   |
| IAS       | WT_CJ4_AP_FLC_PRESSED  |



## Video guide

<div align="left">
      <a href="https://www.youtube.com/watch?v=787Uf6bmZ5Q">
         <img src="https://img.youtube.com/vi/787Uf6bmZ5Q/0.jpg" style="width:100%;">
      </a>
</div>



## Tips

MSFS 2020 currently has a bug if some button is assigned inside sim which is pressed on always. Heading and altitude selecting won't work properly when this bug occurs. Heading will go in 10 increments (instead of 1) and altitude in 1000 increments (instead of 100) . In Honeycomb Bravo these are like Gear handle and all on/off switches. To prevent this bug you have to unbind all buttons that are active all time. These buttons will be highlighted as white in Controls settings. 

Most of these can be assigned through AAO.

For example gear handle can be assigned as Key down event: GEAR_UP and GEAR_DOWN.



## Known issues

- Clicking sounds doesn't play

