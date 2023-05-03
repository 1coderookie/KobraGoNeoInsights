<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Problems  
In this chapter I'll list some of the most common problems people seem to have and what to do about them. Of course this chapter won't cover all of the possible problems one would probably have to deal with, but at least some of the typical problems beginners struggle with will be covered. If you don't find the answer to your specific problem here, please do a research by your own - there are countless websites as well as YouTube videos out there.  

(Note: WIP, so maybe come back another time as well ;) )   

## First Layer Problems / Print Comes Off
If you're having the problem that your first layer isn't consistent across the plate and/or the print doesn't stick on the plate (even though you really cleaned the PEI plate), then it's most likely that your [z-offset](calibration.md#z-offset) isn't right and/or you're dealing with a warped or tilted [bed](hardware/bed.md) and therefore experience certain areas where the distance between the nozzle and the plate will vary too much.   
  
- As a rule of thumb you can keep in mind that if the nozzle is too far above the bed, the prints won't stick and (depending on how far above the nozzle actually is) may result in a spaghetti incident (which is filament all over the place) or a blob of fear (which is a large clump of filament built up around the hotend).  
  If the nozzle is too close to the bed, the filament will get squished into the plate too much and that will (depending on *how* close the nozzle actually is) provoke clogging as well as it makes it difficult to remove the printed model later.  
  *The first layer is crucial for a perfect print, so take your time and get your z-offset dialed in well.*   
  See the section ["Z-Offset"](calibration.md#z-offset) for further tips and check out [this handy reference](https://i.imgur.com/hIcGr8U.png) as well for determining the perfect 1st layer.  
- Also make sure that you trammed the [x-axis gantry](hardware/axes.md#x-axis-gantry), so that the nozzle has the same distance to the plate across the whole area. This might not be enough though if you're encountering a tilted bed along the y-axis, so check the next listing. 
- If you're using the rigid stock spacers (the black round parts between the bedplate and the bedgantry) that came with the printer, then it's most likely that they're not all of the same height (at my Neo they *all* had a different height!). Of course that'll lead to a somewhat warped or tilted bed.  
  Before you start fiddling around with that either trying to get them all to the same height by e.g. sanding them down or by putting some sort of thin material underneath them to eaglize the height, I'd recommend to just get some [adjustable spacers](hardware/bed.md#different-spacers) for the bed for being able to tram the bed itself as well.  
- I'd recommend to check the bedmesh values (query M503 through a program like e.g. OctoPrint, Pronterface to get them listed) or use e.g. OctoPrint for getting a meshview out of it. By doing so you can see how 'flat' and trammed the bed is.  
  If it's tilted, tram it.  
  If it's warped or bent (like e.g. a bow) or if you're having certain spots which seem to be bulges or dents or if you have a certain area which is lower, you can use *Kapton tape* to equalize those areas/spots. Just take off the PEI plate, stick pieces of the Kapton tape right onto the magnetic foil of the bed, put the PEI plate back on and do another ABL sequence. Then check the values or the meshview again. By doing so step by step, you can get yourself a bed as flat as possible. Minor deviations should be compensated by the ABL function later when printing.  
  See the chapter ["Bed"](hardware/bed.md) (mind the expandable textboxes) as well for more informations.  
- Wiggle the bed and check if it moves in the vertical plane. If it does, check the bolts and nuts of the bedgantry and [check the v-slot wheels for perfect position](hardware/axes.md#v-slot-wheels-position_2). Most likely the wheels (or at least one) are a bit too far away from the aluminum frame. Adjust the position of the wheels then, but pay attention to not adjust them too tight as well.  
- Of course you have to pay attention that you really cleaned the PEI plate of the bed properly using e.g. simple dishwasher soap (no balm or 'soft' soap as they often contain some oily ingredients) and IPA to make the prints stick to it. I personally prefer and highly recommend *silicone remover spray* (that's the stuff the guys are using who are painting cars on a professional basis to get off any oil and grease off the chassis before starting the actual paintjob), it just works great. 
- Avoid touching the plate with your bare hands and fingers as that'll leave a tiny amount of grease onto the plate as well.  
- Also make sure that you chose the correct temperature of the bed for the filament you're using. For PLA for example it should be around 55°-60°C. If the bed is too hot, then the print won't reliably stick to it either.   
- Once the plate is clean, the z-offset is dialed in and the bedtemp is correct for the type of filament, the PEI plate really works great. There's *no need* to mess around with some sort of gluestick, tape, hairspray or whatsoever.  
- I'd also suppose to add a brim to your model (you need to do it in the slicer), which helps keeping the print staying on the plate a lot. This is especially useful for objects with a small base. You can configure the width of the brim in your slicer. After finishing the print, you just wait until the object is cooled down and then you can break/tear the brim off the object. If tiny amounts of the brim stay at the model, just use a sharp cutter.   
 

## Stringing
Stringing can be caused and affected by different factors and therefore can't always be avoided by adjusting retraction settings only. You can find countless articles about it, so maybe do a little research on it.  
Based on my own experiences, the following variables besides the retraction settings should be taken into account as well as one probably doesn't think about them in the first place:  
    
- The type of filament (PLA, ABS, PETG, TPU).  
- The quality of filament.  
- The moisture of filament: moist filament increases stringing.  
- The printing temperature: too high as well as too low printing temperatures cause stringing.  
- The [feeder gear pressure](hardware/printhead.md#extruder-feeder): if it's too low, the gear can't grab the filament reliably and therefore can't retract reliably.  
- The state of the feeder gear: if the teeth of the feeder gear which grabs the filament is kinda clogged due to debris of the filament, then it might slip as well.   
- The quality and the state of the [nozzle](hardware/printhead.md#nozzle): low-quality nozzles as well as worn out and/or slightly clogged nozzles can increase stringing. Also the diameter of the nozzle has an impact as it determines how much filament gets extruded.   
- The quality and the state of the PTFE tube inside of the heatbreak (Neo) or the bowden tube overall (Go).  
  As an example: stringing got way better after I replaced the stock PTFE tube with a Capricorn one, it seems that the lower friction of the Capricorn tube affected the retraction capability. Also a slightly clogged and/or deformed tip of the PTFE tube affected this a lot.  
- [Retraction settings](calibration.md#retraction-settings), so the retraction *distance* and the retraction *speed*.  
  Even though one would usually assume that higher values should/would be better to avoid or at least deal with stringing, it's not always the case. So instead of e.g. going higher than 1mm retraction distance at the direct drive of the Neo (which would provoke clogging), go much lower and see how it goes.  
  This seems to be affected not only by the *type* of filament (flexible filament like TPU needs completely different settings than pretty hard filament like PLA for example), but also by the *quality* of filament. Often cheap filament is lighter and more flexible than high quality filament and therefore it needs lower retraction settings overall to achieve good results.   
- The object one wants to print: certain objects just caused stringing, even tho I usually printed without any stringing. I'd recommend to print retraction towers with two cone-shaped towers as well, to get the different diameter into account as well.  
- The settings of the slicer, like wiping, z-hop, outer- vs. inner perimeter and so on. There are many articles and videos about this topic, so I'd recommend to do some research on it for your specific slicer.  
    

## Holes And/Or Bulges In Layers 
These are mostly signs of under- / overextrusion and/or a clogged nozzle.  

- If you observe a **regular pattern** like a vertical line where these **gaps and bulges** occur, then it's most likely the z-seam. You could change the setting of your slicer for the z-seam to "random", but that'll lead to random artefacts all over the print. In that case you'll most likely also note these artefacts in other spots of your model where layers start or end.  
  As you can't use Linear Advance with the stock firmware, there isn't that much you can do about this under- and overextrusion an the beginning and the end of a layer besides making sure that you [calibrated the e-steps](calibration.md#calibrating-e-steps) correctly. You might be able to tweak some settings in your slicer though and optimize it a bit.    
- If you observe **holes in layers**, or even longer **lines in layers where filament is missing**, then it's most likely too much retraction distance and/or a (partial) clog you're dealing with (which also gets provoked by too much retraction distance btw).  
  So I'd recommend to check the [retraction settings](calibration.md#retraction-settings) and [clean the nozzle](hardware/printhead.md#cleaning-the-nozzle) by e.g. doing some cold pulls. If the problem gets a bit better but persists, I'd recommend to disassemble the hotend, clean everything, inspect and maintain it and reassemble it again. Also pay attention to the PTFE tube and make sure you reassembled the hotend correctly. Check out the chapter ["Printhead"](hardware/printhead.md) for more informations.   

## Zits And Blobs
If you're printing from an SD card and you notice zits and blobs all over the print in a regular pattern, then turn off the resume function. It makes the printer stop regularly for a tiny moment when saving to the card which results in those artefacts due to the leaking filament.  
Best would be to not print from the SD card and use an [extra host](printserver.md) running e.g. OctoPrint on.  
  
## 'Rough' Look, Uneven And 'Bubbly' Surface
This is mostly caused by moist filament. When the filament gets heated up in the hotend and gets extruded, the water 'boils' up and the damp releases which results in a pretty 'rough' look. Even tho PLA isn't *that* sensitive to moisture like e.g. Nylon, it still may be moist - even a fresh and sealed spool can be moist (due to the production procedure).  

It's actually kinda difficult for me to describe the look of the surface to give you an exact impression, so I'll keep my eyes open for a good picture I might use to illustrate it.  
You can check if the filament is (way) too moist by extruding with the nozzle up in the air. Watch the string of melted filament which comes out of the hotend, right at the nozzle. Does it seem to be 'bubbly'? Do those bubbles even pop? If so, then it's definitely too moist.  

The solution for this would be to dry your filament. You can either get yourself one of those (imho overpriced) filament dryers, put the spool in the oven in your kitchen (don't go over 50°C for PLA tho!) or use a food dehydrator. I personally don't use any of that - I just use the well-controlled solution we all already have: the heated bed! Just lay your spool flat onto the bed, cover it with e.g. a cardboard box or so and heat it up to about 45°C. Then let it sit for a few hours.  

When storing your filament, use e.g. some vaccum sealed bags and add dessicant.  

## The Pattern Of The Infill 'Shines' Through
If you experience a regular pattern on the outside of the printed model, it might be caused by the infill. If you print the infill first and then print the outer perimeters, then the infill will 'shine' through so to say. So try to change the belonging setting in your slicer and print the outer perimeters/walls first.  

## Dark Pieces Of Melted Filament
If you see dark (like honey or even brown or black) pieces of melted filament somewhere on your print, then this is a sign of a clogged or (most likely) even wrong assembled hotend. It's caused by filament which stays in the hotend somewhere, gets burned and when it comes out it's dark.  
Most of the time there is a little gap where the filament gets collected, like between the nozzle and the PTFE tube when not being cut or assembled properly.  
  
The solution here would be to do some cold pulls first to get as much filament out as possible, then disassemble the hotend and inspect it. Pay attention to the PTFE tube as well. When reassembling, make sure everything sits in place as it should and the tube is long enough to hit the nozzle (and at the Neo it also has to go up to the extruder gear as well). The tube needs to be cut perpendicular as well.  
*If any gap occurs, the melted filament will stick there again and get burned and the problem will occur again.*    

## Layer Shifts / Pushed Off Prints / Stuck Axes
- If you're experiencing layer shifts or stuck movements at either the x- or y-axis, check the position of the wheels and the belt tension.  
- If you're experiencing problems in the height or if your prints get pushed off the bed because the nozzle hit them at a certain height, check the wheels of the x-axis gantry which run along the aluminum frame of the z-axis as well as the lead screw, the anti-backlash nut, the alignment and the complete assembly of the whole z-axis.  

Generally speaking, everything should run smooth when you move it manually by hand. If you feel some kind of resistance or a jam at certain spots, check the belonging axis and the involved parts. Deformed and/or too tight wheels can cause 'similar' problems like a misaligned z-axis for example. See the chapter ["Axes"](hardware/axes.md) for more informations.  

## Can't Load New Filament
If you can't load new filament, first of all check if you pulled the lever on the feeder gear.  
If you did so and were able to insert the filament but it seems that it's getting stuck lower down in the hotend, then it's most likely that the PTFE tube inside of the hotend is clogged or deformed or that you have a clog in or above the nozzle somewhere. To clean, inspect and maintain it, you need to disassemble the hotend. Check the section ["Disassembling The Hotend"](hardware/printhead.md#disassembling-the-hotend) for more informations.  

## Error Messages
It might happen that the whole display turns red and an error message "Err: MINTEMP/MAXTMEP - PRINTER HALTED - Please reset" will be shown (see the following sections for the specific message), blocking any further usage. You won't be able to use the printer anymore unless the problem that causes this error will be solved (at least it was the case when I faced this kind of error message).  
  
Before going into details here, I have to mention that I personally only came across the warnings "Err: MAXTEMP: E1" and "Err: MINTEMP: Bed". I might be wrong of course, but looking at the underlying reasons for these kind of errors, I *assume* that it's also possible to get the warnings "Err: MINTEMP: E1" and "Err: MAXTEMP: Bed". So please keep that in mind when reading further..   
  
- **MINTEMP** erros:  
  These kind of errors are called "thermal runaway errors" and they are triggered by a function called "thermal runaway protection".  
  Basically it's a good thing that these appear (even though the underlying problem isn't 'good' most of the time), as that shows you that this protective function is working. The function observes the development of the heat in a given time and triggers the messages when the expexted temperature of either the bed or the hotend drops about a certain amount of degrees within a certain amount of time and then it triggers the "MINTEMP" error.   
  These are the sections in the files `Configuration_adv.h` of the belonging [stock firmware](firmware/fw_marlin.md#default-settings):   
  ```
  Thermal Protection / Thermal Runaway -> Hotend:
  #define THERMAL_PROTECTION_PERIOD 35         // Seconds
  #define THERMAL_PROTECTION_HYSTERESIS 10     // Degrees Celsius
  ```
  ```
  Thermal Protection / Thermal Runaway -> Bed:
  #define THERMAL_PROTECTION_BED_PERIOD        20 // Seconds
  #define THERMAL_PROTECTION_BED_HYSTERESIS     2 // Degrees Celsius
  ```
  
- **MAXTEMP** errors will be triggered when the temperature of the belonging part (extruder or bed) exceeds the defined maximum temperature (or if a certain hardware error occurs which leads to a resistance value which will be interpreted by the MCU as a too high temperature).  
  The maximum temperatures for both the extruder and the bed are set in the files `Configuration.h` of the belonging [stock firmware](firmware/fw_marlin.md#default-settings):  

  ```
  // Above this temperature the heater will be switched off. This can protect components from overheating, but NOT from shorts and failures.
  #define HEATER_0_MAXTEMP 275  
  #define BED_MAXTEMP      120  // max target temp-10=110
  ```
- It also might happen that a **negative temperature** will be reported. This is most likely the case when a lot of the thin wires of the cable inside of the insulation broke and lost contact and only a few wires are still ok. In that case the resistance raises which leads to a faulty temperature reading. This is also one of the most common reasons which cause the MINTEMP error due to a fluctuating resistance and temperature reading while the e.g. bed and therefore the cable moves (which then causes lost contacts of the broken wires in certain positions), but it'll be mentioned as one of the possible reasons further down below as well. There were just some users who reported a negative temperature reading of the actual bed temperature but they didn't had the red 'locked' screen, so I wanted to mention this scenario already here as well.    

In the following sections I'll go over these messages for noth the extruder and the bed and what the reasons and possible solutions might be.  

### Err: MINTEMP/MAXTEMP: E1
![Err: MAXTEMP: E1](assets/images/controlunit_err_e1-max-temp_web.jpg)  
  
This message will be triggered either if the temperature of the extruder (= E1) drops more than 10°C within a timeframe of 35seconds (= MINTEMP error) or if it reaches above the limit of 275°C (or if you have a certain hardware issue which causes a certain resistance value) (= MAXTEMP error) as you can see in the belonging code sections of the firmware settings:  
```
Thermal Protection / Thermal Runaway -> Hotend:
#define THERMAL_PROTECTION_PERIOD 35         // Seconds
#define THERMAL_PROTECTION_HYSTERESIS 10     // Degrees Celsius
```  
```
// Above this temperature the heater will be switched off. This can protect components from overheating, but NOT from shorts and failures.
#define HEATER_0_MAXTEMP 275  
```
  
Reasons that can cause this might vary from being easy to fix to a real hardware issue. Often the moment *when* this error message actually appears can give you a hint where to search for the problem. I'll list the (imho) most common reasons in the following.   

- The printer is exposed to cold air and therefore the temperature drops rapidly. This might be caused by e.g. a window or door you opened. So make sure to prevent the printer being exposed to an area where (cold) air ventilates too much. Also use the printer in a room which isn't too cold in general.  
- The blue [silicone sock](hardware/printhead.md#silicone-sock) of the heater block came off (or isn't present because you took it off) and the part cooling fan blows at the heater block instead of blowing at the printed part. So make sure to add a silicone sock and adjust the airflow of the part cooling fan.  
- The wires of the thermistor cable are broken (inside of the insulation) and they're losing contact due to movement that occurs.  
- The insulation of the thermistor cable is harmed and the blank wires of both cables are touching each other.  
- The thermistor cable is completely broken or ripped off.  
- The thermistor itself is faulty.  
- The plug of the thermistor cable at the mainboard somehow came off.  
- An electronic component of the mainboard is broken (e.g. due to a shortcut).   

If the error pops up while the printer is moving or printing, then it's most likely one of the first two things I mentioned above.  
It might also be the third point as a broken wire loses contact due to movements and therefore the resistance becomes bigger (if just a few wires of the cable are broken inside of the insulation) or the signal won't be transmitted anymore at all (if the wire is completely broken).  
If the error pops up right away when you turn on the printer, then it's most likely one of the other problems.  

The solution depends on the underlying problem of course.  
If you face a hardware issue of the thermistor part (like a partially or completely broken sensor cable or a faulty thermistor which you could determine by using a multimeter as well), just get yourself a new thermistor and replace the broken one.  
  
If that doesn't solve the issue, I'd suppose to take a magnifying glass and inspect the SMD parts of the mainboard. You probably won't be able to spot a faulty part as not every defect will be visible, but it might happen that you'll spot a melted part like I did when I faced the "Err: MAXTEMP: E1" issue as the following picture shows. <br> ![Melted D4](assets/images/mainboard_melted-D4_web.jpg)  

Once you solved the problem and turn the printer back on, the error message shouldn't appear anymore and you should be able to print again.  
Good luck!

### Err: MINTEMP/MAXTEMP: Bed
![Err: MINTEMP: Bed](assets/images/controlunit_err_bed-min-temp_web.jpg)  

This message will be triggered either if the temperature of the bed drops more than 2°C within a timeframe of 20seconds (= MINTEMP error) or if it reaches above the limit of 120°C (or if you have a certain hardware issue which causes a certain resistance value) (= MAXTEMP error) as you can see in the belonging code sections of the firmware settings:  
```
Thermal Protection / Thermal Runaway -> Bed:
#define THERMAL_PROTECTION_BED_PERIOD        20 // Seconds
#define THERMAL_PROTECTION_BED_HYSTERESIS     2 // Degrees Celsius
```
```
// Above this temperature the heater will be switched off. This can protect components from overheating, but NOT from shorts and failures.
#define BED_MAXTEMP      120  // max target temp-10=110
```
  
Reasons that can cause this might vary from being easy to fix to a real hardware issue. Often the moment *when* this error message actually appears can give you a hint where to search for the problem. I'll list the (imho) most common reasons in the following.   

- The printer is exposed to cold air and therefore the temperature drops rapidly. This might be caused by e.g. a window or door you opened. So make sure to prevent the printer being exposed to an area where (cold) air ventilates too much. Also use the printer in a room which isn't too cold in general.  
  
- The wires of the thermistor cable are broken (inside of the insulation) and they're losing contact due to movement that occurs.  
- The insulation of the thermistor cable is harmed and the blank wires of both cables are touching each other.  
- The thermistor cable is completely broken or ripped off.  
- The thermistor itself is faulty.  
- The plug of the thermistor cable at the mainboard somehow came off.  
- An electronic component of the mainboard is broken (e.g. due to a shortcut).   

If the error pops up while the printer is moving or printing, then it's most likely one of the first two things I mentioned above.    
It's actually *most likely that you're dealing with broken wires* - that's a pretty common issue, as they are made of poor quality and tend to brake over time. In this case a broken wire loses contact due to movements of the bed and therefore the resistance becomes bigger (if just a few wires of the cable are broken inside of the insulation) or the signal won't be transmitted anymore at all (if the wire is completely broken).  
If the error pops up right away when you turn on the printer, then it's most likely one of the other problems.  

The solution depends on the underlying problem of course.  
If you face a hardware issue like a partially or completely broken sensor cable, you can replace the sensor cables. I'll add more specific information about how to do so soon.  
If you face a hardware issue of the thermistor part (which you could determine by using a multimeter), you can get yourself new thermistor 100K NTC thermistor and replace the broken one.   
  
If that doesn't solve the issue, I'd suppose to take a magnifying glass and inspect the SMD parts of the mainboard. You probably won't be able to spot a faulty part as not every defect will be visible, but it might happen that you'll spot a melted part like I did when I faced the "Err: MAXTEMP: E1" issue as the following picture shows. <br> ![Melted D4](assets/images/mainboard_melted-D4_web.jpg)  

Once you solved the problem and turn the printer back on, the error message shouldn't appear anymore and you should be able to print again.  
Good luck!
