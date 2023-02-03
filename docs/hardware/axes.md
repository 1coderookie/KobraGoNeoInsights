<link rel=”manifest” href=”docs/manifest.webmanifest”>
  

# Axes

## X-Axis
The X-axis of both the **Go** and the **Neo** is belt driven.  
You can adjust the tension of the belt by using the knob at the right side of the aluminum profile where the printhead is guided onto.  

??? tip "Belt Tension"

    It's kinda difficult to explain the correct belt tension, so you'd have to experiment a bit with that. Generally speaking, the belt shouldn't be too tightened up and shouldn't be too loose either. If you can 'bend' the belt down by adding a little pressure with your finger onto it, then it's a good sign that you're in the right area of tension.

## Y-Axis
The X-axis of both the **Go** and the **Neo** is belt driven. You can adjust the tension of the belt by using the knob at the front side of the aluminum profile where the bed is guided onto.  

??? tip "Belt Tension"

    It's kinda difficult to explain the correct belt tension, so you'd have to experiment a bit with that. Generally speaking, the belt shouldn't be too tightened up and shouldn't be too loose either. If you can 'bend' the belt down by adding a little pressure with your finger onto it, then it's a good sign that you're in the right area of tension. 
    
## Z-Axis
The Z-axis of both the **Go** and the **Neo** is driven by a single rod. The rod is mounted to the motor by a coupler.  
  
??? tip "Rod Maintenance"

    - Make sure the coupler is mounted correctly and the screws are tightened. Check from time to time that it didn't come loose somehow. 
    - Make sure the rod is clean, there shouldn't stick stuff on it as it could/would block the movement. If you need to clean it, take a toothbrush or something like that to be able to reach the bottom of the thread also.  
    - Once in a while add a little lube to the rod. Don't be excessive here and drown it with oil - just use a tiny bit to make it glide better. I personally like to use PTFE spray for that as it pretty much dries and avoids stuff sticking onto the rod, but every type of *clean* machine oil is fine. 

## Endstop Switches
The endstop switches are triggered when either axis reaches its limits.  
So if you notice that e.g. the motor of the y axis doesn't stop when the bed reaches the end then you should check if the belonging switch is faulty. 

??? experiment "Checking the Switches"

    You can check if the switch really isn't working by triggering it manually while e.g. the bed is moving. If the bed doesn't stop, turn off your printer. Check the connectors at the switch and the mainboard if they're still in place. If everything looks fine here, then it's most likey that the switch itself is faulty. So disassamble the switch from the frame and put in a new one. Wire everything up again and try again triggering it manually if it works now.   
  
## Mods

- Some users stabilize the rod of the Z-axis by adding a top holder/aligner with a ball bearing in the center which sits on top of the rod and mount the holder to the gantry to eliminate wobbling of the rod. For doing so, you could print a construction and add a ball bearing, there are different STL files available for this solution.  
  However, as much as it seems useful at first sight, I personally assume that it might be better if the top of the rod can move freely to avoid putting extra pressure on the frame which could result in shear forces if the guidance doesn't allow at least minimal movement.   
    
- Reddit member [DrumsticknDrumstick](https://www.reddit.com/user/DrumsticknDrumstick/) upgraded the z-axis of his **Neo** to a dual drive, the solution fits both the **Go** and the **Neo**: [Kobra neo/go dual Z mod](https://www.reddit.com/r/anycubic/comments/1083sr2/kobra_neogo_dual_z_mod/)  
  However, as much as I personally appreciate this mod and like this idea in general, I'm not sure if it really is a good idea as both motors and rods have to work *absolutely* simulataneously. I once tried a similar mod with my cheap little CNC machine and problems occured as soon as the movement wasn't absolutely identical anymore. However, looking at it at a 3D printer compared to a CNC of similar building architecture, I might be wrong with my concerns as there isn't any pressure applied to the printhead from the bottom side like it is when a router of a CNC machine hits the surface and cuts out material.      
