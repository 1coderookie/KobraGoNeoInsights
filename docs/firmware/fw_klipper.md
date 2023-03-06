<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Klipper (Mod)  
  
Can you run [Klipper](https://www.klipper3d.org/) on the stock mainboard of the **Go** and **Neo**?  
Oh yes, you can!  

The [Huada HC32F460 MCU](https://github.com/Klipper3d/klipper/commit/72b6bd7efa1ae282220b4bdcfb789075807ebfd2) is officially supported and implemented in the Klipper firmware.  
  
It should be mentioned that you can always go back to the stock firmware by just re-flashing it, so you might just want to give Klipper a try. 
       
!!! warning  
  
    - Keep in mind that even though the stock mainboard of the **Go** and the **Neo** is the same, you have to adjust certain settings of the file `printer.cfg` depending on your specific model!  
    - After flashing Klipper's `firmware.bin`, don't try to start printing right away! Do all the necessary calibrations and double-check your `printer.cfg`!
    - Be aware of the fact that the control unit/display of the printer doesn't work after flashing Klipper (due to the fact that the SPI the unit is connected to isn't supported by Klipper yet). So you'd need additional software like OctoPrint or Mainsail or so to be able to also control the printer manually. See the chapter ["Printserver"](../printserver.md) if you don't have e.g. OctoPrint installed yet.    

??? info "What Is Klipper?"

    Long story short: Klipper is an 'alternative' firmware which gives you way more possibilities and even functions for configuring and using your 3D printer. If you don't know what Klipper is, this may be a good start for your research: [All3DP: Klipper](https://www.all3dp.com/topic/klipper)  

??? info "Discussion Thread About Klipper"

    I opened a [discussion thread about Klipper](https://github.com/1coderookie/KobraGoNeoInsights/discussions/6) just in case any further questions arise or in case you want to comment on certain things without doing so by sending me an email. Keep in mind though that I'm not an expert at all, so if you do have specific questions about Klipper, then it might be better to ask in a special forum like e.g. the [Klipper subreddit](https://www.reddit.com/r/klippers/).  
  
## Installation
Reddit user [xpeng121](https://www.reddit.com/user/xpeng121/) postet a description about how to create the necessary `firmware.bin` file for installing Klipper: [Install Klipper on Kobra Go or Neo](https://www.reddit.com/r/anycubic/comments/10cwm16/install_klipper_on_kobra_go_or_neo/)  
So I won't go over that procedure here once again. The installation procedure is also described at the specific chapter ["Installation"](https://www.klipper3d.org/Installation.html) of the official documentation.
  
Once you've created the `firmware.bin` file, copy it onto your mSD card and flash it as you would do with the stock firmware. Note that the screen doesn't update though after the flash procedure is done as the control unit doesn't work with Klipper anymore, it'll stick with the message "Firmware update. Please wait.". So just wait 5-10min to make sure everything had time enough to be installed, turn off the printer, remove the card and turn on the printer again. After that you'd need to continue creating and/or configuring the file `printer.cfg` as that is the file where all the device specific informations are stored.    
You'll also find links to `printer.cfg` files for the **Go** and the **Neo** in that thread which makes it even easier to get started with Klipper.  
  
However, also when using the beforementioned config files, remember to adapt the config file to your printer and specific settings *before* starting to print or calibrate the printer!  
Also proceed with the [configuration checks](https://www.klipper3d.org/Config_checks.html) before you're trying to print anything!      
  
## Stock Control Unit
The stock control unit of both the **Go** and the **Neo** don't work with Klipper. So is that going to be an issue? Actually I thought the same initially and that was the only reason which was holding me back switching to Klipper right away at the beginning. Now that I did switch, I can say that I don't really miss the control unit. 

Just as an example:  
- Klipper *keeps* the z-offset, so you don't have to fiddle arount at the control unit for that before each and every print because the stcok-fw forgot your settings once again. 
- Setting temps for e.g. heating up the hotend to change a nozzle or load/unload filament can be done by using Mainsail. 
- Initiating the ABL procedure is also be done thru Mainsail, just like everything else.

However, if you really do miss the option to control the printer right at that place later, you have several options to do so:  
- You can use your smartphone, tablet or laptop to just open the mainsail.local page at your browser and use the regular Mainsail frontend (which might be a bit 'uncomfortable' when using a smartphone though).
- You can use an old smartphone or tablet and install [KlipperScreen](https://klipperscreen.readthedocs.io/en/latest/) onto it, which then gives you a nice adapted UI with control buttons.  
  I also set it up, printed a holder for it and mounted it where the original control unit was, but actually I unplugged the phone again as I just control it via my computer and the mainsail.local page anyway. It also kinda bothers me that I have to boot up the phone all the time as I don't leave the printer on 24/7. I'll add pictures of it here soon though.
- If you have a Raspberry Pi or other hardware you could connect a touchscreen to (e.g. by using a HMDI port) running for hosting Mainsail, you can add a touchscreen to that and use [KlipperScreen](https://klipperscreen.readthedocs.io/en/latest/). It's the same UI like using a smartphone or tablet.  
  This is actually a quite handy solution if you're using a RPi as you can set everything up in a dedicated case. I'll probably do that as well, just for the pure comfort of not having to take care about switching the smartphone on and off as the display is powered by the RPi. I just didn't want to spend money again when trying Klipper initially, that's why I used an old smartphone in first place.    
   
## G-Codes & Macros
Klipper uses extended g-codes and macros, so not all of the 'regular' g-code commands are known and useable within Klipper. See the [g-codes chapter](https://www.klipper3d.org/G-Codes.html) of the documentation for an overview of the specific commands.  
You can also find [command templates](https://www.klipper3d.org/Command_Templates.html) in the official documentation.  
  
You'll also need to replace the g-code you added in the start and end section of your slicer. I'll ad the lines for that soon.   
    
## Slicers
Due to the fact that Klipper uses extended G -code and macros, there are a few things to be aware of when using certain slicers like Cura, PrusaSlicer, SuperSlicer etc.  
In the following I'll just go over Cura and SuperSlicer really quick as I used them both and SuperSlicer is a fork (with enhanced functionality) of PrusaSlicer.  

**Cura**  
Even though Cura and Klipper work perfectly together, there are a few things to be aware of.  
Certain classic G-code commands aren't directly supported by Klipper as it uses extended G-code and scripts for certain things. As an example the G-code command `M0` (unconditional stop) isn't recognized by Klipper, you'd have to use the extended G-code command `PAUSE` for that.  
Also there are a few functions of Cura which should improve the print quality which interfere with Klipper's own approaches for that (like Pressure Advance or Input Shaping).  
You'll find a good overview of what to be aware of in the tutorial from [All3DP: Cura & Klipper: How to Make Them Work Together](https://www.all3dp.com/2/cura-klipper-tutorial).
 
**SuperSlicer**  
My personal favourite. In SuperSlicer you can set the G-code flavor depending on the firmware of the printer (menu "Printer Settings") as shown in the screenshot below, so it's already everything set up correctly within the g-code of the sliced files. <br> ![SuperSlicer firmware](../assets/images/klipperfw_superslicer-flavor.png)
  
Besides that, SuperSlicer has many functionalities to finetune and control the output - you can even choose between different patterns for the top layer finish. Besides that it comes with a really handy calibration functionality which guides you step by step through the calibration process and allows you to generate calibration models like temperature or retraction towers with individual settings by just a few clicks.  
I personally would suppose to use the "Arachne Edition" of SuperSlicer and enable that function as it improves the quality of the printed parts. 

I can't go into all the possibilities of SuperSlicer deeper though as it's just too complex, so just do a research on it.  

## OctoPrint, Mainsail or Fluidd?

**OctoPrint** is mentioned and referred to at the Klipper page, so you can use it just fine.  
You'd need to SSH to the host (e.g. the RPi) though to upload edited files like the `printer.cfg` - if there isn't a plugin for that (I don't know actually) which allows you to do so within the interface of OctoPrint.  
  
However, I personally prefer to use **Mainsail** with Klipper as it's tailored for the usage of/with Klipper and gives you more tools made for Klipper.  
Just to mention a few here: you can edit the `printer.cfg` and every other file just directly within Mainsail and don't have to SSH to the Raspberry Pi.  
You already have a heightmap function included which allows you to create and display the meshview after executing an ABL.  
If your slicer does support it (SuperSlicer does), you can have thumbnails of your models displayed.  
There's also a G-Code viewer already built in and you have the possibilty to create custom macros for e.g. executing backups and activate them with one click - and much more.  
Due to the fact that I personally use Mainsail, I'll always refer to it when it comes down to describe or show certain things in this chapter. 
  
**Fluidd** is (imho) pretty similar to Mainsail, but it doesn't seem to be maintained as much as Mainsail (afaik).  
  
So to find out what's the best solution for you, either do a little research on that or just get another mSD card, install e.g. MainsailOS onto it and then just give it a try.  
    
  
## Pressure Advance
By using Klipper you can take advantage of using a feature called "Pressure Advance". Please refer to the official documentation of [Pressure Advance](https://www.klipper3d.org/Pressure_Advance.html) about how to calibrate and use it.  

## Resonance Compensation: Input Shaping
By using Klipper you can take advantage of using Resonance Compensation and a feature called "Input Shaping". You can either calibrate it manually or by using additional hardware like ADXL345 acceleration sensors. Please refer to the official documentation of [Resonance Compensation](https://www.klipper3d.org/Resonance_Compensation.html#resonance-compensation) about how to calibrate and use it.



