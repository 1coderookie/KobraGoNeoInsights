<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Bed
Both of the printers have a heated and magnetic bed with the *physical* dimension of 230x230mm - even though Anycubic states in the official specs that the size is 220x220mm.  
However, if you're looking for a plate from a third party company, you need to get yourself a 230x230mm plate, otherwise it would be too small.  

The temperature of the bed should reach about ≤230°F/110°C maximum and therefore it should be possible to successfully print ABS, PETG and TPU (by using a housing though) besides PLA.  
Both printers offer a 25-point automatic bed leveling which is called "Anycubic LeviQ".  

??? tip "Bed Leveling Function"

    - Don't get misleaded by the term "automatic bed leveling" - the process does *not* level your bed! It only measures and recognizes the distance towards the sensor at the 25 spots where it measures. You can *not* level the bed itself without tinkering as it's mounted directly to the construction which leads the bed in the y-axis.    
    - When it comes to executing the ABL function of the printer, it's advisable to initially check if the ABL sensor is leveled correctly to get the best results out of the ABL process. See the expandable box "Leveling the ABL Sensor" in the section ["Leveling or Dismounting the ABL Sensor"](printhead.md#leveling-or-dismounting-the-abl-sensor) in the chapter "Printhead".  
    - To make the measured values of the ABL come into account later when it comes down to printing, you'll need to add a certain line to the start G-code of the slicer. I'm not 100% sure yet, but right now it seems like the necessary command is "M420 S1 L" which reads the data out of the EEPROM.   
      
The bed uses a removable PEI-coated spring steel plate which makes it easy to remove the printed object.  
The plate that comes with the printer is one-sided coated at the **Go** and double-sided coated at the **Neo**.   
The following picture shows the surface of the coated plate from a close-up view.  
  
![Close-up view of the PEI-coated plate](../assets/images/bed_closeup_web.jpg)  
  
When you look at the backside of the bed, you'll notice a black plastic cap which sticks out.  
  
![Bed connector](../assets/images/bed_connector_side_web.jpg)
  
Be careful to never break it by accident as it protects the wires which are soldered to the contacts of the board at the bottom side.  
  
![Soldered connections](../assets/images/bed_connection_web.jpg)
  
When you take a look underneath the bed itself, you'll spot a little foam piece secured by kapton tape - don't remove that as it protects and insulates the thermistor of the bed which is positioned underneath it.  
  
![Bed thermistor](../assets/images/bed_thermistor_web.jpg)
  
??? info "Bed Thermistor"

    As you can already conclude from looking at the picture, you can't change the thermistor of the bed as it's built into it - at least right now it appears to me like that. I might be wrong though as it might be just soldered to some contacts - to investigate that, I'd need to take off the foam piece which I refused to do so because I don't have any kapton tape yet.  
  
??? tip "Execute PID Tuning for the Bed"

    To make sure the heating algorithm can work as expected and keeps the fluctuation of the temperature as low as possible, execute a PID tuning. You can find informations about how to do that in the chapter ["PID Tuning"](../pid-tune.md).  
  
??? tip "Clean the Plate of the Bed"

    - Before starting a print, make sure the surface of the plate is clean and without any traces of oil, silicone or other stuff which avoids that the filament sticks to the surface. To clean it, use isopropyl alcohol.  
    - Already touching the plate with your fingers leads to a little amoung of grease left there which already might be enough to cause problems for your print to stick on the bed, so maybe always use disposable gloves when touching it, taking it off or repositioning it.
    - If there's a rest of filament stuck on the plate, *never* try to scratch it off with metal or other sharp materials as you don't want to harm the PEI coating. Heat up the bed and try to peel off the filament instead. If that doesn't work, take off the plate and heat up the area using your hot air gun - sooner or later you'll be able to peel it off. However, be careful to not overheat and maybe harm the coating though.  
  
  
??? tip "Level the ABL Sensor"

    It's advisable to level the ABL sensor initially, you can find informations about it in the hardware section within the chapter ["Printhead"](printhead.md#leveling-or-dismounting-the-abl-sensor).  
    
??? tip "Bed Level Visualization"

    The display of the control unit does *not* show a meshview after you proceeded the bed level function - if you'd like to see that, you'd usually have to use additional software like the beforementioned [Octoprint](https://octoprint.org/) and an additional plugin for visualization like the [Bed Level Visualizer](https://plugins.octoprint.org/plugins/bedlevelvisualizer/).  
    To get a visualization out of the data, you need to add some code though, otherwise you won't get that nice graphic you can always see everywhere. So I don't know if the following code is 100% correct or if there's anything obsolete in there or whatever, but at least I got the visualization done at the end (Thanks to reddit member [one-without-zero](https://www.reddit.com/user/one-without-zero/) for pointing out M503 to me!).  
    
    - Tab "Collection":  
        ```
        M140 S60 ; starting by heating the bed for nominal mesh accuracy 
        M117 Homing all axes ; send message to printer display 
        G28 ; home all axes 
        M420 S0 ; Turning off bed leveling while probing, if firmware is set ; to restore after G28 
        M104 S0 ;Turn-off hotend 
        M117 Heating the bed ; send message to printer display 
        M190 S60 ; waiting until the bed is fully warmed up 
        M300 S1000 P500 ; chirp to indicate bed mesh levels is initializing 
        M117 Creating the bed mesh levels ; send message to printer display 
        M155 S30 ; reduce temperature reporting rate to reduce output pollution
        @BEDLEVELVISUALIZER ; tell the plugin to watch for reported mesh 
        G29 T ; run bilinear probing 
        M155 S3 ; reset temperature reporting 
        M140 S0 ; cooling down the bed 
        M104 S0 ; cooling down extruder
        M500 ; store mesh in EEPROM 
        M503 ; report mesh values
        M300 S440 P200 ; make calibration completed tones 
        M300 S660 P250 M300 S880 P300 
        M117 Bed mesh levels completed ; send message to printer display
        ```
    - Tab "Commands", click the "+ Add" button. There you create two new command scripts: "Create mesh" and "Pull latest mesh" (you can name them however you like though).  
        "Create mesh" has the same code like at the "Collection" tab above (to be honest: I actually think this one is obsolete but because now it's working for me here and I don't want to mess around, I'll just add it here to show you my solution):  
        ```
        M140 S60 ; starting by heating the bed for nominal mesh accuracy 
        M117 Homing all axes ; send message to printer display 
        G28 ; home all axes 
        M420 S0 ; Turning off bed leveling while probing, if firmware is set ; to restore after G28 
        M104 S0 ;Turn-off hotend 
        M117 Heating the bed ; send message to printer display 
        M190 S60 ; waiting until the bed is fully warmed up 
        M300 S1000 P500 ; chirp to indicate bed mesh levels is initializing 
        M117 Creating the bed mesh levels ; send message to printer display 
        M155 S30 ; reduce temperature reporting rate to reduce output pollution
        @BEDLEVELVISUALIZER ; tell the plugin to watch for reported mesh 
        G29 T ; run bilinear probing 
        M155 S3 ; reset temperature reporting 
        M140 S0 ; cooling down the bed 
        M104 S0 ; cooling down extruder
        M500 ; store mesh in EEPROM 
        M503 ; report mesh values
        M300 S440 P200 ; make calibration completed tones 
        M300 S660 P250 M300 S880 P300 
        M117 Bed mesh levels completed ; send message to printer display
        ```
        
        "Pull latest mesh" has the following code:  
        ```
        @BEDLEVELVISUALIZER
        M420 T0
        M420 V
        ```
        
    - To create a meshview now, click on the blue info-button "Update Mesh Now". This will start the probing. After it's done, click on "Pull latest mesh" and the graphic should be rendered.  
    - To see a table with the collected data, click on the little configuration wheel again and then click on the tab "Data".  
    - Images will come soon.. ;)


??? tip "Spacers of the Bedmount"

    If you find that the bed is not as flat or trimmed as it should be, it might be a good idea to disassemble it and check the four black spacers that connect the metal y-axis gantry and the bed itself. Measure them with a slide gauge to see if they are really the same height.  
    If they're not, either look for other spacers you might be using, put the stock ones on a flat surface with sandpaper and grind them down to one length or put washers or other suitable material (e.g. gasket material) of the needed thickness under them. Then execute another ABL and compare the new values. From there you can try to get it as much trammed as possible. If that doesn't really help, check the "Mods" section below and read the part about using different types of spacers.       
            
  
??? example "Check the Screws of the Bedplate and the Gantry of the Bed"

    - Check if the screws are all tightened up. Be careful though to not overtighten the screws of the Bedplate as you may compress the little spacers underneath it and therefore the plate may become warped. On the other hand, if you see that your bed is warped somehow or that the bed is much more off in certain areas or at one side, you can check if the screws in that area might be too tightened up or too loose.  
    - Check if the bedplate itself is somehow wobbling. Not only sideways (horizontally), but also up and down (vertically). If so, not only check the v-slot wheels and maybe adjust their fitting using the eccentric nuts, also check if the screws of the gantry of the bed where the wheels are mounted to are tightened up.    
    
??? example "Tramming the Bed"

    If you added adjustable spacers like silicone spacers or springs, you'll be able to tram your bed. When you want to tram the bed by adjusting the tension of the springs or silicone spacers to pull down a side or an edge of the bed, be careful to not bend the bed itself by tightening up just one corner too much. Try to push down one side of the bed and adjust two screws at a time. Even then be careful though and keep an eye on the mesh visualizer or (if you con't have that one) on the values of the ABL.   
    
??? example "Tramming the X-Axis Gantry"  

    To make sure that the bed and the x-axis gantry are parallel to each other, you should also tram the gantry in relation to the bed itself. See the expandable box in the section [X-Axis Gantry](../axes.md/#x-axis-gantry) to read how you could do it. 
    
## Mods

### Different Spacers
Because you can't level the bed itself due to the construction, you may want to replaced the stock spacers with springs or silicone spacers which allows them to adjust the position of the bed itself. You can look out for a set of springs suitable for an Ender 3 for example, those would fit. However, you'd have to get yourself some longer M4 type screws as the stock ones will bee too short.  
Mounting springs instead of spacers which seems to be a good idea at first sight. However, as springs are made from metal which underlies the temperature changes of the heated bed, it'll most likely be necessary to check the level once in a while. You also need to make sure that the bolt can't turn itself loose due to the vibration. Another downside (imho) is, that the springs are pretty long and therefore you either have to use longer screws and/or have to tighten the screws pretty much to compress the springs. This can force warping again though as it puts more stress on the four points where the bed is mounted. So I personally would suggest to use silicone spacers of about the same length as the original spacers, but which also can be compressed a few milimeters to level the bed.  
The following picture shows the stock spacers on the left, springs in te middle and silicone spacers on the right. <br> ![Spacers](../assets/images/bed_different-spacers_web.jpg)
  
??? example "Tramming the Bed"

    However, *if* you are trying this solution, make sure the screws won't turn themselves loose due to the vibration. When you want to level the bed then by adjusting the tension of the springs or silicone spacers to pull down a side or an edge of the bed, be careful to not bend the bed itself by tightening up just one corner too much. Try to push down one side of the bed and adjust two screws at a time. Even then be careful though and keep an eye on the mesh visualizer or (if you con't have that one) on the values of the ABL.  
    
### Insulating the Bed
What I personally can highly recommend is to insulate the underside of the bed. You can get special insulation mats for 3d printers which meet the requirements for this (like being suited for higher temperatures and being flame retardant) for a few bucks. Make sure you order the correct size (preferrably a bit bigger) which is 230x230mm as that's the size of the bedplate itself.   
By insulating the bed the temperature won't fluctuate as much as before, it heats up faster and it takes less energy to keep the desired temperature (so you actually lower the power consumption). It also takes longer for the bed to cool down which became impressively clear after doing a PID tune for the bed and comparing the graphs of before and after adding the insulation (picture will come soon).  
After adding the insulation, the temperature didn't fluctuate anymore at all during a print even when I opened the window from time to time - the graph was just a straight line. So I'm highly satisfied with this actually.     

??? example "Adding the Insulation"  

    Before I'll go into the steps about how to apply the insulation, I have to mention that you'll need longer spacers and screws due to the thickness of the insulation (which is about 9-10mm most of the time). You'll need to raise the whole bedplate to avoid contact between the insulation and the motor mount at the back of the contruction. If you use the beforementioned springs, you'll be fine as they are longer then the stock spacers anyway. If you'll use the stopck spacers or silicone spacers (which may be the same size like the stock spacers), you can add bolt nuts to raise the whole construction.  
    
    For adding the insulation, you need to dismount the bedplate from the gantry by taking out the four screws (remove the PEI coated plate first tho). Be careful with the wires when moving the plate. Put the plate onto the insulation (but don't peel off the protective layer of the adhesive yet!), align it and mark the four holes of the screws.  
    Then place the bed upside down on a flat and clean surface - wipe the surface beforehand tho to make sure that there's no dirt or even metal chips which would press into or stick onto the magnetic surface. Now use IPA or (which I prefer) silicone remover to wipe the underside of the bed where the insulation should be applied to and clean off any dirt or grease from your fingers.  
    Now lay down the insulation onto the bed like if you would apply it (but still with the protective layer on the adhesive!) and adjust the position. Mark the area where the wires are connected to the bed as well and cut away that part of the insulation. Place the spacers above the premarked holes and cut away the insulation in that area as well, so that the spacers will touch the plate later without any insulation between.  
    When it comes down to finally apply the insulation, I personally used Kapton tape and put it onto the whole bedplate first, just in case I'd have to tear off the insulation in the future. I also added two layers of Kapton tape especially above the contacts and the little piece of foam of the thermistor in the center of the bed and marked that area roughly at the insulation, just in case I'd have to replace the thermistor in the future.  
    Once everything is done and prepared, you can finally apply the insulation. Make sure you start at one side to avoid any bubbles, you want the insulation to stick on the bed equally. If some of the insulation protrudes beyond the plate, cut it off.  
    Then add the spacers and the screws and mount the bed onto the gantry again. Make sure that the insulation doesn't touch the construction and the motor mount at the back, the bed has to move as free as before.  
    In case you used adjustable spacers, tram the bed. Also tram the x-axis gantry again in relation to the bed itself.  
    When switching on the printer, make sure you proceed with adjusting the z-offset due to the raised bed and execute an ABL procedure as well as a PID tuning of the bed now and save the new values to the EEPROM.  
    (Pictures will come soon.)
    
