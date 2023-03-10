<link rel=”manifest” href=”docs/manifest.webmanifest”>
  

# Axes

## X-Axis
The X-axis of both the **Go** and the **Neo** is belt driven, the motor which drives the belt (6mm wide, GT-2 type) is located at the left side.   
You can adjust the tension of the belt by using the knob at the right side of the aluminum profile where the printhead is guided onto.  
  
![X-axis knob](../assets/images/x-axis_knob_web.jpg)
  
### Belt Tension
It's kinda difficult to explain the correct belt tension, so you'd have to experiment a bit with that. Generally speaking, the belt shouldn't be too tightened up and shouldn't be too loose either. If it's too tight, too much pressure will be put onto the motor shaft - if it's too loose though, the belt might slip. If you can 'bend' the belt down a bit by putting a some pressure with your finger onto it but you still feel an amount of resistance, then it's a good sign that you're in the right area of tension. If you pluck it like a guitar string then it should make something like a mid to high sound.  

??? example "Belt Maintenance"

    - Check the belt tension from time to time as it might wear out and lengthen a bit. 
    - Check the teeth of the belt if they are still good looking or if they're worn out or if even some teethe are missing.
    - Check if you can see any cracks at the belt. 
    - Check the gear wheels of the motors which are driving the belts. Are they also looking ok? Did they become loose on the motor shaft somehow?  

### V-Slot Wheels Position
The wheels are leading the printhead onto the aluminum profile of the x-axis. They are mounted onto a metal plate where the printhead itself is mounted onto. The wheels run in the V-slot of the profile and therefore they should sit in a good position.    
You can adjust the roller tension by turning the eccentric nut which moves the wheels either towards or away from the aluminum profile. 

  
??? tip "Adjusting the Position of the V-Slot Wheels"

    - The wheels shouldn't sit too tight in the V-slot but also not too loose. They should touch the aluminum profile and sit in there pretty tight, but they should be able to roll and move freely - so they shouldn't sit too tight though (sorry, it's kinda hard to explain). On the other hand, they also shouldn't be too loose or far away from the profile which would lead to instability. The printhead shouldn't wiggle but it has to be able to move freely.   
    
  
??? example "V-Slot Wheels Maintenance"  

    - As the wheels will suffer from running on the aluminum and debris can build up, clean the aluminum and the wheels itself from time to time. 
    - After that, add some sythetic grease like white lithium grease or silicone grease (e.g. "Super Lube" from Loctite) onto the aluminum profile where the wheels are running to reduce friction. 
    - *Make sure you're not using WD-40 or grease which has graphite or MoS2 added!* 
    - If you see debris building up pretty quick, it's most likely because the wheels are too close to the aluminum and therefore it's too much friction which leads to a quick wearout. So make sure the wheels are touching the aluminum but they shouldn't be too tight.
    
    !!! warning "Don't Use WD-40 for Lubrication"
    
        Do yourself a favour and *never* use WD-40 for *lubrication* as it's *not* a lubricant and will harm your POM wheels by time!  
        People use to think WD-40 is the perfect solution for pretty much everything, but they aren't aware of the fact that -due to the chemical recipe it's made of- it's absolutely not sufficient for getting parts lubed mid- to longterm. Fact is, that the chemicals inside of it will even wash off any grease or oil, it can harm POM and rubber and so on.  
        As an example: So let's say you want to lubricate your bike chain and use WD-40 to do so, you'll basically *wash away* the existent lubrification  which is inside the chain - therefore the chain will be worn out pretty quick. You'll also harm the sealings. If you don't believe me, make a little test by yourself: take an air baloon, pump it up, spray WD-40 onto it and wait..   
  
---

## X-Axis Gantry

### V-Slot Wheels Position
The x-axis gantry is moved along the z-axis aluminum profile driven by the z-axis lead screw, guided by v-slot wheels. They run in the v-slot of the z-axis profiles and therefore they should sit in a good position. Means, they shouldn't sit too tight in the V-slot but also not too loose - they should be able to roll and move freely, but they shouldn't be too far away from the profile which would lead to instability.  
You can adjust the roller tension by turning the eccentric nut of the wheel which moves the wheels either towards or away from the aluminum profile. Not all of the wheels have eccentric nuts though as the following picture shows, only the two wheels (one at each side) which are facing the inner side (towards the bed) do have an eccentric nut.  
    
![](../assets/images/x-axis_left-side-nut_web.jpg)
  
![](../assets/images/x-axis_knob_nut_web.jpg)
  
However, you might face the problem that you just can't get all of the three wheels at each side to touch the aluminum frame as they should. So if you need to adjust the position of the wheels using the eccentric nuts, you might encouter the problem that e.g. the inner wheel and the lower wheel on the outside may sit in the v-slot really nice, but that the third wheel (the upper one on the outside in this example) isn't even touching the aluminum and can be spinned in the air. Whatever you'll try with the eccentric nut of the wheel of the inside (because there's only this one), you won't be able to achieve that all of the three wheels touch the aluminum and sit in the slot like they should.  
So - what to do?  
Well, there's a trick, which directly leads us to the process of tramming the x-axis gantry in relation to the bed itself. Expand the box below to read about how to do so.  

??? example "Tramming the X-Axis Gantry and Adjusting the Wheels"  

    In order to tram the x-axis gantry in relation to the bed so that both are as parallel as possible, I'd suggest to tram the bed first in case you added adjustable spacers like silicone spares or springs.  
    Then take two parts of equal height like cans for example and place them onto the left and right side of the bed (make sure they *really* are identical - once I fiddled around 15min before realizing that the two 'identical' cans weren't exactly identical - the height differece was 3mm..).  
    Lower the x-axis gantry until the aluminum frame of it touches the can(s). Then loosen the two hexagon socket screws which are holding each of the Y-shaped metal plate (where the wheels are mounted onto, at the backside so to say) against the aluminum frame of the x-axis gantry. Dont take them out (!), just loosen them a bit.  
    Also unscrew or at least loosen the anti-backlash nut (depending on how much you have to adjust) so that the gantry really rests on the cans completely as shown in the following picture. <br> ![X-axis gantry](../assets/images/tramming_x-gantry_web.jpg)     
    Now you can adjust the position of the wheels by using the eccentric nut again. This will pull the Y-shaped metal bracket in position because it can move a bit now and you can adjust it's position towards the aluminum frame of the x-axis gantry. You might have to tighten up the wheel a lot initially to make the bracket move though.  
    After it repositioned itself, adjust the position of the wheels to the perfect pressure and adjust everything to the perfect position. Once you checked everything again, retighten the two hexagon socket screws at each bracket again. Now all of the wheels should touch the aluminum frame of the z-axis and the x-axis gantry should be as parallel to the bed as possible. Remount the anti-backlash nut and you should be good to go.                 

??? example "V-Slot Wheels Maintenance"  

    - As the wheels will suffer from running on the aluminum and debris can build up, clean the aluminum and the wheels itself from time to time. 
    - After that, add some sythetic grease like white lithium grease or silicone grease (e.g. "Super Lube" from Loctite) onto the aluminum profile where the wheels are running to reduce friction. 
    - *Make sure you're not using WD-40 or grease which has graphite or MoS2 added!* 
    - If you see debris building up pretty quick, it's most likely because the wheels are too close to the aluminum and therefore it's too much friction which leads to a quick wearout. So make sure the wheels are touching the aluminum but they shouldn't be too tight.
    
    !!! warning "Don't Use WD-40 for Lubrication"
    
        Do yourself a favour and *don't* use WD-40 for *lubrication* as it's *not* a lubricant and will harm your POM wheels by time!  
        People use to think WD-40 is the perfect solution for pretty much everything, but they aren't aware of the fact that -due to the chemical recipe it's made of- it's absolutely not sufficient for getting parts lubed mid- to longterm. Fact is, that the chemicals inside of it will even wash off any grease or oil, it can harm POM and rubber and so on.  
        As an example: So let's say you want to lubricate your bike chain and use WD-40 to do so, you'll basically *wash away* the existent lubrification  which is inside the chain - therefore the chain will be worn out pretty quick. You'll also harm the sealings. If you don't believe me, make a little test by yourself: take an air baloon, pump it up, spray WD-40 onto it and wait.. 


---

## Y-Axis
The Y-axis of both the **Go** and the **Neo** is belt driven (6mm wide).  
You can adjust the tension of the belt by using the knob at the front side of the aluminum profile where the bed is guided onto.   
The x-shaped plate for the bedmount itself has v-slot wheels which are running in the v-slot of the aluminum profile.  
The following picture shows the aluminum profile of the y-axis with the knob for adjusting the belt tension at the front.   
  
![Y-axis knob](../assets/images/y-axis_knob_web.jpg)
  
The motor which drives the belt is positioned at the back of the printer.  
  
![Y-axis motor](../assets/images/y-axis_motor_web.jpg)

The limit switch for the y-axis is mounted at the back right before the motor, the gantry triggers the switch when moved completely to the back.  

![Y-axis limit switch](../assets/images/axes_y-endstop_web.jpg)


### Belt Tension
It's kinda difficult to explain the correct belt tension, so you'd have to experiment a bit with that. Generally speaking, the belt shouldn't be too tightened up and shouldn't be too loose either. If it's too tight, too much pressure will be put onto the motor shaft - if it's too loose though, the belt might slip. If you can 'bend' the belt down a bit by putting some pressure with your finger onto it but you still feel an amount of resistance, then it's a good sign that you're in the right area of tension. If you pluck it like a guitar string then it should make something like a mid to high sound.   
    
??? example "Belt Maintenance"

    - Check the belt tension from time to time as it might wear out and lengthen a bit. 
    - Check the teeth of the belt if they are still good looking or if they're worn out or if even some teethe are missing.
    - Check if you can see any cracks at the belt. 
    - Check the gear wheels of the motors which are driving the belts. Are they also looking ok? Did they become loose on the motor shaft somehow?      
    
### V-Slot Wheels Position
The wheels are leading the bed onto the aluminum profile in the middle. They run in the V-slot of the long profile in the middle underneath the bed and therefore they should sit in a good position. Means, they shouldn't sit too tight in the V-slot but also not too loose - they should be able to roll and move freely, but they shouldn't be too far away from the profile which would lead to instability.  
You can adjust the roller tension by turning the eccentric nut which moves the wheels either towards or away from the aluminum profile. Not all of the wheels have eccentric nuts though as you might be able to see at the following picture.  
  
![Bedmount](../assets/images/y-axis_gantry_web.jpg)
   
??? tip "Check the Screws of the Bedplate and the Gantry of the Bed"

    - Check if the screws are all tightened up. Be careful though to not overtighten the screws of the Bedplate as you would compress the little spacers underneath it and therefore the plate may become warped. On the other hand, if you see that your bed is warped somehow or that the bed is much more off in certain areas or at one side, you can check if the screws in that area might be too tightened up.  
    - Check if the bedplate itself is somehow wobbling. Not only sideways/horizontally, but also up and down/vertically. If so, not only check the v-slot wheels and maybe adjust their fitting using the eccentric nuts, also check if the screws of the gantry of the bed where the wheels are mounted to are tightened up. As an example: at my **Neo** the bed was wobbling up and down in one certain area - after checking the screws and tighten them up everything was sturdy as it should be.         
   
??? example "V-Slot Wheels Maintenance"  

    - As the wheels will suffer from running on the aluminum and debris can build up, clean the aluminum and the wheels itself from time to time. 
    - After that, add some sythetic grease like white lithium grease or silicone grease (e.g. "Super Lube" from Loctite) onto the aluminum profile where the wheels are running to reduce friction. 
    - *Make sure you're not using WD-40 or grease which has graphite or MoS2 added!* 
    - If you see debris building up pretty quick, it's most likely because the wheels are too close to the aluminum and therefore it's too much friction which leads to a quick wearout. So make sure the wheels are touching the aluminum but they shouldn't be too tight.
    
    !!! warning "Don't Use WD-40 for Lubrication"
    
        Do yourself a favour and *never* use WD-40 for *lubrication* as it's *not* a lubricant and will harm your POM wheels by time!  
        People use to think WD-40 is the perfect solution for pretty much everything, but they aren't aware of the fact that -due to the chemical recipe it's made of- it's absolutely not sufficient for getting parts lubed mid- to longterm. Fact is, that the chemicals inside of it will even wash off any grease or oil, it can harm POM and rubber and so on.  
        As an example: So let's say you want to lubricate your bike chain and use WD-40 to do so, you'll basically *wash away* the existent lubrification  which is inside the chain - therefore the chain will be worn out pretty quick. You'll also harm the sealings. If you don't believe me, make a little test by yourself: take an air baloon, pump it up, spray WD-40 onto it and wait..    

---

## Z-Axis
The Z-axis of both the **Go** and the **Neo** is driven by a single lead screw. The lead screw has 8mm in diameter with 8mm lead ('distance' of one complete rotation) and 2mm pitch and has a length of 350mm (it's actually this kind of lead screw which is used pretty much everywhere in these kind of machines).  
This rod is mounted to the 5mm shaft of the motor by a coupler at the bottom. The top end of the rod is completely unguided, in between it's guided and secured by a POM anti-backlash nut which you can see at the following picture, it's the black plastic part mounted to the black steel bracket.  
  
![Z-axis views](../assets/images/z-axis_neo_web.jpg)
   
??? example "Dis- and Reassembling the Z-Axis Lead Screw System"   

    If you need to dis- and reassemble assemble the z-axis lead screw system, there are a few things that one should be aware of. Besides that, the necessary steps are pretty easy and self-explaing, so I'll go over them just really quick.  
    
    **Disassembling:**  
    - First, you should somehow fixate the gantry of the x-axis to get the load off of the lead screw. You can do so by e.g. putting two soupcans onto the bed, each on one side (left/right) and then lower the gantry until it rests onto them. Or you can move the gantry up and fixate it with some velcro straps or cable ties as shown in the picture below. <br> ![Parked x-axis gantry](../assets/images/axes_x-gantry-cableties_web.jpg)  
    - Now unplug the cable from the stepper motor, just to be on the safe side. The printer itself is also switched off of course.  
    - Loosen the two screws at the coupler which conects the motor shaft and the lead screw. 
    - Now you can turn the lead screw by hand to screw it out of the anti-backlash nut. After you completely took it out, dismount the anti-backlash nut from the holder at the frame as well.  
      If you fixated the x-axis gantry at the top like shown in the picture above, you can also just screw the lead screw a bit higher into the anti-backlash nut so that it comes out of the coupler and then you just dismount the anti-backlash nut from the holder at the frame. After that you can take out the lead screw with the nut still on and take off the nut then.  
    - Take off the coupler from the motor shaft as well for being able to inspect everything.  
    
    **Reassembling:**  
    - To reassemble everything, just follow your steps backwards.   
    However, there are a few things you should pay attention to now:  
    - Make sure the motor shaft and the bottom tip of the lead screw are free of oil or grease to avoid slipping of the coupler.  
    - Mount the coupler to the bottom of the lead screw first and tighten the screw. Then put it onto the motor shaft and tighten the screw. The coupler should not move or wiggle on either part.    
    - When installing the anti-backlash nut, make sure you press it together while inserting the lead screw so that the spring inside these two parts of the anti-backlash nut is completely compressed and loaded. 
    - Before finally installing the lead screw, loosen up the screws of the motor holder a bit so that the motor itself can move a bit on the horizontal plane. Then install the lead screw, align everything, screw the anti-backlash nut to the belonging holder and align the motor once again. Then finally tighten up the screws of the motor mount. By doing so you do the best you can to get the parts vertically aligned as much as possible.  
   
??? example "Lead Screw Maintenance"

    - Make sure the coupler is mounted correctly.    
      Check from time to time that the coupler didn't come loose somehow. 
    - Make sure the rod is clean, there shouldn't stick debris or dirt on it as it could/would block the movement. The following picture shows a partially clogged thread due to debris of the anti-backlash nut. <br> ![Debris in Thread](../assets/images/axes_dirty-thread_web.jpg) <br> In this case the motor was still able to move the rod across it, but you could notice a tiny jerk at that point.  
    - If you need to clean it, it's advisable to disassamble the whole rod system including the coupler and the anti-backlash nut. The following picture shows the **Neo** where the coupler, rod and nut are dismounted. <br> ![Dismounted z-axis](../assets/images/axes_z-axis-dismounted_web.jpg) <br> See the other expandable box for some guidances about dis- and reassembling the z-axis lead screw system.  
    - Spray e.g. WD-40 on the rod to loosen old sticky oil and debris. Then take a toothbrush or something like that for being able to reach the bottom of the thread also and clean it up. Make sure to not leave any particles from the anti-backlash nut like shown in the picture below or any dirt stuck on it. <br> ![Debris](../assets/images/axes_POMdebris_web.jpg)
    - After this procedure, clean the WD-40 off of the rod by using e.g. car break cleaner or silicone remover spray. It'll wash off everything, you can also use an old cloth to wipe it (but make sure that no textile fibres will stick in the thread somehow). 
    - After you cleaned and dried it, inspect the rod and the anti-backlash nut.  
      Are there any dents in the thread or any kind of deformation that shouldn't be there? Is it really straight or is it somehow bent (roll it across a flat surface)? If so, it would be best to get a new lead screw and replace it.   
      Is the anti-backlash nut worn out like in the picture shown below? If so, replace it, maybe use a brass one instead (note: until now I didn't find a brass one that fits the distance of the holes though). <br> ![Worn out nut](../assets/images/axes_worn-nut_web.jpg) <br> When you mount the anti-backlash nut to the belonging part of the frame, I personally like to not tighten up the screws completely to allow a bit of a movement on the horizontal plane.  
    - If everything is fine though and you want to mount the lead screw to the printer again, add a little lube to the rod. Don't be excessive here and drown it with oil - just use a tiny bit to make it glide better.  
    *Don't use WD-40 or grease which contains graphite or MoS2!*   
    I personally like to use PTFE spray first, let it dry and then put some synthetic lube on which is made for mountainbike chains as it uses to stick a bit better onto the metal. But every good medium to heavy synthetic machine oil will do the job just fine. If you have, you can also add synthetic grease like PTFE or silicone grease.  
    You can draw a line of oil all along one side of the rod from the bottom to the top and then put the rod between your fingers and turn it. By doing so, the excessive oil will build up at your fingers and will also reach the bottom of the rod. Wipe off any excessive amount of oil afterwards again - you don't want to have oil dripping down on your motor later!  
    Tip: to avoid dripping oil down to the motor, I personally wrap a pipe cleaner around the rod right above the coupler. If by time a drop or two will move down, the pipe cleaner will absorb it.     
    - Before installing the rod into the coupler of the motor again, clean the last inch of the bottom again by using the car break cleaner and the cloth. Try to get it as much degreased as possible, so that it doesn't start to slip inside of the coupler later. 
    - When you're done reassembling everything and you home the printhead, you only should hear the low noise of the turning motor now - so now grinding noise from the anti-backlash nut or something like that.  
    
    !!! warning "Don't Use WD-40 for Lubrication"
    
        Do yourself a favour and *never* use WD-40 for *lubrication* as it's *not* a lubricant!  
        It's perfectly fine for washing off old oil from the threaded rod, but it's *not* a sufficient lubrification!  
        People use to think WD-40 is the perfect solution for pretty much everything, but they aren't aware of the fact that -due to the chemical recipe it's made of- it's absolutely not sufficient for getting parts lubed mid- to longterm. Fact is, that the chemicals inside of it will even wash off any grease or oil, it can harm POM and rubber and so on.  
        As an example: So let's say you want to lubricate your bike chain and use WD-40 to do so, you'll basically *wash away* the existent lubrification  which is inside the chain - therefore the chain will be worn out pretty quick. You'll also harm the sealings. If you don't believe me, make a little test by yourself: take an air baloon, pump it up, spray WD-40 onto it and wait..  
  
??? example "Changing the Coupler"

    It might be a good idea to change the coupler as the one which comes with the printer doesn't compensate any misalignement of the motor shaft and the lead screw. So if they aren't in a perfect vertical alignment, it will result in shear forces, increased wear of the anti-backlash nut and even may cause jamming. The following picture shows the stock coupler that is mounted. <br> ![Coupler](../assets/images/axes_stock-coupler_web.jpg) <br> Here is a picture of a flex coupler I replaced the stock coupler with. <br> ![Flex coupler](../assets/images/axes_flexcoupler_web.jpg) <br> When mounting it, I put a ball of a ball bearing between the motorshaft and the lead screw, so that the flexcoupler won't be pushed together by the weight of the z-axis. I also added ball bearings underneath the flexcoupler to keep the main load off of the motorshaft and transfer it to the motorhousing. Additionally, I also added a nylon washer of the correct thickness underneath the motor itself as it was hanging in the air, only held by the two screws of the motormount at the z-axis aluminum profile.      
    If you want to change the coupler, you'll need to get a coupler which suits 5mm on one side and 8mm on the other side as the motor shaft is 5mm and the rod is 8mm in diameter. Make sure you *don't* get a coupler which uses a grub screw that holds onto the shaft and rod itself, you need to get a coupler which uses some kind of a clamp mechanism as the stock one. The reason is simple: the motor shaft is round, it doesn't have a flat area where a grub screw needs to be screwn onto. Same goes for the lead screw itself.    
    
??? example "Changing the Anti-Backlash Nut"  

    If the anti-backlash nut that came with the printer is worn out like shown in the picture below, you should look out for a new one. <br> ![Worn out nut](../assets/images/axes_worn-nut_web.jpg) <br> The nut shown at the picture above is still useable though as it still sits tight on the rod. However, sooner or later the debris will come off again and stick on the rod which may causes jams or stuttering of the z-axis movement.     
    If you find a spring tensioned anti-backlash nut made of brass, you can also use that. However, until now I didn't find one which fits the distance of the holes though.  
    When you (re-)install the anti-backlash nut, make sure that you press both parts together when putting the lead screw in. There's a little spring between the upper and the lower part of the nut which is there to prevent the backlash. This spring needs to be pushed together during the installation, so that there's tension and both parts of that nut system are being pushed away from each other when installed.  
        
    !!! tip "Oldham Coupler"
    
        If you find one that fits, you can mount an Oldham coupler additionally between the nut and the holder of the frame. That'll allow horizontal movement of the rod which avoids jamming, stuttering or banding caused by the z-axis.  
  
      
---

## Endstop Switches
The endstop switches are located at the *minimum* endposition of each axis and are triggered when either axis reaches its limit. The switches of the x- and y-axes are mechanical switches, the one at the z-axis is an optical switch.    
So if you notice that e.g. the motor of the y-axis doesn't stop when the bed reaches the end then you should check if the belonging switch is faulty. 

??? example "Checking the Switches"

    You can check if the switch really isn't working by triggering it manually while e.g. the bed is moving. If the bed doesn't stop, turn off your printer. Check the connectors at the switch and the mainboard if they're still in place. If everything looks fine here, then it's most likey that the switch itself is faulty. So disassamble the switch from the frame and put in a new one. Wire everything up again and try again triggering it manually if it works now.   
  
---

## Mods

The following mods should fit both the **Go** and the **Neo** due to the mostly identical design of the printer itself. So I'm just listing them without any distinction.  
  
### Z-Axis: Bearing Block at the Top 
Some users stabilize the rod of the Z-axis by adding a bearing block at the top. That's basically a holder/aligner with a ball bearing in the center which sits on top of the lead screw and mount the holder to the gantry to eliminate wobbling of the lead screw. For doing so, they print a construction and add a ball bearing, there are different STL files available for this solution.  
  However, as much as it may seem useful at first sight, I personally vote against this. In my opinion it's better if the top of the lead screw can move freely to avoid putting extra pressure on the lead screw, the frame and associated parts - especially in this case where we don't have a high precision type of construction and parts. If the guidance at the top doesn't allow at least minimal movement, then this could result in shear forces and even in bending the lead screw itself which would cause jamming or banding caused by the z-axis, also the anti-backlash nut will mist likely wear out earlier.  
  
??? note "Analogy to Fixed vs Free End of the Z-Axis"
  
    The reason for this is quite simple, yet it seems that people aren't aware of it, so I'll try to explain it with an analogy.  
    Think of the z-axis lead screw like it's a pool cue which is curved like the really bad ones you have to play with in certain bars. So when you put the cue on the table and roll it - what happens? It'll bump and stutter, there won't be a smooth movement, right?  
    So now imagine a friend is holding the top and the bottom of it in place while you're holding it somewhere at the middle for example. Your friend here is the coupler and the holder at the top of the lead screw, you're the anti-backlash nut.  
    So when your friend tries to turn the cue by rotatin it at the bottom while both of you still hold the other two spots - what happens? Will you as the 'anti-backlash nut' feel the wiggle and the forces or will it turn smooth? Exactly, you'll feel it - depending on how much the cue is bent and where exactly you placed your hand you'll either feel it stronger or weaker.  
    So now let's place this cue on the edge of the table, so that only the bottom part lays on it. Again you place your hand somewhere in the middle and hold the cue tight, the end of the cue is just in the air.  
    So when your friend rotates the cue again at the bottom - what will happen? Exactly, the end of the cue will wiggle around and you won't feel the forces that strong anymore like before.  
    Now you and your friend still hold the cue at these positions, but both of you allow a tiny bit of movement, like you allow to move your arms just a tiny bit, following the movement of the cue. Again your friend rotates the cue at the bottom while the top of the cue can still wiggle around in the air. What will happen? Exactly, you as the 'anti-backlash nut' guy won't feel pretty much any forces or stuttering anymore.  
    I know, using analogies isn't always a good idea to explain things, but I hope it became at least a bit more clear to you why (imho) the end of the lead screw shouldn't be rigidly fixed and why I suppose to use a flexible coupler at the bottom and an Oldham coupler in the middle where the anti-backlash nut is mounted to the frame.   
  
    
### Z-Axis: Dual Driven Z-Axis 
Reddit member [DrumsticknDrumstick](https://www.reddit.com/user/DrumsticknDrumstick/) upgraded the z-axis of his **Neo** to a dual drive, the solution fits both the **Go** and the **Neo**: [Kobra neo/go dual Z mod](https://www.reddit.com/r/anycubic/comments/1083sr2/kobra_neogo_dual_z_mod/)  
  Due to the pretty much same construction of the frame, you should also be able to use mod kits that fit the Creality Ender 3 for example, but here a user mentioned that the lead screw appears to not be the same like at the **Go** or the **Neo**. I can't judge this as I didn't get myself such a kit and didn't compare them.  
  However, as much as I personally appreciate this mod and like this idea in general, I'm not sure if it really is a good idea as both motors and rods have to work *absolutely* simulataneously and have to be in sync. I once tried a similar mod with my cheap little CNC machine and problems occured as soon as the movement wasn't absolutely identical anymore. However, looking at it at a 3D printer compared to a CNC of similar building architecture, I might be wrong with my concerns as there isn't any pressure applied to the printhead from the bottom side like it is when a router of a CNC machine hits the surface and cuts out material.  
  There are also solutions to find where both lead screws are driven by that one motor only, using a gear and a belt that connects those three parts (motor and lead screws). As long as you can't drive each stepper motor with it's own stepper driver and therefore could use the G-Code command G34 Z steppers auto-alignment, this belt solution somehow looks more appealing to me personally.  
