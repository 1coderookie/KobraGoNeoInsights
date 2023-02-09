<link rel=”manifest” href=”docs/manifest.webmanifest”>
  

# Axes

## X-Axis
The X-axis of both the **Go** and the **Neo** is belt driven, the motor which drives the belt is located at the left side.  
You can adjust the tension of the belt by using the knob at the right side of the aluminum profile where the printhead is guided onto.  
  
![X-axis knob](../assets/images/x-axis_knob_web.jpg)
  
### Belt Tension
It's kinda difficult to explain the correct belt tension, so you'd have to experiment a bit with that. Generally speaking, the belt shouldn't be too tightened up and shouldn't be too loose either. If it's too tight, too much pressure will be put onto the motor shaft - if it's too loose though, the belt might slip. If you can 'bend' the belt down a bit by adding a little pressure with your finger onto it but you still feel an amount of resistance, then it's a good sign that you're in the right area of tension. If you pluck it like a guitar string then it should make a relatively high sound.  

### V Slot Wheels Position
The wheels are leading the bed onto the aluminum profile in the middle. They run in the V-slot of the profile and therefore they should sit in a good position. Means, they shouldn't sit too tight in the V-slot but also not too loose - they should be able to roll and move freely, but they shouldn't be too far away from the profile which would lead to instability.  
You can adjust the roller tension by turning the eccentric nut which moves the wheels either towards or away from the aluminum profile. Not all of the wheels have eccentric nuts though as the following pictures show.  
  
![](../assets/images/x-axis_left-side-nut_web.jpg)
  
![](../assets/images/x-axis_knob_nut_web.jpg)
  
---

## Y-Axis
The X-axis of both the **Go** and the **Neo** is belt driven. You can adjust the tension of the belt by using the knob at the front side of the aluminum profile where the bed is guided onto. The bedmount itself has v-slot wheels which are running in the v-slot of the aluminum profile.  
The following picture shows the aluminum profile of the y-axis with the knob for adjusting the belt tension at the front.   
  
![Y-axis knob](../assets/images/y-axis_knob_web.jpg)
  
The motor which drives the belt is positioned at the back of the printer.  
  
![Y-axis motor](../assets/images/y-axis_motor_web.jpg)

### Belt Tension
It's kinda difficult to explain the correct belt tension, so you'd have to experiment a bit with that. Generally speaking, the belt shouldn't be too tightened up and shouldn't be too loose either. If it's too tight, too much pressure will be put onto the motor shaft - if it's too loose though, the belt might slip. If you can 'bend' the belt down a bit by adding a little pressure with your finger onto it but you still feel an amount of resistance, then it's a good sign that you're in the right area of tension. If you pluck it like a guitar string then it should make a relatively high sound. 
    
### V Slot Wheels Position
The wheels are leading the bed onto the aluminum profile in the middle. They run in the V-slot of the long profile in the middle underneath the bed and therefore they should sit in a good position. Means, they shouldn't sit too tight in the V-slot but also not too loose - they should be able to roll and move freely, but they shouldn't be too far away from the profile which would lead to instability.  
You can adjust the roller tension by turning the eccentric nut which moves the wheels either towards or away from the aluminum profile. Not all of the wheels have eccentric nuts though as you might be able to see at the following picture.  
  
![Bedmount](../assets/images/y-axis_gantry_web.jpg)
   
    
---

## Z-Axis
The Z-axis of both the **Go** and the **Neo** is driven by a single rod. The rod is mounted to the motor by a coupler at the bottom. At the end of the top of the rod it's completely unguided, in between it's guided and secured by an anti-backlash nut which you can see at the following picture, it's the black plastic part mounted to the black steel bracket.  
  
![Z-axis views](../assets/images/z-axis_neo_web.jpg)
   
??? tip "Rod Maintenance"

    - Make sure the coupler is mounted correctly and the screws are tightened. Check from time to time that it didn't come loose somehow. 
    - Make sure the rod is clean, there shouldn't stick stuff on it as it could/would block the movement. If you need to clean it, take a toothbrush or something like that to be able to reach the bottom of the thread also.  
    - Once in a while add a little lube to the rod. Don't be excessive here and drown it with oil - just use a tiny bit to make it glide better. I personally like to use PTFE spray for that as it pretty much dries and avoids stuff sticking onto the rod, but every type of *clean* machine oil is fine. 

### V Slot Wheels Position
The wheels are leading the bed onto the aluminum profile in the middle. They run in the V-slot of the z-axis profiles and therefore they should sit in a good position. Means, they shouldn't sit too tight in the V-slot but also not too loose - they should be able to roll and move freely, but they shouldn't be too far away from the profile which would lead to instability.  
You can adjust the roller tension by turning the eccentric nut which moves the wheels either towards or away from the aluminum profile. Not all of the wheels have eccentric nuts though as the picture above shows.  

??? note

    I noticed at my **Neo** that it's impossible for me to adjust the position in a way that leads to the circumstance that all of the three wheels are in a correct position. Both upper wheels on the outside of the profile aren't touching the profile, there always remains a little gap. Even though it seems that everything works fine, so that's either a faulty design or it's intended to be like that.    
    
---

## Endstop Switches
The endstop switches are triggered when either axis reaches its limits.  
So if you notice that e.g. the motor of the y axis doesn't stop when the bed reaches the end then you should check if the belonging switch is faulty. 

??? example "Checking the Switches"

    You can check if the switch really isn't working by triggering it manually while e.g. the bed is moving. If the bed doesn't stop, turn off your printer. Check the connectors at the switch and the mainboard if they're still in place. If everything looks fine here, then it's most likey that the switch itself is faulty. So disassamble the switch from the frame and put in a new one. Wire everything up again and try again triggering it manually if it works now.   
  
---

## Mods

- Some users stabilize the rod of the Z-axis by adding a top holder/aligner with a ball bearing in the center which sits on top of the rod and mount the holder to the gantry to eliminate wobbling of the rod. For doing so, you could print a construction and add a ball bearing, there are different STL files available for this solution.  
  However, as much as it seems useful at first sight, I personally assume that it might be better if the top of the rod can move freely to avoid putting extra pressure on the frame which could result in shear forces if the guidance doesn't allow at least minimal movement.   
    
- Reddit member [DrumsticknDrumstick](https://www.reddit.com/user/DrumsticknDrumstick/) upgraded the z-axis of his **Neo** to a dual drive, the solution fits both the **Go** and the **Neo**: [Kobra neo/go dual Z mod](https://www.reddit.com/r/anycubic/comments/1083sr2/kobra_neogo_dual_z_mod/)  
  However, as much as I personally appreciate this mod and like this idea in general, I'm not sure if it really is a good idea as both motors and rods have to work *absolutely* simulataneously. I once tried a similar mod with my cheap little CNC machine and problems occured as soon as the movement wasn't absolutely identical anymore. However, looking at it at a 3D printer compared to a CNC of similar building architecture, I might be wrong with my concerns as there isn't any pressure applied to the printhead from the bottom side like it is when a router of a CNC machine hits the surface and cuts out material.      
