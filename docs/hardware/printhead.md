<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Printhead
The printheads of the **Go** and the **Neo** aren't identical because of the different type of extruder they're using:  

- the **Go** uses a bowden drive feeder/extruder while 
- the **Neo** is using a direct drive feeder/extruder.   
  
If you look at both printheads from the front and compare their size, you'll notice that the one of the **Go** is a bit smaller and more suqare than the wider and more rectangular shaped one of the **Neo**.  
  
## Go
??? question "Got a **Go**?"  

    Do you own a Kobra **Go** and want to contribute? That would be great! <br> I'd need pictures of the printhead like the ones I show here of the **Neo** for example, so people can see the difference between those two models like the shape and the position of the ABL sensor. <br> Just send me an email to <br> `3dneo (at) quantentunnel.de` <br> Thank you!    
  
## Neo  
The following picture shows a new printhead for the **Neo** as it comes as a spare part.  
  
![New Neo print head spare part](../assets/images/head_neo-spare_web.jpg)

The following picture shows a close up view of the printhead of the **Neo** from the front view. At the bottom you can see the blue silicone sock of the heater block with the nozzle in the center and the orange tip of the ABL sensor at the right side.  
  
![Neo printhead front view](../assets/images/head_neo-front_web.jpg) 
  
---

## ABL Sensor
Both printers come with a proximity sensor for automatic bed levelling (ABL) which is (afaik) the same model.  
The ABL sensor at the **Go** is mounted pretty much straight behind the heater block, where at the **Neo** it's located a few centimeters to the right side next to the heater block.  
  
!!! tip  

    Measure the original position (depth/height) of the sensor as it came with and write it down. In case you have to change the sensor or even you loosened the screw which holds it in place by accident you can always put it back in the original position, so that you don't have to deal with fiddling around to find the best position for it afterwards. 
  
### Go
??? question "Got a **Go**?"  

    Do you own a Kobra **Go** and want to contribute? That would be great! <br> I'd need pictures of the printhead from the bottom view like the one I show here of the **Neo**, so people can see where the ABL sensor is located. <br> Just send me an email to <br> `3dneo (at) quantentunnel.de` <br> Thank you!  
  
### Neo
The following picture shows the location of the ABL sensor at the printhead of the **Neo**, looking at it from a bottom view angle - the ABL sensor is the part at the right side with the round orange tip.   
  
![Orange tip of the ABL sensor at the right side](../assets/images/head_neo-bottom_web.jpg)
    
The ABL sensor itself is mounted in a plastic bracket which is the mounted to the metal backplate. You can adjust the height of the position by a little spring supported screw located at the top.  
  
![ABL sensor](../assets/images/head_ABL-sensor-front_web.jpg)
    
---  
  
## Extruder / Feeder
The **Go** uses a bowden drive extruder/feeder, while the **Neo** is using a direct drive extruder/feeder.  
If you're about to buy one of either models and you're not sure which fits you better, always go for the direct drive and get yourself the **Neo**.

### Go
  
??? question "Got a **Go**?"  

    Do you own a Kobra **Go** and want to contribute? That would be great! <br> I'd need a picture of the bowden drive feeder, so people could see the difference between the **Go** and the **Neo**. <br> Just send me an email to <br> `3dneo (at) quantentunnel.de` <br> Thank you! 
  
### Neo
The following picture shows the extruder/feeder of the **Neo** with the mounted plastic cover of the printhead.  
  
![Direct drive of the Neo](../assets/images/head_neo_directdrive_web.jpg)
  
At the top in front of the little hole where the filament is inserted you find a little lever for manual release of the tension while loading/unloading the filament. The screw in the front adjusts the pressure of the feeder gear which is brought onto the filament. The following picture shows the mechanism without the plastic cover.  
  
![Feeder top view](../assets/images/head_feeder_topview_web.jpg)
  
!!! warning

    Make sure that you set the retraction distance and speed to the correct values for a direct drive! In general, it's supposed to be something around 1mm distance and probabyl around 50mm speed. If you set the distance to a value which is too high (e.g. the default 6mm for the **Go** as a bowden drive), the melted filament might be pulled back too far and reaches the PTFE tube which might get clogged then. 
  
!!! tip

    When adjusting the pressure of the feeder gear, make sure you don't tighten it up too much as it could squeeze and deform the filament. On the other hand it shouldn't be too loose though as it should transport the filament reliably. So you might want to try different settings of the tension.   
  
---  
  
## Hotend & Heatbreak
  
### Go
  
??? question "Got a **Go**?"  

    Do you own a Kobra **Go** and want to contribute? That would be great! <br> I'd need pictures of the hotend like the ones I show here of the **Neo** for example, so people can see the difference between those two models. <br> Just send me an email to <br> `3dneo (at) quantentunnel.de` <br> Thank you!  
  
### Neo  
  
The hotend of the **Neo** is shown in the following picture. Note the shape of the heatbreak as it's plugged into the belonging hole at the printhead and secured by two screws. The outer diameter of the heatbreak is 6mm(?), the inner diameter is 4mm and the total length is probably something around 2.4-2.5cm (sorry, I forgot to measure it as I had it disassambled, will do it next time though). 
  
![Hotend](../assets/images/head_neo_block-hotend-disass_web.jpg)  
  
Additionally there is a little PTFE-tube inside of it, which is about 4cm long and 4mm thick with a 2mm hole inside of it to guide the 1.75mm filament.  
  
![Hotend mounted with block and tube](../assets/images/head_neo_block-hotend-tube-used_web.jpg)    
  
!!! warning

    Too high temperatures may harm the PTFE tube - it may become deformed. 
  
??? tip "Can't Load New Filament?!"

    If you can't load new filament even though nothing seems to be sticking in there anymore, it's most likely that the little PTFE tube inside of the hotend is clogged. To clean or replace it you need to disassamble the hotend from the printhead. Scroll down to the "disassambling" section to find a little guide about how to do that.   
  
??? tip "Spare Part Hotend"

    - If you need a new hotend because your heater block or the heatbreak needs to be changed, you can get yourself the spare part hotend for the regular *Kobra*. If you look at the picture of it and compare it with the ones I've shown above, you'll notice that the shape of the heatbreak is the same. So up to me it'll fit perfectly.   
    - Besides that, the hotend for the *Kobra* comes with a cartridge heater and a thermistor which are also compatible with the ones from the **Go** and **Neo** - at least from a technical side of view. So you'd have them as a spare part also. <br> However, the wires of these parts are way too short though, so you wont't be able to connect them directly! So in case you want to install them, you probably could either just cut the plug and the old part and solder the wires together or (if you have the tools for that) crimp the specific socket for the plug to the old wire to just connect them this way. <br> *Remember to execute a PID tuning after changing the thermistor and/or the dartridge heater!*  
    - However, scroll down and check out the "disassambling" section below to see how to dis- and reassamble it. *Maybe you don't need new parts, so try to clean up everything first and reassamble it before ordering new parts right away.*
  
---  
  
## Heater Block
Both printers use an E3D V5 compatible heater block.  
Both the thermistor and the cartidge heater have to be plugged into the specific holes and should be fixed with at tiny grub screw (HEX 1.5).  
  
![Heater block V5](../assets/images/head_block-screws-close_web.jpg)  
      
---  
  
## Nozzle
Anycubic ships the printheads with a 0.4mm brass nozzle for 1.75mm filament.  
The nozzle is compatible with e.g. E3D V5/V6 nozzles as shown in the following picture.  
  
![E3D nozzle](../assets/images/head_nozzle-e3d_web.jpg)  

    
!!! warning  

    - *Be careful to NOT touch and harm the wires and contacts of the thermistor and the heating cartridge with at brass brush or the wrench!* <br> You may either harm the insulation, break the wire or even cause a shortcut which can result in a broken mainboard once you powered the printer up again. 
    - If you want to change the nozzle (*check out the expandable admonition below!*) and need to grab the heater block with a wrench, make sure you really just grab the heater block and never get any wires up in between - preferably grab the heater block from that sides where the wires don't come out.   
    - If you want to clean the nozzle using a brass brush for example, *never* do it when the printer is powered up and the heating process of the extruder is in progress to avoid causing a shortcut by touching the contacs with the brush.  
    - *Make sure you DON'T turn the heater block!* In case you want to change the nozzle, you don't want to loosen the heater block from the hotend, so just hold the heater block in place without turning it.     
    
??? tip "About Cleaning the Nozzle"

    - For cleaning the nozzle and getting rid of excessive filament during the printing process or right before printing starts as the extruder is heating up, just use a long and thin wooden stick like a skewer. A wooden toothpick also works fine - just make sure you don't burn yourself as it may be a bit short. 
    - Using a needle with the correct diameter to stick it into the hot nozzle for cleaning it sometimes works. If you still encounter problems with the flow of the filament though or if you even can't load new filament, most likely the little PTFE tube inside of the heatbreak is clogged. Scroll down to the "disassambling" section where you'll find a little guide about how to get it out and clean it.  
     
??? example "Changing the Nozzle"  

    - If you just want to change the nozzle, take off the silicone sock of the heater block, then *heat up the extruder first* about 5-10°C above your regular printing temperature and pull back the filament a bit once it's warm enough. 
    - Once the extruder heated up, let it sit at that temperature for about a minute or two to make sure that even the last amount of filament which might stick somewhere in the gaps or the thread is melted. 
    - Then *turn off the printer* and ideally unplug it from the power outlet. Don't fiddle around while it's turned on - in case you slip with the wrench and harm the wires you could create a shortcut which most likely will blow something up of your mainboard.  
    - Then grab the heater block with a wrench to hold it in place and screw out the nozzle carefully. Use a sufficient tool like a wrench or a socket wrench for the nozzle - don't use a pair of pliers as it may/will round off the screw nut. 
    - Make sure you don't turn the heater block at all to not loosen it from the heat break! Just hold it in place.
    - If the nozzle won't come loose, heat up the extruder again, raise the temperature a bit and let it sit longer to melt the filament in the gaps which seems to block. Before trying to unscrew the nozzle, switch off the printer again. <br> If that still doesn't work, you could take a peace of damp cloth and hold it against the nozzle (*not* the heater block, *only the nozzle*!) for a moment to cool it down. Due to the sudden decrease of temperature the metal of the nozzle will contract a tiny bit which may result in being able to unscrew it.  
    - For installing the new nozzle, screw it in and turn it back about one rotation once you feel it hits the hotend. I personally do this after everything cooled down until it's safe to touch because then I can screw in the nozzle by hand and therefore I can feel right at the start if it doesn't sit correctly. 
    - Check if you didn't harm any wires! 
    - If everything is fine, power up the printer, heat up the extruder again and carefully tighten up the nozzle (don't overtighten it though). 
    - Don't get irritated by the fact that there's a little gap between the head of the nozzle and the heater block - that's totally fine and it's supposed to be like that as the following picture shows. <br> ![Mounted nozzle](../assets/images/head_nozzle-mounted_web.jpg)     
    
        !!! warning  
        
            ***Never try to unscrew the nozzle from the heater block while the parts are cold!*** <br> Melted filament or some kind of screw lock glue will make it hard or even impossible to unscrew it and you risk to shear off the nozzle!  
     
??? info "About Nozzles in General" 

    - When it comes down to choose the right nozzle size, it all depends on what you want to print and how detailed it should be. The standard size of 0.4mm the printers come with is a good starting point. <br> However, you may find yourself in the situation that you want to print more detailed objects or objects which should be more sturdy or where it doesn't matter if the surface doesn't look as clean and flat as possible, so you probably should adjust the size and switch to a smaller oder bigger diameter like 0.2-0.3mm for detailed objects and 0.6mm for the 'rougher' prints. <br> Keep in mind though that the printing time usually increases by choosing a smaller diameter and it decreases when you're using a bigger diameter due to the smaller/larger layer height that is possible to print. <br> Search the web for more specific informations about finding and choosing the right nozzle size for your project.  
  
    - In case you're using *Cura* as a slicer, make sure you update to the current version v5.x (Note: It doesn't run at Ubuntu versions below 20.x though) as it uses the new Arachne engine and offers better quality as a result of that. In case you never heard of that, I recommend to watch the following videos from [Thomas Sanladerer](https://www.youtube.com/channel/UCb8Rde3uRL1ohROUVg46h1A) or read the articles at his page [https://toms3d.org/](https://toms3d.org/) where he shows the result of using a 0.6mm nozzle with Cura v5.x comparing to a 0.4 nozzle using Cura 4.x (SPOILER: you barely can see a difference).  
  
        - [Video: 0.4mm nozzles just became obsolete](https://www.youtube.com/watch?v=WgXM2zPusXo)  
          [Article: 0.4mm nozzles just became obsolete](https://toms3d.org/2022/07/28/arachne-in-prusaslicer-0-4mm-nozzles-just-became-obsolete/)  
        - [Video: Get the benefits of a 0.6mm nozzle with a 0.4?](https://www.youtube.com/watch?v=nmigF5qyJ4M)  
          [Article: Get the benefits of a 0.6mm nozzle with a 0.4?](https://toms3d.org/2022/09/22/get-the-benefits-of-a-0-6mm-nozzle-with-a-0-4/)  
  
    - Do yourself a favour and don't buy those cheap brass nozzles where you'll get a dozen of them for a few bucks. It's just not worth it.  
    Remember that the nozzle is pretty much the most crucial part when it comes down to printing and achieving good results, as it's the last link in the chain of the print process and puts out the filament - so go for a manufacturer who is known for quality nozzles.  
  
    - I personally use the E3D V6 brass nozzles (0.6 mm right now) for printing PLA+. Yes, they are a bit more expensive than the super cheap ones, but it's still a good price and it's really worth it - they last longer, they're precisely made and you'll get much better results. As long as you don't want to print special abrasive filaments, you're always good with these standard E3D V6 brass nozzles.  
  
    - If you want to print filaments that are more abrasive, you probably want to go with nozzles made from plated copper, stainless or hardened steel, ruby sapphire nozzles and so on. Check out the web for further and more specific informations about what to choose.  
  
---   
  
## Silicone Sock
The silicone sock isolates the heater block. Therefore it should stay in place and shouldn't come off, as it may cause the "thermal runaway" error.  
The sock which comes with the printhead isn't the best one to use (in my opinion) as it seems to come off pretty easily. There are compatible socks at the aftermarket which I personally use and which I can highly recommend. They have a bigger lip which slips over the heater block and covers a bigger area of the top than the one which comes with the printer. Therefore they stay in place much better when they heat up and become more flexible.  
The following pictures show the compatible one from the aftermarket on the left side and the stock sock on the right side.     
  
![Silicone socks top view](../assets/images/silisocks_top_web.jpg)   
  
Additionaly, they also cover and therefore isolate the base of the nozzle - something that the stock ones don't do at all.  
  
![Silicone socks bottom view](../assets/images/silisocks_bottom_web.jpg)  
  
---  
  
## Thermistor & Cartridge Heater
The *thermistor* which is used is a capsuled NTC 100k (probably "3950"). The diameter is 3mm, the length should be minimum 6mm as that is the depth of the hole in the heater block and the length of the wire is about 150cm.  
You should be able to use a compatible item from the aftermarket which fits a V5/V6 heater block, e.g. an ATC Semitec 104GT-2.  
The following picture shows the thermistor from the aftermarket I used and the specific plug which is necessary to fit in the belonging socket at the mainboard.  
  
![Thermistor and plug](../assets/images/head_plug-therm_web.jpg)  
  
The *cartidge heater* which is used is a 24V 40W element. The diameter is 6mm, the length of the original part is about 18mm, the length of the wire is about 150cm.  
However, a cartridge heater from the aftermarket with a length of about 21mm is just fine, it just sticks out at both sides of the heater block at the end which shouldn't be a problem. It seems that it's is a typical dimension for V5/V6 heater blocks. The following picture shows the original part on the left side and a compatbile part from the aftermarket I used at the right side.  
  
![Cartridge heaters](../assets/images/head_cart-heater_web.jpg)  
  
The following picture shows the specific plug which is necessary to fit into the socket at the maiboard.  

![Specific plug of the cartridge heater](../assets/images/head_cart-plug_web.jpg)
  

!!! warning info inline 

    If you need to replace the thermistor and/or the cartridge heater, *make sure you don't overtighten the screws as it could harm both the thermistor and the heater cartridge!* <br> Note the dent from the screw and the deformed thermistor due to an overtightened screw from the manufacturer at my **Neo**.  
    
![Deformed thermistor due to an overtightened screw](../assets/images/head_therm-cart-broken_web.jpg)|    
  
??? tip "General Tips" 

    - If you need to install a new thermistor and/or cartridge heater, you have to unstrip the wires from the cable conduit. You can just unroll the conduit, pull out the wires from the old part while tugging in the wires of the new part. Be careful to not pull too hard to not harm any thin wires which might be wrapped around the wires of the old part. <br> ![Stripping in the new wires](../assets/images/stripping_in_wires_web.jpg)    
  
    - When installing the parts at the heater block and putting back on the plastic cap of the printhead, I personally avoided to bend the thin wires as it was done within the original installation. I just guided the wires along outside the plastic cover. By doing so, you minimize the risk of getting a shortcut due to a harmed or melted wire isolation at the part where the wires are bent and twisted originally. The following picture shows my new installed thermistor and cartridge heater with the wires running outside of the plastic cap. <br> ![Wires running outside of the plastic cap](../assets/images/head_neo_new-sen-therm_web.jpg)  

!!! success      
    
    ***After successful installation of the new thermistor and/or cartridge heater, execute a PID tuning using e.g. Octoprint.***  
  
---  
  
## Disassambling the Printhead
  
Disassambling the printhead isn't really complicated. Just make sure you're careful and put the screws in a place and order that makes it easy for you to reassamble everything later. The following steps are just a rough guide through so that you know what you'll be confrontated with.   
  
!!! warning  

    - If you need to disassamble the printhead for e.g. changing the hotend, *unload the filament first!* 
    - For changing the nozzle or disassambling the heatbreak from the heater block, you have to *heat up the parts first!* <br> The main reason for that is to melt the filament which most likely entered little gaps there. Usually it's said that it should be around 200°C but that's probably not sufficient because (in my opinion) it depends on the material of the filament. So my suggestion is to heat up the extruder about 5-10°C more than the temperature you're printing with, then you should be on the safe side. <br> So either do that using the pre-heat function of the printer or by using a sufficient heat gut. However - don't burn yourself by touching the hot metal parts!
    - Before starting to tinker *turn off the printer* and *unplug it from the power outlet!*
    - *Use the sufficient tools!* <br> So please don't try to loosen the nozzle with a pair of pliers for example, use e.g. a wrench for that. <br> I also strongly recommend to *not* use a pair of pliers for the heater block, also for that you should use a wrench (if you don't have one of that size, use an adjustable one). A wrench has a smooth surface and therefore won't scratch the surface or even put dents into the block.  
    - Make sure you *don't lose a screw* and make sure you'll *know where the screws belong* later when you want to reassamble everything again. <br> You might will be able to remember the belonging screws and positions if your tinkering lasts only an hour, but if anything crosses your plan and therefore you have to pause tinkering, you maybe won't remember one week later. So maybe start sorting the screws and take notes where they belong and/or take pictures right away from the start.
    - *Be patient and careful.* Generally speaking, if you unscrew something and it doesn't come off easy, don't start pulling too hard as you might have overseen a screw or clip, so better watch twice. 
    - *Don't harm or rip off any wires* as it may cause severe damage to your mainboard or might be complicated to fix later on.  
  
### Go
  
??? question "Got a **Go**?"  

    Do you own a Kobra **Go** and want to contribute? That would be great! <br> I'd need pictures and a little step-by-step description of disassambling the printhead like you can see underneath for the **Neo**, so people can see the difference between those two models. <br> Just send me an email to <br> `3dneo (at) quantentunnel.de` <br> Thank you!  
  
  
### Neo  
 
Whatever you want to do, like if you want to change the hotend, the heater block, the heatbreak, a fan or even want to disassamble the whole feeder system, you have to remove the plastic cover of the printhead first.  
It's secured by two hexagon socket screws at the top of the metal back plate and a plastic clip at each side at the lower bottom as you can see at the following picture (well, you don't really see the plastic clip though but you can see the belonging notch of one of them). Be gentle and careful to not break one of the clips - the best way to get them out of their fittings is to gently push together the whole plastic cover at the bottom sides.  
  
![Backside view of the head with mounted plastic cover](../assets/images/head_neo_complete_backside_marked_web.jpg)  
  
After the plastic cover is gone, you can see the fans, the proximity sensor at the right side and the heater block at center down at the bottom and so on. Depending on what you want do do now, you need to follow different steps. But first let's have a look at the coverless head from different points of view, starting with the view from the front with a straight look at the little fan for cooling the printed part.  
  
![Front side view](../assets/images/head_dis-front_web.jpg)   
  
Now we look at the left side where you can see the motor of the feeder gear. You can spot three hexagon socket screws there - two at the top and one at the bottom close to the motor housing, which are holding the entire feeder system onto the metal backplate.    
  
![Left side view](../assets/images/head_neo_leftside_motor_mount_marked_web.jpg)
  
From the right side view you see the fan for cooling the extruder and the ABL sensor with the orange tip at the very right side of the construction.    
  
![Right side view](../assets/images/head_rightside_web.jpg) 
  
Looking at the head from the bottom right side, you can see the fan outlet on the left, the hotend with the stock silicone sock and the orange tip of the ABL sensor.    
  
![Bottom right side view](../assets/images/head_bottom-view_web.jpg)   
The following picture shows the whole metal plate where the feeder construction (the marked tips of the three screws on the right side) and the bracket of the ABL sensor (the two marked screws on the left side) is mounted onto - I took these pictures when the head wasn't mounted to the carrier of the x-axis so you can have a better look at the deatails.   
  
![Backside view metal plate](../assets/images/head_neo_backplate_marked_web.jpg)
  
??? example "Disassambling the Hotend, Heater Block and/or Heatbreak"

    - First you have to disassamble the fan on the right side by taking out the two hexagon socket screws at the top and bottom of the fan frame. <br> ![Disassamble the fan on the right side](../assets/images/head_neo_rightside_marked_web.jpg)  
    - Then you'll see two hexagon socket screws at the side which are holding the hotend - loosen them until you can gently pull out the hotend. <br> ![Loosen the screws to take out the hotend](../assets/images/head_neo_vent-dis-extruder_web.jpg) <br> You could've seen the heads of the screws already earlier before disassambling the fan, but you wouldn't have been able to reach them as the following picture shows. <br> ![Closeup of the screws which you want to reach](../assets/images/head_hotend-screws_closeup_web.jpg)  
    - If you want to change the hotend, the heatbreak or the heater block now, take out the PTFE tube from the heatbreak first. Then **heat up the metal parts** by using a heat gun for example and unscrew the hotend from the heater block. Make sure to neither harm any parts while using the wrench nor yourself by accidentally touching the hot material.  
  
    !!! warning  

        - When pulling out the hotend, *make sure the PTFE tube of the hotend comes out, too!* <br> Inspect it if it isn't clogged - if so, either clean it up carefully by e.g. using a little 2mm drill *manually by hand* or just get a new one as a replacement. Make sure the filament runs through the tube nice and easy and without any friction.   
        - When pulling out the hotend, *be careful to not break any wires or rip them off from the sensor and heater catridge* - so better unscrew the tiny hex screws a bit and take out the thermistor and the heating cartridge. 
        - Check the wires and contacts if they aren't harmed and if everything is ok. 
        - ***Never try to unscrew the heatbreak from the heater block while the parts are cold!*** <br> Melted filament or some kind of screw lock glue might make it hard or even impossible to unscrew it and you risk to shear off the heatbreak!  

    !!! danger  

        *If you can see bare wire shining through the isolation of the wires of either the thermistor or the cartridge heater I'd strongly recommend to replace the component to not risk a shortcut and therefore a broken mainboard (seriously - you don't want to get a blown off mainboard like it happened to me just because of a part which maybe costs a buck or two).*   
   

??? example "Disassambling the ABL Sensor"

    - If you want to change the ABL sensor, loosen the two hexagon socket screw at the backplate which holds the plastic bracket in place (where the ABL sensor sits in). They are located at the left side of the back plate if you look at it from the back (see pictures above). The following picture shows the screws from a side view angle to give you a better impression about the location. At the bottom you see the little plastic clip. <br> ![Screws for the ABL sensor on the left side](../assets/images/head_neo_ABL-sensor_screws_marked_web.jpg)
    - The bracket itself is designed as a slay which can be adjusted by turning the screw at the very top of this construction. *Measure and mark or note the position of the ABL sensor first before loosening anything or even taking it out of the bracket.* In case you forgot about that, the following picture of an original spare part printhead shows the position. The upper edge of the sensor is in line with the upper edge of the slay/bracket, the orange tip of the sensor at the bottom sticks out about 3.5mm of the bracket. <br> ![Screw at the top to move the slay](../assets/images/head_ABL-sensor_top_closeup_web.jpg)  
    - Be careful when you want to take out the sensor from the plastic bracket and therefore have to release the tiny plastic clips which close the bracket - don't break them! <br> ![image](../assets/images/head_ABL-sensor_clip_closeup_web.jpg)
        

??? example "Disassambling the Feeder System" 

    - I didn't disassamble the feeder system yet, so I can't really provide any specific steps or further pictures of the disassambling the feeder system itself. However, if you need to gain access to it, it migth come in handy to disassamble the metal backplate first, which is secured by three hexagon socket screws only. 
    - In case you dropped something tiny like a screw or so in the wholes at the top of the feeder, it's probably sufficient to disassamble the system from the metal backplate by taking out the three hexagon socket screws and shake the whole thing around a bit. There are enough holes and openings at the back where you also could try to reach the lost thing using a pair of tweezers. If that doesn't work, proceed with the next step.
    - There is a metal part with cooling fins underneath the 'big' fan at the right side. <br> ![Metal plate with cooling fins](../assets/images/head_neo_cooling-fins_web.jpg) <br> This metal part is secured by three screws as you can see at the following picture. <br> ![The three screws holding the metal plate](../assets/images/head_neo_screws-cooling-plate_marked_web.jpg) <br> If you unscrew those three hexagon socket screws and take that metal part off, you can get a closer look at the gears of the feeder system (you don't necessarily have to remove the fan to do so). Now you should be able to remove your lost part with some tweezers or get a closer look at the gears if anything is damaged. 
    - From what I've seen looking at the printhead while the plastic cover is taken off, you probably would have to disassamble the motor from the system if you want to go even further from here, but I can't really say anything about that right now.
      
      
  
??? example "Reassambling" 

    For reassambling, just put everything back together by reverting the beforementioned steps. Make sure you're using the right screws and don't forget any of them. Don't overtighten the screws - as my father (R.I.P.) used to say: "After tight comes loose!" (roughly translated). 
  
    1. Warm up the parts using e.g. a heat gun and screw the heatbreak into the heater block until it sits tight.  
    2. Put back the cleaned or renewed PTFE tube.  
    3. Put the thermistor and the heater cartridge back in place and secure them by *carefully* tighten the tiny hex screw - *don't overtighten them as you could harm the thermistor and the heater cartridge!*  
    4. Then push the heatbreak back into the specific hole - make sure you push it deep enough (I personally push it as far into it as it goes).  
    5. Turn the hotend so that the wires which are coming from the heater block are hanging freely and aren't bent too much.  
    6. Then tighten up the screws, so that the hotend doesn't turn or wiggle anymore (but don't overtighten the screws though).  
    7. Reassamble the fan and the plastic cover.   
  
---  
  
## Mods

### Go  
  
- Reddit member [xpeng121](https://www.reddit.com/user/xpeng121/) posted his modification for the Kobra **Go** to a direct drive extruder: [Kobra Go direct drive mod. Yes it's Neo now...](https://www.reddit.com/r/anycubic/comments/10howol/kobra_go_direct_drive_mod_yes_its_neo_now/)  
  
### Neo  
  
..
