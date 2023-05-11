<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Printhead
The printheads of the **Go** and the **Neo** aren't identical because of the different type of extruder they're using:  

- the **Go** uses a bowden drive feeder system while 
- the **Neo** is using a direct drive feeder system.   
  
If you look at both printheads from the front and compare their size, you'll notice that the one of the **Go** is a bit smaller (and lighter) and more square than the wider (and heavier) and more rectangular shaped one of the **Neo**.  
  
---  
  
## Go
The following picture shows a new printhead for the **Go** as it comes as a spare part.  
  
![New Go print head spare part](../assets/images/head_go_spare_web.jpg)

The following picture shows a close up view of the printhead of the **Go** from the front view. At the bottom you can see the nozzle in the center and the orange tip of the ABL sensor at the left side.  
  
![Go printhead front view](../assets/images/head_go_front_web.jpg)    
  
You can find a more detailed inside-view further down below in the disassembling section.  
  
---  
  
## Neo  
The following picture shows a new printhead for the **Neo** as it comes as a spare part.  
  
![New Neo print head spare part](../assets/images/head_neo-spare_web.jpg)

The following picture shows a close up view of the printhead of the **Neo** from the front view. At the bottom you can see the blue silicone sock of the heater block with the nozzle in the center and the orange tip of the ABL sensor at the right side.  
  
![Neo printhead front view](../assets/images/head_neo-front_web.jpg) 
  
You can find a more detailed inside-view further down below in the disassembling section.  
  
---

## ABL Sensor
Both printers come with a proximity sensor for automatic bed levelling (ABL) which is (afaik) the same model.  
The ABL sensor at the **Go** is mounted pretty much straight behind the heater block, where at the **Neo** it's located a few centimeters to the right side next to the heater block.  
  
??? tip "Sensor Position"  

    Most of the time users have to adjust the postion of the ABL sensor, even when the printer is brandnew and came straight from the factory. The steps of the procedure are described within the section of the specific model.     
  
---  
  
### Go
The following picture shows the location of the ABL sensor at the printhead of the **Go**, looking at it from a bottom view angle - the ABL sensor is the part at the left side with the round orange tip.   
  
![Orange tip of the ABL sensor at the right side](../assets/images/head_go_bottom_web.jpg)
    
The ABL sensor itself is mounted in a plastic bracket which is the mounted to the metal backplate. You can adjust the height of the position by loosening the screw at the left side of the clamp which then allows you to move the sensor.  
  
![ABL sensor](../assets/images/head_go_ABL-bracket-side_web.jpg)
  
---  
    
#### Leveling The ABL Sensor

Check if you need to level your ABL sensor in relation to the nozzle (which should be done after every maintenance at the hotend as well as when you got the printer brandnew from the manufacturer).  

!!! warning "Attention"  

    After adjusting the height of the ABL sensor, adjust your Z offset before starting to print!  

The following picture shows a sensor that should/has to be leveled (don't mind the tiny rest of filament at the tip of the nozzle which touches the paper instead of the nozzle itself though, I chipped it away before leveling everything).      
![This sensor needs to be leveld](../assets/images/head_neo_ABL2level_web.jpg)

Leveling procedure:

- Take the [height gauge](https://cdn.shopify.com/s/files/1/0245/5519/2380/files/Height_gauge.rar?v=1667814312) from Anycubic. <br> If you don't have the height gauge, take a sheet of paper and the bigger two-sided open-end wrench that came with your printer. <br> If you also don't have that, take something with a flat surface that is 1.95mm thick as this is the thickness of the wrench that came with the printer (2mm will be fine also I guess).
- Put on the spring steel plate on the heater bed and place the printhead about the center of the bed.
- If you're using the height gauge, put it under the printhead and lower the head by turning the z axis rod manually. The nozzle should then touch the lower part of the gauge while the proximity sensor should touch the higher part of it. 
- If you don't have/use the height gauge, place a sheet of paper under the printhead now. Then lower the head to make the nozzle touch the sheet of paper. You should still be able to move the paper but you should feel a minimum amount of resistance as a sign that the nozzle is touching it. <br> Now place the wrench under the ABL sensor. The sensor should touch the wrench.  
- If you need to adjust the height of the sensor, loosen the screw at the left side of the clamp that holds the sensor in place. <br> ![Screw clamp](../assets/images/head_go_ABL-bracket-side_web.jpg) <br> Move the sensor and tighten up the screw again once you found the correct position.  
- After completing the beforementioned steps, take the parts away from the bed, set your Z offset to zero (0) if you didn't do it yet and home all axes. Then execute the ABL process and dial in your z-offset.          
  
---  
    
### Neo
The following picture shows the location of the ABL sensor at the printhead of the **Neo**, looking at it from a bottom view angle - the ABL sensor is the part at the right side with the round orange tip.   
  
![Orange tip of the ABL sensor at the right side](../assets/images/head_neo-bottom_web.jpg)
    
The ABL sensor itself is mounted in a plastic bracket which is the mounted to the metal backplate. You can adjust the height of the position by a little spring supported screw located at the top.  
  
![ABL sensor](../assets/images/head_ABL-sensor-front_web.jpg)
  
---  
      
#### Leveling The ABL Sensor

Check if you need to level your ABL sensor in relation to the nozzle (which should be done after every maintenance at the hotend as well as when you got the printer brandnew from the manufacturer).  

!!! warning "Attention"  

    After adjusting the height of the ABL sensor, adjust your Z offset before starting to print!  

The following picture shows a sensor that should/has to be leveled (don't mind the tiny rest of filament at the tip of the nozzle which touches the paper instead of the nozzle itself though, I chipped it away before leveling everything).      
![This sensor needs to be leveld](../assets/images/head_neo_ABL2level_web.jpg)

Leveling procedure:  

- To adjust the height of the ABL sensor and level it, check out the video from Anycubic ["Leveling Operation for Anycubic Kobra Neo"](https://www.youtube.com/watch?v=25x84AaiUpQ) how to do so. However, I'll also list the steps in the following. 
- Take the [height gauge](https://cdn.shopify.com/s/files/1/0245/5519/2380/files/Height_gauge.rar?v=1667814312) from Anycubic. <br> If you don't have the height gauge, take a sheet of paper and the bigger two-sided open-end wrench that came with your printer. <br> If you also don't have that, take something with a flat surface that is 1.95mm thick as this is the thickness of the wrench that came with the printer (2mm will be fine also I guess).
- Put on the spring steel plate on the heater bed and place the printhead about the center of the bed.
- If you're using the height gauge, put it under the printhead and lower the head by turning the z axis rod manually. The nozzle should then touch the lower part of the gauge while the proximity sensor should touch the higher part of it. 
- If you don't have/use the height gauge, place a sheet of paper under the printhead now. Then lower the head to make the nozzle touch the sheet of paper. You should still be able to move the paper but you should feel a minimum amount of resistance as a sign that the nozzle is touching it. <br> Now place the wrench under the ABL sensor. The sensor should touch the wrench.  
- If the sensor is too high or too low, adjust the height by turning the little M2 hexagon socket screw at the top of the bracket that holds the sensor.  <br> ![Screw at the top to move the sledge](../assets/images/head_ABL-sensor_top_closeup_web.jpg) <br> You're only able to move it a few milimeters by doing so though!   
-  If you need to adjust a bigger height, you'd need to disassemble the sensor from the bracket itself first to already change it's position in the bracket (see the pictures of it in the "dismounting" section above.  
- After completing the beforementioned steps, take the parts away from the bed, set your Z offset to zero (0) if you didn't do it yet and home all axes. Then execute the ABL process and dial in your z-offset.
       
---  
  
## Extruder / Feeder
The **Go** uses a bowden drive extruder/feeder, while the **Neo** is using a direct drive extruder/feeder.  
  
---
  
### Go
  
The following picture shows the bowden drive feeder system of the **Go**. The feeder gear box mounted onto the extruder motor is located on the left side next to the z-axis lead screw and is connected with the white PTFE bowden tube (which leads the filament) to the printhead.  

![](../assets/images/head_GO_feeder-head_web.jpg)  

A closer view of the feeder gear box mounted onto the extruder motor:  

![](../assets/images/head_GO_feeder-system_web.jpg)  

The following picture shows the feeder gear box itself.  

![](../assets/images/head_GO_feeder-gear_web.jpg)  



<!---  
??? tip "Feeder Gear Pressure"

    When adjusting the pressure of the feeder gear, make sure you don't tighten it up too much as it could squeeze and deform the filament. On the other hand it shouldn't be too loose though as it should transport the filament reliably.  
    When pulling out the filament of the extruder system, you should notice little dents on the surface of the filament from the teeth of the feeder gear, the filament itself shouldn't be squeezed and deformed though, it should still be "round" so to say. You don't want the feeder gear to "bite" too much into the filament as well though, as this may lead to inconsistentites of the filament flow. I personally like to extrude a bit so that the gear actually has to pull it in. Then I do a cold pull and check the marks of the gear on the filament itself. If you can see and feel little marks of the teeth of the gear on the surface of the filament, then it should be ok. If you don't feel and see any marks, then it's too loose. PLA is pretty hard, so the pressure can/should be a bit higher as well, but if the marks are pretty deep, then it already might be too much. If the filament is already a bit squeezed and kinda flat, then it's definitely way too much pressure (you'll most likely experience some weird artefacts, inconcisties and patterns at your prints as well then). 
    The filament should be fed reliably, which especially comes into account while retracting. So keep an eye on the shaft of the motor by looking at the back of the motor - if you notice that it's slipping while retracting, you definitely need to increase the tension.  
    As a rule of thumb you can keep in mind that the pressure should be higher when using hard filament like PLA and lower when using soft filament like TPU.    
-->

---  
  
### Neo
The following picture shows the extruder/feeder of the **Neo** with the mounted plastic cover of the printhead.  
  
![Direct drive of the Neo](../assets/images/head_neo_directdrive_web.jpg)
  
At the top in front of the little hole where the filament is inserted you find a little lever for manual release of the tension while loading/unloading the filament. The screw in the front adjusts the pressure of the feeder gear which is brought onto the filament. The following picture shows the mechanism without the plastic cover.  
  
![Feeder top view](../assets/images/head_feeder_topview_web.jpg)
  
You can access the inside of the feeder system by dismounting the heatsink, which is located at the right side underneath the heatsink fan. The following picture shows the inside of the system.  

![Feeder inside](../assets/images/head_neo_feeder-inside_web.jpg)  
  
!!! warning "Retraction Settings"

    Make sure that you set the retraction distance and speed to the correct values for a direct drive!  
    In general, it's supposed to be something around 1mm retraction distance for direct drive systems like the **Neo**. The profile from Anycubic has this setting set to 6mm though, which is *way* too much for the direct drive! If you set the distance to a value which is too high (e.g. the default 6mm for the **Go** as a bowden drive), the melted filament might be pulled back too far and reaches the PTFE tube which might get clogged then.  
    You can find some more information about this topic in the section ["Retraction Settings"](../calibration.md#retraction-settings).
  
??? tip "Feeder Gear Pressure"

    When adjusting the pressure of the feeder gear, make sure you don't tighten it up too much as it could squeeze and deform the filament. On the other hand it shouldn't be too loose though as it should transport the filament reliably.  
    When pulling out the filament of the extruder system, you should notice little dents on the surface of the filament from the teeth of the feeder gear, the filament itself shouldn't be squeezed and deformed though, it should still be "round" so to say. You don't want the feeder gear to "bite" too much into the filament as well though, as this may lead to inconsistentites of the filament flow. I personally like to extrude a bit so that the gear actually has to pull it in. Then I do a cold pull and check the marks of the gear on the filament itself. If you can see and feel little marks of the teeth of the gear on the surface of the filament, then it should be ok. If you don't feel and see any marks, then it's too loose. PLA is pretty hard, so the pressure can/should be a bit higher as well, but if the marks are pretty deep, then it already might be too much. If the filament is already a bit squeezed and kinda flat, then it's definitely way too much pressure (you'll most likely experience some weird artefacts, inconcisties and patterns at your prints as well then).   
    The filament should be fed reliably, which especially comes into account while retracting. So keep an eye on the shaft of the motor by looking at the back of the motor - if you notice that it's slipping while retracting, you definitely need to increase the tension.  
    As a rule of thumb you can keep in mind that the pressure should be higher when using hard filament like PLA and lower when using soft filament like TPU.  
  
??? tip "Print A Filament Guiding Sleeve"

    I printed a [filament guiding sleeve](https://www.thingiverse.com/thing:5720072) made by ["fredfeuerstein2"](https://www.thingiverse.com/fredfeuerstein2/designs) which sticks in the hole of the feeder gear system where the filament enters. It's guiding the filament and makes sure that the filament will be fed centered. <br> [!Filament guiding sleeve](../assets/images/head_neo_filguide_web.jpg) <br> It's originally designed for the regular Kobra, but it does fit and works great on the **Neo** as well.   
  
---  
  
## Hotend & Heatbreak
In the following, the specific hotends will be shown. Before jumping to the specific section, mind the notes in the expandable textboxes as well.  
  
!!! warning

    - Too high temperatures may harm the PTFE tube - it may become deformed!   
    - If you dismounted the hotend and you put it back into the printhead, make sure you check and adjust the position of the ABL sensor in relation to the nozzle and that you check and set your new z-offset afterwards!  
    - If you replaced your old hotend with a new one (regardless of whether you also replaced the thermistor and/or cartridge heater with a new one or keep using the existing ones), execute a PID tuning afterwards!
  
??? tip "Can't Load New Filament?!"

    If you can't load new filament, first of all check if you pulled the lever on the feeder gear.
    If you did so and were able to insert the filament but it seems that it's getting stuck lower down in the hotend, then it's most likely that the PTFE tube inside of the hotend is clogged or deformed or that you have a clog in or above the nozzle somewhere. To clean, inspect and maintain it, you need to disassemble the hotend. Check the section ["Disassembling The Hotend"](#disassembling-the-hotend) further down below for more information.     
    
??? info "Spare Part PTFE Bowden Tube"

    If you need a new PTFE bowden tube, I'd recommend to get the 4mm "Capricorn XS" tube for 1.75mm filament at the length of 1m. Then just cut the belonging length and replace the old bowden tube. You can also get it in a set with a cutter.  
    However, make sure you make a clean and perpendicular cut at a 90° angle to avoid any small gaps between the nozzle and the end of the tube! I personally like to just cut along the end of the heatbreak, using it as a guide for the knife. <br> ![Capricorn XS](../assets/images/head_capricornXS_web.jpg)     
    
??? info "Spare Part Heatbreak"

    If you need a new heatbreak, you should be able to use whichever V5 compatible heatbreak you'd like to use, you just have to pay attention to the dimensions. It should be about the same length as the stock one, so don't buy anything significantly shorter or longer. Make sure to pay attention to the surface at the top part - that should be even and smooth, so don't get yourself the ones with the thread on the outside.   
    Some people 'upgraded' to an all-metal heatbreak, which one should avoid though if only printing PLA as it may cause and increase clogging problems. So up to me always go with a heatbreak that uses a PTFE inliner all the way down to the nozzle in case you're only or mostly printing PLA.   
    The following picture shows such a heatbreak from a third party manufacturer which I use in my **Neo**, it's about 27mm long and works just fine. Due to the slightly bigger length than the stock one, the nozzle is a bit further down though, so I had to adjust the position of the printed part cooling fan duct I'm using. I chose the 'regular' version with the additional PTFE tube instead of an all-metal one as I'm only PLA right now. <br> ![3rd party heatbreak](../assets/images/head_3rdparty-heatbreak_web.jpg)  
  
??? example "Large Clump Of Melted Filament Built Up"

    Sometimes it may happen that melted filament builds up on top of the heater block to a large clump. The reason for that is that the heatbreak isn't screwed into the heater block tight enough so that the melted fiolament can squeeze out. It also may be caused by bad and cheap parts where the thread isn't just as good as it should be. <br> ![Blob](../assets/images/head_blob_web.jpg) <br> So if you encouter this problem, here is what I recommend to do (based on my own experience with this dilemma).  
    
    - Take off the plastic cover first to get better access to the whole area.  
    - Heat up everthing - I did this by using the preherat function for PLA at the control unit.
    - Once the filament starts to melt and gets soft, grab a wooden stick and take away as much as possible carefully. *Don't* use a screwdriver or something like that to do so as you might harm the wires and/or cause a shortcut at e.g. the contacts of the cartridge heater. <br> *Be really careful when taking away the clumps to not harm or rip off any of the wires!* You can also use a cloth to wipe off the melted filament from the heater block and so on, just make sure you don't burn yourself!  
    - For the next steps you need to be a bit quick in proceeding them, so if this is the first time you're diassembling the hotend, take a look at the sections here at the page and read them first so you'll know where the screws are located and which steps you need to take. Then proceed with the following steps.
    - So, once everything is as clean as possible, turn off the printer and loosen the grub screws inside the heater block to take out the thermistor and the cartridge heater. Give it a quick wipe with the cloth if they're covered by a lot of filament, too (but don't waste too much time here as the filament is becoming hard again now pretty quick!). 
    - Then take out the nozzle from the heater block and unscrew the heater block from the hotend. Pay attention if you can feel that the heatbreak was loose in the heater block to check if that was the reason for the filament being able to squeeze out and build up. 
    - Dismount the fan on the right side and loosen the two hexagon socket screws which are holding the heatbreak in place. If it doesn't fall out by itself, pull it out. When using the **Neo**, make sure the little PTFE tube also comes out, take it out of the heatbreak.  
    - If you were using a cheap nozzle and have a spare one, just throw away the old one. If it's a good or your only nozzle, try to get it back to work again by giving it a proper cleaning and doing some cold pulls when it's installed again. 
    - Now put all the metal parts (heatbreak, heater block and probably the nozzle) in a glass with acetone. close the lid and let it sit there for about 24hrs. The acetone won't dissolve PLA filament or so automagically like it does with ABS, but it'll make it soft and easier to clean. 
    - In the meantime you can take care of the thermistor and the cartridge heater. Scratch off the hardened filament from the metal parts by using a cutter for example, but be *really* careful to not slip off and harm any wires! I personally didn't take care of the little clump at the part where ther wires are coming out of the metal part because I didn't wanted to risk harming the wires, so I just let it sit there.  
    - When you're about to clean the meatal parts which soaked in the acetone, I'd recommend wearing disposable gloves as acteone isn't really healthy for your skin. So put on those gloves and start cleaning the parts by carefully scratching off the rest of the filament. Use a cutter, a brass brush etc., but always be careful to not really harm anything. Pay special attention to all the threads and the holes of the heater block where the thermistor and the cartridge heater will take place. If you don't get everything cleaned up at the first time, just put it back in the acetone, wait again and then repeat the cleaning steps. 
    - Once everything looks nice and clean, rinse off the acetone with clear water and let it dry. This is especially important for the inner side of the nozzle - you don't want to have acetone in there.  
    - Then reassemble everything and put it back in place. Read the notes in the specific sections here about how to reassemble the specific parts and what to pay attention to.  
    - At the end when everything is reassembled and you heated up the hotend to finally mount the nozzle and load the filament, extrude filament to see if everything is ok. 
    - If so (I hope it will be!), don't start printing right away - execute a PID tuning for the hotend first.  
    - Also check if you need to re-level the ABL sensor in relation to the nozzle due to a probably different position of the hotend now.  
    - Execute an ABL and take care of your Z-offset, most likely the position of your nozzle will be different due to a different position of the whole hotend.  
  
---  
   
### Go
  
The hotend of the **Go** is shown in the next pictures. In the second picture you can see the heatbreak screwed into the block but dismounted from the aluminum cooling element.  

![Hotend](../assets/images/head_go_hotend_web.jpg)  
  
![Hotend disassembled](../assets/images/head_go_hotend-dis_web.jpg)
  
---  
  
### Neo  
  
The hotend of the **Neo** is shown in the following picture. It's plugged into the heatsink and secured by two screws. The outer diameter of the heatbreak is 7mm at the thick part (top and bottom), at the smaller part between it's 6mm. The inner diameter is about 4.2mm. The length measured from the top until the 'stop ring' before the thread is 15.5mm and the length in total is about 24.6mm. 
  
![Hotend](../assets/images/head_neo_block-hotend-disass_web.jpg)  
  
Additionally there is a little PTFE-tube inside of it, which is about 4cm long and 4mm thick with a 2mm hole inside of it to guide the 1.75mm filament.  
  
![Hotend mounted with block and tube](../assets/images/head_neo_block-hotend-tube-used_web.jpg)    
  
??? info "Spare Part Hotend"

    - If you need a new hotend because your heater block or the heatbreak needs to be changed, you can get yourself the spare part hotend for the regular *Kobra*. If you look at the picture of it and compare it with the ones I've shown above, you'll notice that the shape of the heatbreak is the same. So up to me it'll fit perfectly.   
    - If the old thermistor and/or cartridge heater are still good and the wires aren't harmed, you don't have to fiddle around to use the new ones! Just take the existing ones out of the old heater block and install them in the new one.   
    - Besides that, the hotend for the *Kobra* comes with a cartridge heater and a thermistor which are also compatible with the ones from the **Go** and **Neo** - at least from a technical side of view. So you'd have them as a spare part also. <br> However, the wires of these parts are way too short though, so you wont't be able to connect them directly! So in case you have to use them, you probably could either just cut the plug and the old part and solder the wires together or (if you have the tools for that) crimp the specific socket for the plug to the old wire to just connect them this way. Polarity doesn't seem to matter here, so just connect the wires.  
    - *Remember to execute a PID tuning after changing the thermistor and/or the cartridge heater!*  
    - However, scroll down and check out the "Disassembling" section below to see how to dis- and reassemble it. *Maybe you don't need new parts, so try to clean up everything first and reassemble it before ordering new parts right away.*  
    
    Besides the stock hotend you can also just get or build yourself a hotend by using a V5 compatible heatbreak and heater block which fits just fine. The following picture shows a hotend I built myself from third party manufacturer parts: a regular heatbreak for V5 compatible heater blocks where the PTFE inliner moves all the way down to the nozzle (so it's *not* a full-metal heatbreak as I use to print PLA/PLA+ only right now), a V5 compatible heater block made of plated copper and a Capricorn XS PTFE tube. <br> ![3rd party hotend](../assets/images/head_3rdparty-hotend_web.jpg)  
      
---  
  
## Heater Block
Both printers use an E3D **V5** compatible heater block.  
Both the thermistor and the cartidge heater have to be plugged into the specific holes and should be fixed with at tiny grub screw (HEX 1.5).  
  
![Heater block V5](../assets/images/head_block-screws-close_web.jpg)  
  
!!! warning  

    If you need to replace the thermistor and/or the cartridge heater, *make sure you don't overtighten the screws as it could harm both the thermistor and the heater cartridge!* Note the dent from the screw and the deformed thermistor due to an overtightened screw from the manufacturer at my **Neo**. <br> ![Deformed thermistor due to an overtightened screw](../assets/images/head_therm-cart-broken_web.jpg)  
      
??? info "Spare Part Heater Block"

    If you need a new heater block, you can just get yourself a regular V5 compatible one. It might be smart to not get the cheapest one available as they sometimes lack of precision and therefore may cause problems with leaking filament. Usually the heater blocks are made of aluminum, but you can also get them made of plated copper as shown in the following picture. <br> ![V5 plated copper](../assets/images/head_heaterblock-v5-copper_web.jpg)  

---   
  
## Silicone Sock
The silicone sock that comes with the hotend insulates the heater block. Therefore it should stay in place and shouldn't come off, as it *might* cause the "thermal runaway" error.  
  
The following pictures shows a V5 heater block compatible silicone sock from the aftermarket on the left side and the stock sock on the right side.     
  
![Silicone socks top view](../assets/images/silisocks_top_web.jpg)   
  
Additionaly, the ones from the aftermarket also cover and therefore insulate the base of the nozzle - something that the stock ones don't do at all.  
  
![Silicone socks bottom view](../assets/images/silisocks_bottom_web.jpg)  
  
??? info "Spare Part Silicone Sock"  

    The sock which comes with the printhead isn't the best one to use (in my opinion) as it seems to come off pretty easily. There are compatible V5 silicone socks at the aftermarket which I personally use and which I can highly recommend. They have a bigger lip which slips over the heater block and covers a bigger area of the top than the one which comes with the printer. Therefore they stay in place much better when they heat up and become more flexible.    
    If you read the above and still don't know what you should look or search for, search for "silicone sock V5" for example as these socks are for a V5 heater block. You can get them pretty much everywhere, so if you use to shop at Amazon or ebay for example, you'll find many offers which are pretty much the same at the end. <br> Just make sure that you're **not** getting the ones for a V6 or a volcano heater block! You can also diffenrentiate them by already looking at the shape: the wrong ones for the V6 are more flat on one side, the *correct ones* for the V5 are more *cubic* as you can see at the pictures above.  
  
---  
  
## Thermistor & Cartridge Heater
The **thermistor** which is used is a capsuled NTC 100k. The diameter is 3mm, the length should be minimum 6mm as that is the depth of the hole in the heater block and the length of the wire is about 150cm.  
Based on the setting of the firmware it's an ATC Semitec 104GT-2/104NT-4-R025H42G (4.7k pullup). You should be able to find and use a compatible item from the aftermarket (which I successfully did - you just have to pay attention to the wire length actually).  
The following picture shows the thermistor from the aftermarket I used and the specific plug which is necessary to fit in the belonging socket at the mainboard.  
  
![Thermistor and plug](../assets/images/head_plug-therm_web.jpg)  
  
The **cartidge heater** which is used is a 24V 40W element. The diameter is 6mm, the length of the original part is about 18mm, the length of the wire is about 150cm.  
However, a cartridge heater from the aftermarket with a length of about 21mm is just fine, it just sticks out at both sides of the heater block at the end which shouldn't be a problem. It seems that it's is a typical dimension for V5/V6 heater blocks. The following picture shows the original part on the left side and a compatible part from the aftermarket I used at the right side.  
  
![Cartridge heaters](../assets/images/head_cart-heater_web.jpg)  
  
The following picture shows the specific plug which is necessary to fit into the socket at the mainboard.  

![Specific plug of the cartridge heater](../assets/images/head_cart-plug_web.jpg)
  

!!! warning  

    If you need to replace the thermistor and/or the cartridge heater, *make sure you don't overtighten the screws as it could harm both the thermistor and the heater cartridge!* Note the dent from the screw and the deformed thermistor due to an overtightened screw from the manufacturer at my **Neo**. <br> ![Deformed thermistor due to an overtightened screw](../assets/images/head_therm-cart-broken_web.jpg)    
   
??? tip "General Tips" 

    - If you need to install a new thermistor and/or cartridge heater, you have to unstrip the wires from the cable conduit. You can just unroll the conduit, pull out the wires from the old part while tugging in the wires of the new part. Be careful to not pull too hard to not harm any thin wires which might be wrapped around the wires of the old part. <br> ![Stripping in the new wires](../assets/images/stripping_in_wires_web.jpg)    
    - When installing the parts at the heater block and putting back on the plastic cap of the printhead, I personally avoided to bend the thin wires as it was done within the original installation. I just guided the wires along outside the plastic cover. By doing so, you minimize the risk of getting a shortcut due to a harmed or melted wire isolation at the part where the wires are bent and twisted originally. The following picture shows my new installed thermistor and cartridge heater with the wires running outside of the plastic cap. <br> ![Wires running outside of the plastic cap](../assets/images/head_neo_new-sen-therm_web.jpg)  

??? tip "Execute PID Tuning"      
    
    After successful installation of the new thermistor and/or cartridge heater, execute a PID tuning using e.g. Octoprint!  
  
---  
  
## Nozzle
Anycubic ships the printheads with a 0.4mm **E3D V6 type** brass nozzle for 1.75mm filament.  
  
![E3D nozzle](../assets/images/head_nozzle-e3d_web.jpg)  

So if you're looking for replacement nozzles, make sure to get yourself the correct type!  
I highly recommend to only use high quality nozzles, like the [**original E3D V6 nozzles**](https://e3d-online.com/products/v6-nozzles) (see the infobox below as well)!  
    
!!! warning  

    - *Be careful to NOT touch and harm the wires and contacts of the thermistor and the heating cartridge with at brass brush or the wrench!* <br> You may either harm the insulation, break the wire or even cause a shortcut which can result in a broken mainboard once you powered the printer up again. 
    - If you want to change the nozzle (*check out the expandable admonition below!*) and need to grab the heater block with a wrench, make sure you really just grab the heater block and never get any wires up in between - preferably grab the heater block from that sides where the wires don't come out.   
    - If you want to clean the nozzle using a brass brush for example, *never* do it when the printer is powered up and the heating process of the extruder is in progress to avoid causing a shortcut by touching the contacs with the brush.  
    - *Make sure you DON'T turn the heater block!* In case you want to change the nozzle, you don't want to loosen the heater block from the hotend, so just hold the heater block in place without turning it.     
    - *Don't do cold pulls for cleaning a nozzle when using any kind of coated nozzles!* This also involves hardened steel nozzles! Referring to the manufacturers, the coating might be harmed when doing so.   
    
??? info "About Nozzles In General" 

    - *Do yourself a favour and don't buy those cheap brass nozzles where you'll get a dozen of them for a few bucks.* It's just not worth it.  
    Remember that the nozzle is pretty much the most crucial part when it comes down to printing and achieving good results, as it's the last link in the chain of the print process and puts out the filament - so go for an established manufacturer who is known for producing quality nozzles.  
      Means, avoid those cheap sets of nozzles where you get a dozen nozzles for a few bucks. Those often lack quality: the bore might be off-center and/or might have a burr (which leads to heavy stringing), the thread might not be precise (which leads to leaking) and so on.  
      I personally only use [**original E3D V6 nozzles**](https://e3d-online.com/products/v6-nozzles). Yes, they are a bit more expensive than the super cheap ones, but it's still a good price and it's really worth it - they last longer, they're precisely made and you'll get much better results. As long as you don't want to print special abrasive filaments, you're always good with the standard E3D V6 brass nozzles.  
  
    - If you want to print filaments that are more abrasive, you probably want to go with nozzles made from plated copper, stainless or hardened steel, ruby sapphire nozzles and so on. Check out the web for further and more specific information about what to choose.  
      Be aware of the fact though, that the manufacturers *clearly advise against doing cold pulls with any kind of coated nozzles*! This also involves hardened steel nozzles! Referring to them, the coating might be harmed when doing so.  
    
    - When it comes down to choose the right nozzle size, it all depends on what you want to print and how detailed it should be. The standard size of 0.4mm the printers come with is a good starting point.  
      However, you may find yourself in the situation that you want to print more detailed objects or objects which should be more sturdy or where it doesn't matter if the surface doesn't look as clean and flat as possible, so you probably should adjust the size and switch to a smaller oder bigger diameter like 0.2-0.3mm for high detailed objects and 0.6mm for the 'rougher' prints.   
      Keep in mind though that the printing time usually increases by choosing a smaller diameter and it decreases when you're using a bigger diameter.  
      The printing time as well as the quality also depends on the [layer height](../calibration.md#layer-height) you're using, so by choosing a smaller layer height you can also get detailed and great looking prints with a 0.6mm nozzle.  
      Last but not least a smaller nozzle bore is more likely to clog and some filaments even have a sticker on the spool saying that e.g. it should be printed with minimum a 0.4mm nozzle. So choose wisely if you really want to use a nozzle with a 0.2mm bore for example.  
      Search the web for more specific information about finding and choosing the right nozzle size for your project. You may want to start with this article from [All3DP: The Best 3D Printer Nozzle Types, Sizes & Materials](https://www.all3dp.com/2/3d-printer-nozzle-size-material-what-to-know-which-to-buy). 
  
    - In case you're using *Cura* as a slicer, make sure you update to the current version v5.x (Note: It doesn't run at Ubuntu versions below 20.x though) as it uses the new Arachne engine and offers better quality as a result of that. In case you never heard of that, I recommend to watch the following videos from [Thomas Sanladerer](https://www.youtube.com/channel/UCb8Rde3uRL1ohROUVg46h1A) or read the articles at his page [https://toms3d.org/](https://toms3d.org/) where he shows the result of using a 0.6mm nozzle with Cura v5.x comparing to a 0.4 nozzle using Cura 4.x (SPOILER: you barely can see a difference).  
  
        - [Video: 0.4mm nozzles just became obsolete](https://www.youtube.com/watch?v=WgXM2zPusXo)  
          [Article: 0.4mm nozzles just became obsolete](https://toms3d.org/2022/07/28/arachne-in-prusaslicer-0-4mm-nozzles-just-became-obsolete/)  
        - [Video: Get the benefits of a 0.6mm nozzle with a 0.4?](https://www.youtube.com/watch?v=nmigF5qyJ4M)  
          [Article: Get the benefits of a 0.6mm nozzle with a 0.4?](https://toms3d.org/2022/09/22/get-the-benefits-of-a-0-6mm-nozzle-with-a-0-4/)  
  
  
  
---  
  
### Cleaning The Nozzle
If you need to clean the nozzle during the printing procedure to take off excessive amount of melted filament or if the nozzle is clogged, mind the warnings from above and check out the following steps in the expandable block below.  
  
However, keep in mind that nozzles are consumables though, they won't last forever. So get yourself some good quality nozzles right away so that you can easily replace a nozzle which is too clogged or where the tip may already be harmed.  
A harmed tip or worn out nozzle may also cause artefacts like stringing for example, so also keep that in mind if you suddenly see yourself confronted with weird and unexplainable printing behavior (in terms of quality).  

!!! warning  

    *Don't do cold pulls for cleaning a nozzle when using any kind of coated nozzles!* This also involves hardened steel nozzles! Referring to the manufacturers, the coating might be harmed when doing so.  
    
  
??? example "Cleaning The Nozzle"

    - For cleaning the nozzle and getting rid of excessive filament during the printing process or right before printing starts as the extruder is heating up, you can use a long and thin wooden stick like a skewer. A wooden toothpick also works fine - just make sure you don't burn yourself as it may be a bit short. I personally use these long pipe cleaners which have this kinda cotton stuff all around them. It doesn't melt when touching the hot nozzle and filament sticks great to it.  
    - Before and after each print I recommend to wipe away the melted filament at the nozzle with a 'cotton' pipe cleaner, a paper towel or a cloth - but *don't burn yourself!* This procedure keeps the nozzle clean and the rest of the filament won't burn black onto the brass which makes it hard to remove later.   
    - If the nozzle is already too smeared and has too much filament burnt onto the surface to be cleaned with a paper towel, you can use a small brass brush. Be careful though to not harm the tip of the nozzle by scrubbing too hard across it! Be careful to *not* touch any wires or contacts during brushing at it may cause a shortcut and blow off your mainboard! So I'd suggest you heat up the nozzle and then turn off the printer before starting to brush.  
    - If the nozzle is clogged, using a needle with the correct diameter to stick it into the hot nozzle for cleaning it sometimes works. Just stick in in the heatened up nozzle and poke around. Be careful to not harm the tip of the nozzle though!  
    - You can also use certain filament which is made for cleaning. You load it and let it run through. 
    - If the nozzle is clogged and therefore the cleaning filament can't run through, you could also try to do a *"cold pull"*. To do so you heat up the nozzle to about 220°C, load the cleaning filament and manually push it through a bit. Then let the nozzle cool down to about 90-100°C and rip out the filament. You may have to repeat this procedure a few times until the cleaning filament can run through again. However, be careful not to rip off the filament by doing the cold pull as you then definitely have to disassemble the hotend.  
      *Attention: don't do cold pulls when using any kind of coated nozzles! This also involves hardened steel nozzles! The manufacturers say that it might harm the coating of the inside of the nozzle!* 
    - If you still encounter problems with the flow of the filament though or if you even can't load new filament, most likely the little PTFE tube inside of the heatbreak is clogged. Scroll down to the "Disassembling" section where you'll find a little guide about how to get it out and clean it.  
    - If you took out the nozzle from the heater block and can't get it clean, heat it up with a hot air gun. Then you can poke out the soft filament. You can also try to put it in acetone and let it sit there - the longer the better (I'd say minimum 24hrs). This method works especially great with ABS as that just dissolves, but it also works at least a bit with other types of filament like PLA (although not as good as with ABS at all) and makes it a bit softer. Then you can try to poke the filament out. This also works with the heater block and the heatbreak if you want to clean them also. Make sure to rinse them with water before installing though.  
  
---  
       
### Changing The Nozzle
If you need to change the nozzle, mind the warnings from above and check out the following steps in the expandable block below.
     
!!! warning  
        
    - ***Never try to unscrew the nozzle from the heater block while the parts are cold!*** <br> Melted filament or some kind of screw lock glue will make it hard or even impossible to unscrew it and you risk to shear off the nozzle!  
    - Make sure you're holding the heater block tight to avoid *any* movement and don't overtighten the nozzle when installing it! <br> Reddit user [I_Sells_Drugs](https://www.reddit.com/user/I_Sells_Drugs/) was so kind to allow me to show pictures of [his attempt to tighten up the nozzle even more](https://www.reddit.com/r/anycubic/comments/10rf58m/does_this_mean_i_need_to_replace_entire_hotend/) as he got irritated by the little gap between the head of the nozzle and the heater block. He managed to shear off the heatbreak from the heater block as the following picture shows. <br> ![sheared off heatbreak](../assets/images/sheared-off-heatbreak_web.jpg)      
     
??? example "Changing The Nozzle"  

    - If you just want to change the nozzle, take off the silicone sock of the heater block, then *heat up the extruder first* about 5-10°C above your regular printing temperature and pull back the filament a bit once it's warm enough. 
    - Once the extruder heated up, let it sit at that temperature for about a minute or two to make sure that even the last amount of filament which might stick somewhere in the gaps or the thread is melted. 
    - Then *turn off the printer* and ideally unplug it from the power outlet. Don't fiddle around while it's turned on - in case you slip with the wrench and harm the wires you could create a shortcut which most likely will blow something up of your mainboard.  
    - Then grab the heater block with a wrench to hold it in place and screw out the nozzle carefully. Use a sufficient tool like a wrench or a socket wrench for the nozzle - don't use a pair of pliers as it may/will round off the screw nut. 
    - Make sure you don't turn the heater block at all to not loosen it from the heat break! Just hold it in place.
    - If the nozzle won't come loose, heat up the extruder again, raise the temperature a bit and let it sit longer to melt the filament in the gaps which seems to block. Before trying to unscrew the nozzle, switch off the printer again. <br> If that still doesn't work, you could take a piece of damp cloth and hold it against the nozzle (*not* the heater block, *only the nozzle*!) for a moment to cool it down. Due to the sudden decrease of temperature the metal of the nozzle will contract a tiny bit which may result in being able to unscrew it.  
    - For installing the new nozzle, screw it in and turn it back about one rotation once you feel it hits the heatbreak. I personally do this after everything cooled down until it's safe to touch because then I can screw in the nozzle by hand and therefore I can feel right at the start if it doesn't sit correctly.
    - Check if you didn't harm any wires! 
    - If everything is fine, power up the printer and heat up the extruder again. Most nozzle manufacturers say that you should heat it up to about 250°C, but that might already harm the PTFE tube. So go with 230-240°.  
    - Then carefully tighten up the nozzle, but don't overtighten it though. However, you need to make sure that it's tight enough (about 1.5NM) and that it really touches the heatbreak! There shouldn't be any gap between the heatbreak and the nozzle inside of the heater block!  
    - Don't get irritated by the fact that there's a little gap between the head of the nozzle and the heater block oncce you installed everything correctly - that's totally fine and it's supposed to be like that as the following picture shows. <br> ![Mounted nozzle](../assets/images/head_nozzle-mounted_web.jpg)     
             
---  
  
## Disassembling
  
Disassembling the printhead isn't really complicated. Just make sure you're careful and put the screws in a place and order that makes it easy for you to reassemble everything later. The following steps are just a rough guide through so that you know what you'll be confrontated with. I'd recommend to take a picture of each step, so that you can look at them later when reassembling - just in case you don't know how to proceed at a certain point or if you're not sure where certain screws belong.    
  
!!! warning  

    - If you need to disassemble the printhead for e.g. changing the hotend, *unload the filament first!* 
    - For changing the nozzle or disassembling the heatbreak from the heater block, you have to *heat up the parts first!* <br> The main reason for that is to melt the filament which most likely entered little gaps there. Usually it's said that it should be around 200°C but that's probably not sufficient because (in my opinion) it depends on the material of the filament. So my suggestion is to heat up the extruder about 5-10°C more than the temperature you're printing with, then you should be on the safe side. <br> So either do that using the pre-heat function of the printer or by using a sufficient heat gut. However - don't burn yourself by touching the hot metal parts!
    - Before starting to tinker *turn off the printer* and *unplug it from the power outlet!*
    - *Use the sufficient tools!* <br> So please don't try to loosen the nozzle with a pair of pliers for example, use e.g. a wrench for that. <br> I also strongly recommend to *not* use a pair of pliers for the heater block, also for that you should use a wrench (if you don't have one of that size, use an adjustable one). A wrench has a smooth surface and therefore won't scratch the surface or even put dents into the block.  
    - Make sure you *don't lose a screw* and make sure you'll *know where the screws belong* later when you want to reassemble everything again. <br> You might will be able to remember the belonging screws and positions if your tinkering lasts only an hour, but if anything crosses your plan and therefore you have to pause tinkering, you maybe won't remember one week later. So maybe start sorting the screws and take notes where they belong and/or take pictures right away from the start.
    - *Be patient and careful.* Generally speaking, if you unscrew something and it doesn't come off easy, don't start pulling too hard as you might have overseen a screw or clip, so better watch twice. 
    - *Don't harm or rip off any wires* as it may cause severe damage to your mainboard or might be complicated to fix later on.  
  
---  
    
### Take Off The Plastic Cover 

#### Go
Whatever you want to do, like if you want to change the hotend, the heater block, the heatbreak, a fan or even want to disassemble the whole feeder system, you have to remove the plastic cover of the printhead first.  
It's secured by two hexagon socket screws at the top of the metal back plate and a plastic clip at each side at the lower bottom. Be gentle and careful to not break one of the clips - the best way to get them out of their fittings is to gently push together the whole plastic cover at the bottom sides.   
  
After the plastic cover is gone, you can see the fan and the fanduct inside the plastic cover, the proximity sensor at the left side, the aluminum cooling element of the hotend/heatbreak in the middle and the heater block down at the bottom.
  
![Head no cover](../assets/images/head_go_no-cover_web.jpg)   
  
---  
    
#### Neo
Whatever you want to do, like if you want to change the hotend, the heater block, the heatbreak, a fan or even want to disassemble the whole feeder system, you have to remove the plastic cover of the printhead first.  
It's secured by two hexagon socket screws at the top of the metal back plate and a plastic clip at each side at the lower bottom as you can see at the following picture (well, you don't really see the plastic clip though but you can see the belonging notch of one of them). Be gentle and careful to not break one of the clips - the best way to get them out of their fittings is to gently push together the whole plastic cover at the bottom sides.  
  
![Backside view of the head with mounted plastic cover](../assets/images/head_neo_complete_backside_marked_web.jpg)  
  
After the plastic cover is gone, you can see the fans, the proximity sensor at the right side and the heater block at center down at the bottom and so on. Depending on what you want do do now, you need to follow different steps. But first let's have a look at the coverless head from different points of view, starting with the view from the front with a straight look at the little fan for cooling the printed part.  
  
![Front side view](../assets/images/head_dis-front_web.jpg) 
![Fan parts](../assets/images/head_neo_fan-parts_web.jpg)  
  
Now we look at the left side where you can see the motor of the feeder gear. You can spot three hexagon socket screws there - two at the top and one at the bottom close to the motor housing, which are holding the entire feeder system onto the metal backplate.    
  
![Left side view](../assets/images/head_neo_leftside_motor_mount_marked_web.jpg)
  
From the right side view you see the fan for cooling the heatsink and the ABL sensor with the orange tip at the very right side of the construction.    
  
![Right side view](../assets/images/head_rightside_web.jpg) 
![Fan heatsink](../assets/images/head_neo_fan-heatsink_web.jpg)
  
Looking at the head from the bottom right side, you can see the fan outlet on the left, the hotend with the stock silicone sock and the orange tip of the ABL sensor.    
  
![Bottom right side view](../assets/images/head_bottom-view_web.jpg)   
The following picture shows the whole metal plate where the feeder construction (the marked tips of the three screws on the right side) and the bracket of the ABL sensor (the two marked screws on the left side) is mounted onto - I took these pictures when the head wasn't mounted to the carrier of the x-axis so you can have a better look at the deatails.   
  
![Backside view metal plate](../assets/images/head_neo_backplate_marked_web.jpg)
  
---

### Disassembling The Hotend
If you need to dismount the hotend from the printhead to change it or if you need to disassemble it, check out the following steps for your specific model first to get an idea about how to proceed. 

!!! warning  

    - When pulling out the hotend at the **Neo**, *make sure the PTFE tube placed in the heatbreak comes out, too!*  
    - Inspect the PTFE tube if it's burned, deformed  or clogged - if so, get a new one as a replacement (I'd recommend using a Capricorn bowden tube). Make sure the filament runs through the tube nice and easy and without any friction.   
    - When pulling out the hotend, *be careful to not break any wires or rip them off from the sensor and heater catridge* - so better unscrew the tiny hex screws a bit and take out the thermistor and the heating cartridge first as mentioned above. 
    - Check the wires and contacts if they aren't harmed and if everything is ok. 
    - ***Never try to unscrew the heatbreak and/or the nozzle from the heater block while the parts are cold!*** 
      Melted filament or some kind of screw lock glue might make it hard or even impossible to unscrew these parts and you risk to shear them off!  

!!! danger  

    *If you can see bare wire shining through the isolation of the wires of either the thermistor or the cartridge heater, I'd strongly recommend to replace the component to not risk a shortcut and therefore a broken mainboard!*   
  
---  
  
#### Go
 
- When you look at the hotend, you'll see two bigger hexagon socket screws at the top left and right corner of the cooling element and two tiny hexagon grub screws at the lower end. <br> ![Screws](../assets/images/head_go_hotend-screws_web.jpg)
- Before you start to disassemble it though, take out the thermistor and the cartridge heater of the heater block first by loosening the two tiny grub screws. <br> ![Screws heater block](../assets/images/head_block-screws-close_web.jpg) <br> Be careful to not rip any wires!  
- The two bigger screws at the top are holding the cooling element and therefore the whole hotend in place.  then unscrew the two bigger hexagon socket screws at the top of the cooling element and you can take the hotend away from the metal plate. <br> ![Hotend dismounted](../assets/images/head_go_extruder-dismounted_web.jpg)
- If you want to change the hotend, the heatbreak or the heater block now, unscrew the nut at the top of the cooling element where the long PTFE tube runs through that leads the filament. Then loosen the two tiny hex grub screws just a little bit until you can pull out the heatbreak from the cooling element. <br> ![Extruder disassembled](../assets/images/head_go_hotend-dis_web.jpg) <br> For any further steps of disassembling (taking out the nozzle or the heatbreak from the heater block), **heat up the metal parts** by using a heat gun for example and then unscrew the heatbreak and/or from the heater block. Make sure to neither harm any parts while using the wrench nor yourself by accidentally touching the hot material.  
  
---  
    
#### Neo

- Before you start to disassemble the hotend, take out the thermistor and the cartridge heater of the heater block first by loosening the two tiny grub screws. <br> ![Screws heater block](../assets/images/head_block-screws-close_web.jpg) <br> Be careful to not rip any wires!  
- First you have to disassemble the fan on the right side by taking out the two hexagon socket screws at the top and bottom of the fan frame. <br> ![Disassemble the fan on the right side](../assets/images/head_neo_rightside_marked_web.jpg)  
- Then you'll see two hexagon socket screws at the side which are holding the hotend - loosen them until you can gently pull out the hotend. <br> ![Loosen the screws to take out the hotend](../assets/images/head_neo_vent-dis-extruder_web.jpg) <br> You could've seen the heads of the screws already earlier before disassembling the fan, but you wouldn't have been able to reach them as the following picture shows. <br> ![Closeup of the screws which you want to reach](../assets/images/head_hotend-screws_closeup_web.jpg)  
- If you want to change the the heatbreak, the nozzle or the heater block now, take out the PTFE tube from the heatbreak first. Then **heat up the metal parts** by using a heat gun for example and unscrew the heatbreak and/or the nozzle from the heater block. Make sure to neither harm any parts while using the wrench nor yourself by accidentally touching the hot material.  
  
  
---

### Dismounting The ABL Sensor

If you need to dismount the ABL sensor from the printhead to change it, check out the following steps for your specific model first to get an idea about how to proceed.  
  
---  
  
#### Go

- If you want to change the ABL sensor, you probably have to completely dismount the bracket/clamp that holds the sensor from the metal backplate. I'm not really sure about it as I didn't do it myself yet, but if the bracket is shaped like a U then that should be the way to go. Here you can see the two screws that hold it in place, looking at the metal plate from the back. <br> ![Screws at the back](../assets/images/head_go_abl-mount-back_web.jpg)  
- After reassembling the sensor, make sure to level it.  
  
---  
    
#### Neo

- If you want to change the ABL sensor, it's advisable first to take off the whole printhead from the carriage of the x-axis by taking out the four hexagon socket screws at the back that hold the plate. 
- Then loosen the two hexagon socket screws at the backplate which holds the plastic bracket in place (where the ABL sensor sits in). They are located at the left side of the back plate if you look at it from the back (see pictures above). The following picture shows the screws from a side view angle to give you a better impression about the location. At the bottom you see one of the little plastic clips - there are two of them on each side. <br> ![Screws for the ABL sensor on the left side](../assets/images/head_neo_ABL-sensor_screws_marked_web.jpg)
- The bracket itself is designed as a sledge which can be adjusted by turning the M2 hexagon socket screw at the very top of this construction as you can see at the following picture. <br> ![Screw at the top to move the sledge](../assets/images/head_ABL-sensor_top_closeup_web.jpg) 
- Be careful when you want to take out the sensor from the plastic bracket and therefore have to release the tiny plastic clips which close the bracket - don't break them! <br> ![image](../assets/images/head_ABL-sensor_clip_closeup_web.jpg) 
- The following picture shows once again the two plastic clips on one side - they're on both sides, but it's sufficient to unclip them at one side as the other side will come loose as well then. Just be careful when you unclip one side and move the top of the bracket as it's still clipped in at the other side, so don't be rough here. <br> Now you can replace the sensor or readjust the position in the bracket. Be aware that there is something like a tiny thread on the little plastic lip located towards the lower end of this lid of the bracket (see red mark on the picture to the right) - make sure this thread fits into the thread of the sensor. If everything sits just right you don't need much pressure to close the lid, so be aware and careful here to not break anything. <br> ![ABL sensor disassembled](../assets/images/ABL_sensor-dissambled_web.jpg)          
- After reassembling the sensor, make sure to level it.
  
---

### Disassembling The Feeder Gear

If you need to disassemble the feeder gear system, check out the following steps for your specific model first to get an idea about how to proceed.  
  
---  
  
#### Go
Sorry, no description available yet..
  
---  
  
#### Neo

- In case you dropped something tiny like a screw or so in the wholes at the top of the feeder or if you need to check the feeder gear system due to problems, it's probably sufficient to disassemble the system from the metal backplate by taking out the three hexagon socket screws and shake the whole thing around a bit. There are enough holes and openings at the back where you also could try to reach the lost thing using a pair of tweezers. If that doesn't work, proceed with the next step.   
- There is a metal part with cooling fins underneath the 'big' fan at the right side, this is the heatsink. <br> ![Metal plate with cooling fins](../assets/images/head_neo_cooling-fins_web.jpg) <br> This heatsink is secured by three screws as you can see at the following picture. <br> ![The three screws holding the metal plate](../assets/images/head_neo_screws-cooling-plate_marked_web.jpg) <br> If you unscrew those three hexagon socket screws and take the heatsink off, you can get a closer look at the gears of the feeder system. <br> ![Neo feeder gear system](../assets/images/head_neo_feeder-inside_web.jpg)  
  
---  
  
## Reassembling

For reassembling, just put everything back together by proceeding the steps of disassemblingin in reverse. Make sure you're using the right screws and don't forget any of them.  
Don't overtighten the screws though - as my father (R.I.P.) used to say: "After tight comes loose!" (roughly translated ;) ).  
<!---  
However, you might also want to have a look at some steps I mentioned in the expandable box below.  
-->

!!! warning "Attention"

    - If you dismounted the hotend and/or the ABL sensor, make sure to level the ABL sensor again and control your Z offset!  
    - If you replaced the hotend/heater block and/or changed the thermistor and/or the cartridge heater, execute a PID tuning!  

<!---
#### Go  
  
??? example "Reassembling The Hotend" 
  
    1. Screw the heatbreak into the heater block in the corresponding depth and screw in the nozzle from the other side until they touch. Don't tighten up the nozzle yet!    
    2. Put back the cleaned or renewed PTFE tube into the heatsink element, let the tube stick out about 5cm at the bottom, don't tighten up the nut yet.  
    3. Then push the heatbreak back into the heatsink part - make sure you push it deep enough until the little 'ring' of the heatbreak touches the heatsink part. The PTFE tube should touch the bottom of the heatbreak - because you let it stick out more than necessary, it should therefore come up a bit out of the cooling element at the top.
    4. Watch out to put the hotend in place the right way: the 'bigger' part of the heater block should be located at the front. Everything should be aligned. 
    5. Then tighten up the tiny grub screws to secure the heatbreak, so that the hotend doesn't turn or wiggle anymore (but don't overtighten the screws though). Tighten up the nut of the PTFE tube then.
    6. Mount the whole hotend/cooling element back on the metal plate by using the two bigger hexagon socket screws.  
    7. Put the thermistor and the heater cartridge back in place and secure them by *carefully* tighten the tiny hex screw - *don't overtighten them as you could harm the thermistor and the heater cartridge!*  
    8. Reassemble the fan and the plastic cover.   
    
#### Neo

??? example "Reassembling" 
  
    1. Warm up the parts using e.g. a heat gun and screw the heatbreak into the heater block until it sits tight.  
    2. Put back the cleaned or renewed PTFE tube.  
    3. Put the thermistor and the heater cartridge back in place and secure them by *carefully* tighten the tiny hex screw - *don't overtighten them as you could harm the thermistor and the heater cartridge!*  
    4. Then push the heatbreak back into the specific hole of the heatsink - make sure you push it deep enough (I personally push it as far into it as it goes).  
    5. Turn the hotend so that the wires which are coming from the heater block are hanging freely and aren't bent too much.  
    6. Then tighten up the two hexagon socket screws at the heatsink which hold the heatbreak in place, so that the hotend doesn't turn or wiggle anymore (but don't overtighten the screws though).  
    7. Reassemble the fan and the plastic cover.   
-->

---  
  
## Mods

In the following I'll list some mods I found which belong to the part "printhead" somehow. I won't put them in a special order, so you'd have to got through the list I guess. 
  
---  
  
### Go  
  
- Reddit member [xpeng121](https://www.reddit.com/user/xpeng121/) posted his modification for the Kobra **Go** to a ***direct drive extruder***: [Kobra Go direct drive mod. Yes it's Neo now...](https://www.reddit.com/r/anycubic/comments/10howol/kobra_go_direct_drive_mod_yes_its_neo_now/)  
- [MW-Mechanical](https://www.printables.com/de/social/455820-mw-mechanical) created an [Upgraded fan duct (exposed print head setup) for Anycubic Kobra Go](https://www.printables.com/de/model/338244-upgraded-fan-duct-exposed-print-head-setup-for-any) which is supposed to achieve better part cooling.
- [Gallapagos](https://www.thingiverse.com/gallapagos/designs) created a [Monomonster](https://www.thingiverse.com/thing:5741047) for the **Go** using a 5015 style blower fan.
  
---  
    
### Neo  
  
- [Martin](https://www.printables.com/de/social/443043-martin) created a [replacement for the stock fan duct ](https://www.printables.com/de/model/378928-anycubic-kobra-neo-fan-duct) of the **Neo** which is supposed to achieve better part cooling due to air flow from three sides.  
  He also created a [fan duct for a 5015 radial fan](https://www.printables.com/en/model/426167-kobra-neo-fan-duct-for-5015-fan/files) which replaces the stock parts.  
- [Gregg Bennett](https://www.printables.com/de/social/221278-greg-bennett/about) created an [extension for the stock fan duct](https://www.printables.com/de/model/399159-air-duct-anycubic-kobra-neo-httpsyoutubeso7tb6e8yh) of the **Neo** which has to be mounted onto it and leads the airflow closer to the printed object underneath the nozzle.    
  
