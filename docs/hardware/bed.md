<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Bed
Both of the printers have a heated and magnetic bed with the *physical* dimension of 230x230mm - even though Anycubic states in the official specs that the size is 220x220mm.  
However, if you're looking for a bedplate or a PEI plate from a third party company, you need to get yourself a 230x230mm plate, otherwise it would be too small.  

The temperature of the bed should reach about ≤230°F/110°C maximum and therefore it should be possible to successfully print ABS, PETG and TPU (by using a housing though) besides PLA.  
Both printers offer a 25-point automatic bed leveling which is called "Anycubic LeviQ".  
        
The bed uses a removable PEI-coated spring steel plate which makes it easy to remove the printed object.  
The plate that comes with the printer is one-sided coated at the **Go** and double-sided coated at the **Neo**.   
The following picture shows the surface of the coated plate of the **Neo** from a close-up view.  
  
![Close-up view of the PEI-coated plate](../assets/images/bed_closeup_web.jpg)  
  
When you look at the backside of the bed, you'll notice a black plastic cap which sticks out.  
  
![Bed connector](../assets/images/bed_connector_side_web.jpg)
  
Be careful to never break it by accident as it protects the wires which are soldered to the contacts of the board at the bottom side.  
  
![Soldered connections](../assets/images/bed_connection_web.jpg)
  
When you take a look underneath the bed itself, you'll spot a little foam piece secured by kapton tape - don't remove that as it protects and insulates the thermistor of the bed which is positioned underneath it.  
  
![Bed thermistor](../assets/images/bed_thermistor_web.jpg)
  
The following picture shows the unmounted bed from the underside.  

![Bed underside](../assets/images/bed_underside_web.jpg)  

The bedplate itself is mounted to the y-axis gantry shown in the following picture.  

![Bed gantry](../assets/images/bed_gantry_web.jpg)
  
??? info "Bed Thermistor"

    The thermistor of the bed is positioned underneath the white piece of foam in the center of the bed. It's soldered to two contacts at the plate, so in case the thermistor is broken, you should be able to replace it.    
  
??? tip "Bed Leveling Function"

    - Don't get misleaded by the term "automatic bed leveling" - the process does *not* level your bed! It only measures and recognizes the distance towards the sensor at the 25 spots where it measures. You can *not* level the bed itself without tinkering as it's mounted directly to the construction which leads the bed in the y-axis.    
    - When it comes to executing the ABL function of the printer, it's advisable to initially check if the ABL sensor is leveled correctly to get the best results out of the ABL process. See the expandable box "Leveling the ABL Sensor" in the section ["Leveling or Dismounting the ABL Sensor"](printhead.md#leveling-or-dismounting-the-abl-sensor) in the chapter "Printhead".  
    - To make the measured values of the ABL come into account later when it comes down to printing, you'll need to add a certain line to the start G-code of the slicer. I'm not 100% sure yet, but right now it seems like the necessary command is `M420 S1` which reads the data out of the EEPROM.  
    - Keep in mind that every time you proceed an ABL process, you'll have to set the z-offset again!
  
??? tip "Execute PID Tuning For The Bed"

    To make sure the heating algorithm can work as expected and keeps the fluctuation of the temperature as low as possible, execute a PID tuning. You can find informations about how to do that in the chapter ["PID Tuning"](../pid-tune.md).  
  
??? tip "Clean the Plate Of The Bed"

    - Before starting a print, make sure the surface of the plate is clean and without any traces of oil, silicone or other stuff which avoids that the filament sticks to the surface. To clean it, use isopropyl alcohol or (what I personally use and recommend) silicone remover spray (it's the stuff the guys use to clean the surface before spraypainting a car).  
    - Already touching the plate with your fingers leads to a little amoung of grease left there which already might be enough to cause problems for your print to stick on the bed, so maybe always use disposable gloves when touching it, taking it off or repositioning it.
    - If there's a rest of filament stuck on the plate, *never* try to scratch it off with metal or other sharp materials as you don't want to harm the PEI coating. Heat up the bed and try to peel off the filament instead. If that doesn't work, take off the plate and heat up the area using your hot air gun - sooner or later you'll be able to peel it off. However, be careful to not overheat and maybe harm the coating though.  
  
  
??? tip "Level The ABL Sensor"

    It's advisable to level the ABL sensor in relation to the nozzle initially, you can find informations about it in the hardware section within the chapter ["Printhead"](printhead.md#leveling-or-dismounting-the-abl-sensor).  
    
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


??? tip "Spacers Of The Bedmount"

    If you find that the bed is not as flat or trimmed as it should be, it might be a good idea to disassemble it and check the four black spacers that connect the metal y-axis gantry and the bed itself. Measure them with a slide gauge to see if they are really the same height.  
    If they're not, either look for other spacers you might be using, put the stock ones on a flat surface with sandpaper and grind them down to one length or put washers or other suitable material (e.g. gasket material) of the needed thickness under them. Then execute another ABL and compare the new values. From there you can try to get it as much trammed as possible. If that doesn't really help, check the "Mods" section below and read the part about using different types of spacers.       
            
  
??? example "Check The Screws Of The Bedplate And The Gantry Of The Bed"

    - Check if the screws are all tightened up. Be careful though to not overtighten the screws of the Bedplate as you may compress the little spacers underneath it and therefore the plate may become warped. On the other hand, if you see that your bed is warped somehow or that the bed is much more off in certain areas or at one side, you can check if the screws in that area might be too tightened up or too loose.  
    - Check if the bedplate itself is somehow wobbling. Not only sideways (horizontally), but also up and down (vertically). If so, not only check the v-slot wheels and maybe adjust their fitting using the eccentric nuts, also check if the screws of the gantry of the bed where the wheels are mounted to are tightened up.    
    
??? example "Tramming The Bed"

    If you added adjustable spacers like silicone spacers or springs, you'll be able to tram your bed. When you want to tram the bed by adjusting the tension of the springs or silicone spacers to pull down a side or an edge of the bed, be careful to not bend the bed itself by tightening up just one corner too much. Try to push down one side of the bed and adjust two screws at a time. Even then be careful though and keep an eye on the mesh visualizer or (if you con't have that one) on the values of the ABL.   
    
??? example "Tramming The X-Axis Gantry"  

    To make sure that the bed and the x-axis gantry are parallel to each other, you should also tram the gantry in relation to the bed itself - if you're using the stock spacers. If you're using adjustable spacers, you should tram the x-axis gantry to the frame and then tram the bed in relation to the nozzle (imhoo). See the expandable box in the section [X-Axis Gantry](../axes.md/#x-axis-gantry) to read how you could do it. 
    
## Mods

### Different Spacers
Because you can't level the bed itself due to the construction, you may want to replaced the stock spacers with springs or silicone spacers which allows tramming of the bed itself.  
It's adviseable to make sure that the bolt can't turn itself loose due to the vibration, so add a nylon lock nut or a counter nut to the tip of the screw underneath the bed gantry as well.  

**Springs**  
Mounting springs instead of rigid spacers allows you to tram the bed itself. You'd have to get yourself some longer M4 type screws as well as the stock ones will be too short. Get yourself some nylon washers as well which you place between the underside of the bed and the springs to prevent scratching the surface. Add a lock nut underneath the gantry to the end of the screws as well after tramming the bed.    
However, as springs are made from metal which underlies the temperature changes of the heated bed, it'll probably be necessary to check the level once in a while.    
  
I personally used 8x25mm springs (the yellow ones shown below) and M4x40mm countersunk head screws as that allowed me to add some bigger lock nut knobs I had laying around. So if you go with regular M4 lock nuts, 35mm (or *maybe* even 30mm) screws should be fine as well I guess. Those springs were part of a bundle from Capricorn, they came together with 1m of the Capricorn tube and a cutter (and a sticker) for a really fair price (about 11€ for everything together).  

**Silicone Spacers**  
You could also use silicone spacers of about the same length as the stock spacers for being able to use the stock screws and still being able to tram the bed. They are adjustable as well due to the flexible material and they don't expand and shrink with changing temperatures like metal springs will do in a minor range. I'd suppose to add a lock nut underneath the gantry to the end of the screws as well after tramming the bed though.  
  
Keep in mind that the silicone spacers (I used 18mm long ones shown below) compress when tramming the bed. Therefore it *might* happen that you'll get into trouble because the position of the whole bedplate will be lowered a bit, so make sure that the bedplate doesn't somehow hit the motor mount at the back of the y-axis. *Especially when adding insulation to the underside of the bed, you'll need to raise the bedplate a bit, so I highly recommend using the abovementioned 25mm springs in that case anyway!*   
  
The following picture shows the stock spacers on the left, springs in te middle and silicone spacers on the right. <br> ![Spacers](../assets/images/bed_different-spacers_web.jpg)
  
??? example "Tramming The Bed"

    When you want to tram the bed by adjusting the tension of the springs or silicone spacers to pull down a side or an edge of the bed, be careful to not bend the bed itself by tightening up just one corner too much. Try to push down one side of the bed and adjust two screws at a time.    
    I personally tram the bed by adding just a little bit of load to the spacers, so that the bed doesn't wobble. Then I'm measuring the distance between the tip of the ABL sensor and the bedplate where the screws are located in first place and adjust the four screws to get the same distance. Then I proceed with an ABL and look at the mesh and the values and repeat the steps if necessary.  
    Remember that every time you adjust one screw, it most likely will affect the other screws as well!  
    For finetuning I add Kapton tape on the magnetic surface of the bed underneath the PEI plate to egalize warped or dented areas as much as possible.  
    In case you're using Klipper like me, you can use the macro ["screws_tilt_adjust with the command SCREWS_TILT_CALCULATE"](https://www.klipper3d.org/Manual_Level.html#adjusting-bed-leveling-screws-using-the-bed-probe) to finetune the tramming of the bed.  
    When you're done, make sure the screws won't turn themselves loose due to the vibration, so add e.g. an additional lock nut as well.    
    Also remember to check your z-offset as it'll most likely has to be adjusted.  
    
### Insulating The Bed
What I personally can highly recommend is to insulate the underside of the bed.  
You can get special insulation mats for 3d printers which meet the requirements for this (like being suited for higher temperatures and being flame retardant) for a few bucks. See the expandable textblock below for some tips about the installation.    
Make sure you order the correct size (preferrably a bit bigger) which is 230x230mm as that's the size of the bedplate itself.  

![Bed insulated](../assets/images/bed_insulated_web.jpg)

By insulating the bed the temperature won't fluctuate as much as before, it heats up faster and it takes less energy to keep the desired temperature (so you actually lower the power consumption). It also takes longer for the bed to cool down which became impressively clear after doing a PID tune for the bed and comparing the graphs of before and after adding the insulation as the following screenshots will show.  
The first screenshot shows the bed temperature (blue graph) before the insulation while doing a PID tuning. The temperature is set to 60°C, after reaching that temperature the bed cools down to 55°C and heats up to 60°C again (and so on). The second screenshot shows the same process but with installed insulation. You can clearly see that it takes longer to cool down after reaching the 60°C as the blue graph of the second screenshot isn't declining as steep and fast to the 55°C target temperature as the one in the first screenshot.  
![Bed PID before insulating](../assets/images/bed_pre-insulation_PID.jpg)   
![Bed PID after insulating](../assets/images/bed_post-insulation_PID.jpg)  
  
After adding the insulation, the temperature didn't fluctuate anymore at all during a print, even when I opened the window from time to time - the graph was just a straight line. So I'm highly satisfied with this actually and can strongly recommend insulating the bedplate.     

??? example "Adding The Insulation"  

    Before I'll go into the steps about how to apply the insulation, I have to mention that *you'll need longer spacers and screws due to the thickness of the insulation (which is about 9-10mm most of the time)!*  
    *You'll need to raise the whole bedplate to avoid contact between the insulation and the motor mount at the back of the construction.* If you use the beforementioned springs, you'll be fine as they are longer then the stock spacers anyway. If you'll use the stock spacers or silicone spacers of about the same size, you can add bolt nuts underneath to raise the bed.  
    *It's also advisable to have Kapton tape on hand to cover the whole underside of the bedplate with it (before you actually apply the insulation) and to secure the edges and sides of the insulation (after applying the insulation).*     
    
    - For adding the insulation, you need to dismount the bedplate from the gantry by taking out the four screws (remove the PEI coated plate first tho). Be careful with the wires when moving the plate. Put the plate onto the insulation (but don't peel off the protective layer of the adhesive yet!), align it and mark the four holes of the screws.  
    - Then place the bed upside down on a flat and clean surface - wipe the surface beforehand tho to make sure that there's no dirt or even metal chips which would press into or stick onto the magnetic surface. Now use IPA or (which I prefer) silicone remover to wipe the underside of the bed where the insulation should be applied to and clean off any dirt or grease from your fingers.  
    - Now lay down the insulation onto the bed like if you would apply it (*but still with the protective layer on the adhesive!*) and adjust the position. Mark the area where the wires are connected to the bed as well and cut away that part of the insulation. Place the spacers above the premarked holes and cut away the insulation in that area as well, so that the spacers will touch the plate later without any insulation between. I'd recommend to mark the areas that should be cut and then take the insulation away from the bedplate, so that you don't harm the surface when using a sharp knife or so.   
    - When it comes down to finally apply the insulation, *I personally would suggest to cover the whole surface of the bed with Kapton tape first,* just in case you'd have to tear off the insulation in the future. I also added two layers of Kapton tape especially above the contacts and the little piece of foam of the thermistor in the center of the bed and marked that area roughly at the insulation, just in case I'd have to replace the thermistor in the future.  
    - Once everything is done and prepared, you can finally apply the insulation. Make sure you start at one side to avoid any bubbles, you want the insulation to stick on the bed equally. If some of the insulation protrudes beyond the plate, cut it off. The following picture shows the applied insulation. <br> ![Bed insulated](../assets/images/bed_insulated_web.jpg)   
    - *I highly recommend to additionally secure the insulation by using some pieces of Kapton tape as well to ensure that the edges and sides of the insulation won't come loose.* Don't skip this step, as the insulation most likely will come off sooner or later at the sides and edges (at least mine did).    
    - Then add the spacers and the screws and mount the bed onto the gantry again. Make sure that the insulation doesn't touch the construction and the motor mount at the back, the bed has to move as free as before. So move the bedplate manually to see if everything is fine and if there's enough clearance between the insulation and the other parts.  
    - If you used adjustable spacers, tram the bed again.  
    - When switching on the printer, make sure you proceed with executing an ABL procedure, adjusting the z-offset due to the raised bed and execute a PID tuning of the bed now and save the new values to the EEPROM.  
    
