# Ender3dent
Gonna build a Voron. Build a Trident.

![Ender3dent Buildguide GIF](/Gallery/ender3dent-buildguide.gif "Ender3dent Buildguide GIF")

# What if you took 2 Ender 3's and made something else?

I wanted to take 2 old Ender 3 printers and make a trident (this is based off of the OG Ender 3 not the pro v2, v3, neo s1 plus or whatever Creality is calling it these days). This is basically a Voron trident built with 2040 v-slot extrusions and a bunch of compromises. Proceed at your own risk.

![2plus2ender3dent JPG](/Gallery/2_plus_2_ender3dent.jpg "2plus2ender3dent JPG")
![TwoEnder3dent Render JPG](/Gallery/2_ender3dent.jpg "TwoEnder3dent Render JPG")

## Goals

* Re-use as many parts from 2 Ender 3's to build a Voron Trident
* Rigid all metal frame (no printed frame extensions like the Ender 3 NG)
* Easily enclosable (no top hats or weird panel shapes)
* Use the trident style gantry and Z axis

## Why should you build this?

You probably shouldn't. A new trident frame is cheap, Ender frames are too small and have poor build quality. If you ONLY re-use ender extrusions the frame would be incredibly tiny (see below). This would significantly reduce the build volume compared to a stock ender. To compromise I’ve opted to re-use some of the ender extrusions, but additional extrusions are required for this build. Again, for the amount of time and $$ you could probably just build a spec trident. But if you're stubborn like me and want to re-use parts from your old Ender 3's this is the perfect project for you! *(maybe)

![too_small_try_again JPG](/Gallery/too_small_try_again.jpg "First design is too small JPG")

## ⚠️What do you need to build this? ⚠️

Oh, wait you're still reading? Ok guess you actually want to build this abomination.

You'll need:
* 2x Ender 3 printers (this is based off of the OG Ender 3 not the pro v2, 3, neopro or whatever creality is calling it these days)
* 4x 530mm 2040
* 2x 400mm 2040
* 6x MGN12H Linear Rails (Sizes TBD)
* ⚠️Cut extrusions to length
* ⚠️Drill blind joints
* ⚠️Tap holes

## Inspiration

In my search for an ender 3 corexy conversion, I've seen many different builds and concepts. The ones below have inspired me to make this.

* [u/gnit0](https://www.reddit.com/r/ender3/comments/xr9097/ideas_to_combine_two_ender_3v2s/)
* [PandER-V](https://www.printables.com/model/744568-pander-v-beta)
* [Ender3 NG V1.2](https://www.printables.com/model/922401-ender-3-ng-v12-corexy-conversion)

⚠️ THIS IS A WORK IN PROGRESS, RESULTS NOT GURANTEED, BUILD AT YOUR OWN RISK ⚠️

<details>
  <summary>Old Description</summary>
 
## BOM


1. go to https://vorondesign.com/voron_trident
2. select configurator, make your choices like direct feed, blind joints, 250
3. hit show or download
4. remove parts you already own

### yeah .. but what CAN i reuse?

| Part                    | Can reuse                               |
|-------------------------|-----------------------------------------|
| Creality mainboard      | yes, but need more stepper, see below   |
| Leadscrew               | yes                                     |
| 2nd Leadscrew           | yes                                     |
| Stock leadscrew coupler | yes, better than the "spring" ones      |
| Bed heater              | yes                                     |
| Flexplate               | yes                                     |
| steppers                | yes, but need more                      |
| Power Supply            | yes, even the fat one                   |
| AC Inlet + Switch       | yes, check voron mods                   |
| Cables                  | yes, except toolhead wiring             |
| Display                 | Yes, if its the monochrome              |
| Raspberry               | yes                                     |
| Custom Extruder         | likely yes, check the many Trident mods |
| Custom Hotend           | likely yes, check the many Trident mods |
| Vwheels                 | no                                      |
| Sheetmetal Parts        | no                                      |
| Random screw            | maybe                                   |


### Secondary / Primary MCU
Basically everything with at least 2 stepper driver will work.

Example 1
* Creality: Z, Z1, Z2
* Skr Pico: A, B
* Ebb36   : E

Example 2
* Creality: Z, Z1, Z2, E
* ERB V2.0: A, B

Example 3:
* Manta M5P: Z, Z1, Z2, A, B
* Ebb36: E

Please notice that same motion stepper should share the same mcu.

### The Frame
Make sure to:

* NOT buy V-Slot, as the MGN9 rails don't sit tightly on them.
* NOT buy Slot 5, aka ITEM (they need smaller alignment studs on printed parts and different rolling nuts).
* Pre-drill and pre-tap are expensive and not hard to do on your own.
* Buy Misumi or Bosch B-Type.


### When coming from a Enderwire

You CAN reuse your existing mgn12, however you need new mounts and thicccc weatherstrips for the panels.
Mgn12 mounts, idk maybe there are others/betters

* https://www.thingiverse.com/thing:5124692
* https://www.thingiverse.com/thing:5348910

Untested but you could also use 4040 for the Z vertical extrusions, maybe a 2040 in the front to look nice with fridge door mod.

* https://github.com/tanaes/whopping_Voron_mods/tree/main/clickyclacky_door

While you are at it maybe also replace the extrusions going side way and to the rear with 2040 too for more speeds, just keep the overall dimensions in mind.


### How to build

1. go to https://vorondesign.com/voron_trident
2. click "Manual"
3. follow the manual 1:1 except bed mounting
4. see this for bed mounting, make something yourself or buy a Trident bed


* [bottom](Gallery/PXL_20230406_105018828.jpg)
* [top](Gallery/PXL_20230830_124231232.jpg)


### example price calc

```
Trident selfsource
 115€ 5xmgn9 + 1xmgn12
  65€ siboor leadscrew stepper (3 pieces, 15€ each)
  60€ frame
  30€ skr pico as secondary mcu
  50€ Trident screw kit (cheaper in metric land locally)
  15€ 5M Gates belts
  12€ 2x 10pc f695 (are 20 enough?)
   5€ spherical bearings
=352 €  (no panels tho)

Building an Enderwire with Siboor kit instead of a Trident
€346.44 (requires a Ender3 v2 or pro)

```

## WHY

### General

* inverted electronics
* shorter reverse bowden
* fast preheating print area
* over bed static fans (RSCD)
* quick and easy underbed fan replacements
* print on eye level, reduce back bending/pain
* additional bottom storage when not printing near max Z
    * filament storage
    * plate storage
    * finished plates /parts can slowly cooldown while printing the next
* easier to tune, less belts to tension equally
* static AB motors easy to extend with dampers, fans or replace for longer
* 250 build can have a internal Spoolroller even with 260 bed (see mods)


### vs. Switchwire
* stable xy gantry
* internal spool holder
* no Z dragchain required and still looking neat
* waaaay more mods than SW

## But V2 is style, V2 is love

If you absolutely must, then feel free to apply the principal of stuffing Ender parts into different Frame to the V2 frame.

https://github.com/OneHotTake/EndeVOR-2.4

## frigg 3d printers gimma something real

https://github.com/Futtawuh/EnderCNC

## FAQ

* What can i reuse?
   * everything that is not sheetmetal or vwheels and preferable not the frame
* How to mount the Ender 3 bed?
   * [bottom](Gallery/PXL_20230406_105018828.jpg)
   * [top](Gallery/PXL_20230830_124231232.jpg)

## Mods

* Trident inverted Trident Inverted Electronics
    * https://mods.vorondesign.com/detail/pXkXHVIUbqSWqQKJISczw
* Reusing leadscrew & coupler to not lose Z height
    * https://www.printables.com/model/644553-trident-motor-spacer-standoffs-for-leadscrew-coupl
* Internal Spoolroller
    * https://www.printables.com/model/584995-internal-spoolholder-for-2020-extrusion



## Galery

### How it all started
and why you should invest a minuscula amount of money for new extrusions
![VT.979 the original](/Gallery/vt.979_yell_pls_dont_buy_a_frame_kit_.jpg "VT.979 the original")

### Ender3dent
> Fun fact 1111 & 1112 battled for the 1111 serial
> technically 1112 is Voron Trident #1111 as they start from 0

![VT.1111 Kignis](/Gallery/vt.1111_kignis.jpg "VT.1111 Kignis")
![VT.1112 Yell](/Gallery/vt.1112_yell.jpg "VT.1112 Yell")
![vt.1540 hanarius](/Gallery/vt.1540_hanarius.jpg "VT 1540 hanarius")
![VT.1583 Evidences](/Gallery/vt.1583_evidences.jpg "VT.1583 Evidences")
![VT.1741 ravenkeeper](/Gallery/vt.1759_wallen.jpg "VT.1759 Wallen")
![vt.1816 hanarius](/Gallery/vt.1816_hanarius.jpg "VT 1816 hanarius")


### Ender4dent
![VT.1741 ravenkeeper](/Gallery/vt.1741_ravenkeeper.jpg "VT.1741 ravenkeeper")

### Ender5dent
build it and DM me on discord °~°

### Ender6dent
![VT.1233 Coursin](/Gallery/vt.1233_coursin.jpg "VT.1233 Coursin")


### Other relevant images
Ender3dent with mgn12 aka Enderwire to Ender3dent conversion showing the need for thicker foam (weather stripes in this case)
![Enderwire Conversion](/Gallery/EnderwireToEnder3dent_mgn12_.jpg "Enderwire Conversion")


  </details>
