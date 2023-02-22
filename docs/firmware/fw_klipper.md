<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Klipper (Mod)  
  
Can you run [Klipper](https://www.klipper3d.org/) on the stock mainboard? Oh yes, you can!  
    
Reddit user [xpeng121](https://www.reddit.com/user/xpeng121/) postet a description about how to get it done: [Install Klipper on Kobra Go or Neo](https://www.reddit.com/r/anycubic/comments/10cwm16/install_klipper_on_kobra_go_or_neo/)

!!! warning  
  
    - Keep in mind that even though the stock mainboard of the **Go** and the **Neo** is the same, you have to adjust certain settings of the Klipper configuration depending on your specific model!  
    - After flashing Klipper's `firmware.bin`, don't try to start printing right away! Do all the necessary calibrations and double-check your `printer.cfg`!
    - Be aware of the fact that the control unit/display of the printer doesn't work after flashing Klipper (due to the fact that the SPI the unit is connected to isn't supported by Klipper yet). So you'd need additional software like OctoPrint or Mainsail or so to be able to also control the printer manually. See the chapter ["Printserver"](../printserver.md) if you don't have e.g. OctoPrint installed yet.    

??? tip "What Is Klipper?"

    Long story short: Klipper is an 'alternative' firmware which gives you way more possibilities and even functions for configuring and using your 3D printer. If you don't know what Klipper is, this may be a good start for your research: [All3DP: Klipper](https://www.all3dp.com/topic/klipper)  

??? tip "Cura and Klipper"

    Even though Cura and Klipper work perfectly together, there are a few things to be aware of.  
    Certain classic G-code commands aren't directly supported by Klipper as it uses extended G-code and scripts for certain things. As an example the G-code command `M0` (unconditional stop) isn't recognized by Klipper, you'd have to use the extended G-code command `PAUSE` for that.  
    Also there are a few functions of Cura which should improve the print quality which interfere with Klipper's own approaches for that (like Pressure Advance or Input Shaping).  
    You'll find a good overview of what to be aware of in the tutorial from [All3DP: Cura & Klipper: How to Make Them Work Together](https://www.all3dp.com/2/cura-klipper-tutorial).
  
??? tip "OctoPrint, Mainsail or Fluidd with Klipper?"

    OctoPrint is mentioned and referred to at the Klipper page, so you can use it just fine. Especially when you want to use the TimeLapse plugin there isn't really an alternative to OctoPrint.  
    However, I personally prefer to use Mainsail with Klipper as it gives you more tools made for Klipper. Just to mention a few here: you can edit the `printer.cfg` and every other file just directly within Mainsail and don't have to SSH to the Raspberry Pi. You already have a heightmap function included which allows you to create and display the meshview after executing an ABL. There's also a G-Code viewer already built in - and much more.  
    Fluidd is pretty similar to Mainsail, but it doen't seem to be maintained as much as Mainsail (afaik).  
    So to find out what's the best solution for you, either do a little research on that or just get another mSD card, install e.g. MainsailOS onto it and then just give it a try.  
    
