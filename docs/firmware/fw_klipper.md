<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Klipper (Mod)  
  
Can you run [Klipper](https://www.klipper3d.org/) on the stock mainboard of the **Go** and **Neo**?  
Oh yes, you can!  

The [Huada HC32F460 MCU](https://github.com/Klipper3d/klipper/commit/72b6bd7efa1ae282220b4bdcfb789075807ebfd2) is officially supported and implemented in the Klipper firmware.  
  
??? tip "Important Information To Be Aware Of" 

    - It should already be mentioned here that you can always go back to the stock firmware by just re-flashing it, so you might just want to give Klipper a try. 
    - Be aware of the fact that the control unit and display of the printer doesn't work after flashing Klipper due to the fact that the SPI the unit is connected to isn't supported by Klipper yet. See the belonging section further down below for more information. 
    - You'd need a host to run additional software like OctoPrint or Mainsail for being able to use the printer with Klipper. See the belonging section further down below for some information and my personal recommendation abput what to use.  
    If you don't have a host running OctoPrint/Mainsail/.. yet, see the chapter ["Printserver"](../printserver.md) for some information about hardware you could use for that.    
      

??? info "What Is Klipper?"

    Long story short: Klipper is an 'alternative' firmware which gives you way more possibilities and even functions for configuring and using your 3D printer. If you don't know what Klipper is, this may be a good start for your research: [All3DP: Klipper](https://www.all3dp.com/topic/klipper)  

??? info "Discussion Thread About Klipper"

    I opened a [discussion thread about Klipper](https://github.com/1coderookie/KobraGoNeoInsights/discussions/6) just in case any further questions arise or in case you want to comment on certain things without doing so by sending me an email. Keep in mind though that I'm not an expert at all, so if you do have specific questions about Klipper, please refer to the [official documentation of Klipper](https://www.klipper3d.org/Overview.html), the [Klipper discourse group](https://klipper.discourse.group/) and/or ask in a special forum like e.g. the [Klipper subreddit](https://www.reddit.com/r/klippers/).  
  
## Requirements
If you want to use Klipper with your printer, you'll need additional hardware for having a host running Moonraker and Mainsail/Fluidd/Octoprint on, which then gets connected to the printer (which has to be flashed with the Klipper firmware of course).  
Please see the chapter ["Printserver"](../printserver.md) for some possible hardware you can use for that.  
  
## Installation
*Credits to reddit user [xpeng121](https://www.reddit.com/user/xpeng121/) who initially posted how to get Klipper running on the **Go** and the **Neo**: [Install Klipper on Kobra Go or Neo](https://www.reddit.com/r/anycubic/comments/10cwm16/install_klipper_on_kobra_go_or_neo/).*  
  
Basically you need to clone the Klipper repository and compile the necessary `klipper.bin` file (aka `firmware.bin`) which you flash onto the mainboard then.  
Referring to the beforementioned post of xpeng121, you need to  

- change the MCU to "HC32F460" and 
- the serial to "Anycubic Kobra"  

during the setup process for creating the `klipper.bin` file.  
For further information about the installation steps please read the chapter ["Installation"](https://www.klipper3d.org/Installation.html) of the official Klipper documentation.  

??? tip "Compiled `klipper.bin` Available"

    I set up a repository where you can download the compiled `klipper.bin` (aka `firmware.bin`): [Klipper4KobraGoNeo](https://github.com/1coderookie/Klipper4KobraGoNeo)  
    Thanks to @[cringegnere](https://github.com/cringegnere) for making the file available!  
    **USE AT YOUR OWN RISK!**

??? tip "Use KIAUH For Installation"

    If you're installing Klipper and frontends on [different hardware like a Raspberry Pi](../printserver.md#how-to-install) and therefore don't use e.g. the MainsailOS image for the RPi, you can use [KIAUH](https://github.com/th33xitus/kiauh), which is an installation script for Klipper, KlipperScreen, frontends like Mainsail and so on.  
    
??? tip "Installing Frontends As A Docker Container"

    If you want to install frontends like e.g. Mainsail as a Docker container, check out the [prind repository](https://github.com/mkuf/prind).

Once you've created the `firmware.bin` file, copy it to the root directory (means, directly onto the card, not in a subfolder!) of your mSD card. I personally would suggest to remove all files from the mSD card and only copy the `firmware.bin` file onto it.  
Then you flash it as you would do with the stock firmware. Means, you turn off the printer, put the card into the cardreader and turn on the printer.  
Note that the screen doesn't update though after the flash procedure is done as the control unit doesn't work with Klipper anymore, it'll stick with the message "Firmware update. Please wait."! So just wait 5-10min to make sure everything had time enough to be installed.  
Then turn off the printer, remove the card, connect your host which has OctoPrint/Mainsail/.. running with the printer using an USB-C cable and turn on the printer again.  
Now you should be able to connect OctoPrint/Mainsail/.. with the printer. If an error message pops up that no connection to the MCU was possible, click on "Restart Firmware" or turn off the printer and switch it on again.  

!!! warning  
  
    - After flashing Klipper's `firmware.bin`, don't try to start printing right away!  
    - Keep in mind that even though the stock mainboard of the **Go** and the **Neo** is the same, you have to adjust certain settings of the file `printer.cfg` depending on your specific model *before* starting to print or calibrate the printer! So don't try to start printing right away!    
    - Proceed with the [configuration checks](https://www.klipper3d.org/Config_checks.html) before you're trying to print anything!      
    - Make sure to adjust the offsets for both the [z-endstop (command `Z_ENDSTOP_CALIBRATE`)](https://www.klipper3d.org/Manual_Level.html#calibrating-a-z-endstop) and the [probe (command `PROBE_CALIBRATE`)](https://www.klipper3d.org/Probe_Calibrate.html#calibrating-probe-z-offset) as well - those are two independent steps and need to be done prior to printing!  
  
## Configuration  
Besides the `firmware.bin` of Klipper (aka `klipper.bin`) you also need a file named `printer.cfg` which contains the specific settings for your model. Please refer to the official Klipper documentation about [configuring Klipper](https://www.klipper3d.org/Installation.html#configuring-klipper).  

You can find preconfigured `printer.cfg` files for both the **Go** and the **Neo** in the belonging repository I set up for this: [Klipper4KobraGoNeo](https://github.com/1coderookie/Klipper4KobraGoNeo).  
For the **Go** you also find a preconfigured file named `printer-anycubic-kobra-go-2022.cfg` within the Klipper repository [here](https://github.com/Klipper3d/klipper/blob/master/config/printer-anycubic-kobra-go-2022.cfg).  
  
Before you can start with the beforementioned tests to see if anything works correctly, you should check and adjust the settings in the file `printer.cfg` if necessary. *Don't start to print right away!*    
  
I won't mention and explain all the settings here as you can just use the official documentation of Klipper to see what each setting means.  
 
  
!!! warning "Adjust The `cycle_time` For The Fans"  

    There is one specific setting I'd like to mention here though as it may cause problems if you don't adjust that. It's the setting `[fan]` for the part cooling fan.  
    So, in the file `printer.cfg` there is a section for the settings of the fans. Klipper is using software PWM by default, the default frequency here seems to be 100Hz.  
    However, users reported dying part cooling fans shortly after switching to Klipper (you can find one of the discussions [here](https://github.com/1coderookie/Klipper4KobraGoNeo/discussions/2)). This problem seems to be related to the default PWM frequency.  
    After investiganting the problem it seems that [the fan runs at 20kHz](https://github.com/1coderookie/Klipper4KobraGoNeo/discussions/2#discussioncomment-5626026) when using the stock firmware as [@xiaopeng12138](https://github.com/xiaopeng12138) found out. So I'd recommend to change the belonging setting for the part cooling fan to the specific "cycle_time" value "0.000050" which is 20kHz.  
   
    This is the belonging section and the setting for the part cooling fan:  
    ```
    [fan]
    pin: PB5
    cycle_time: 0.000050
    ```
    
    
    
## Special Functions   
In the following I'll list some of the special functions which make Klipper so interesting and outstanding compared to the stock firmware, besides the fact that you can adjust the firmware settings to your own needs.  
  
### G-Codes & Macros
Klipper uses extended g-codes and macros, so not all of the 'regular' G-code commands are known and useable within Klipper. See the [g-codes chapter](https://www.klipper3d.org/G-Codes.html) of the official Klipper documentation for an overview of the specific commands.  
You can also find [command templates](https://www.klipper3d.org/Command_Templates.html) in the official documentation.  
  
Due to the fact that Klipper also uses macros, you can set up your own macros to set up certain routines or to e.g. use scripts to do automatic backups of your Klipper configs. 
  
### ABL and Manual Bed Leveling
Of course Klipper supports both ABL and manual bed leveling as well. Please see the official Klipper documentation for more detailed information about this topic, I'll only mention some notes about it here in the following. So before you continue to read here, maybe check out the official Klipper documentation first and read the chapters ["Bed Level Support"](https://www.klipper3d.org/Config_Reference.html#bed-level-support) and ["Bed Level"](https://www.klipper3d.org/Bed_Level.html).  

After executing an ABL sequence, you need to save those results for having them written to your `printer.cfg` file - they *won't* be saved automatically!  
You can either choose an individual name or just save it as "default".  

However, for loading the values and to get ABL to work while printing, you need to add a specific command to your `[gcode_macro START_PRINT]` file to load the bed mesh profile. This has to be added *after* the last G28 (home the printer) command in there. Here's an example of how it looks like with the belonging command for a bed mesh saved as "default".  

```
# Home the printer 
G28

# Load default bed mesh profile
BED_MESH_PROFILE LOAD=default
```

If you chose individual names for different bed meshs (e.g. "mesh1"), you need to name the specific one you want to be loaded then in the abovementioned command (e.g. `BED_MESH_PROFILE LOAD=mesh1`). If you saved the mesh using the "default" name like it's being suggested by the UI, enter the name "default" as shown above.    

You can configure the ABL procedure within your `printer.cfg` as well so that it fits your needs.  
Means, you can change the amount and location of probing points, the probing speed and the amount of probes for each probing point. You can also choose between different probe algorithms. 

As an example, this is the belonging section `[bed_mesh]` in the `printer.cfg` file:  
```
[bed_mesh]
speed: 400
horizontal_move_z: 7
mesh_min: 32, 26
mesh_max: 189, 189
probe_count: 5, 5
relative_reference_index: 13
algorithm: lagrange
```  
Please see the [configuration reference for the bed mesh](https://www.klipper3d.org/Config_Reference.html#bed_mesh) for more detailed information.  

There's even an [approach which probes the specific area you're going to print on](https://gist.github.com/ChipCE/95fdbd3c2f3a064397f9610f915f7d02) before staring the print. 
  
Besides that, you can also use manual bed leveling in addition to the ABL, see the belonging description in the official Klipper documentation [here](https://www.klipper3d.org/Manual_Level.html).  
This is especially useful for people who replaced the stock spacers of the bed with [adjustable spacers](../hardware/bed/#different-spacers) for being able to tram the bed itself as well.  

I'd suppose to also read the description of the function ["screws_tilt_adjust" with the command "SCREWS_TILT_CALCULATE"](https://www.klipper3d.org/Manual_Level.html#adjusting-bed-leveling-screws-using-the-bed-probe), which tells you exactly how much and in which direction you have to turn each screw to tram the bed (after configuring it for your printer) by using the probe.  
  
  
### Pressure Advance
By using Klipper you can take advantage of using a feature called "Pressure Advance". Basically this function looks ahead while printing and adjusts the pressure of the filament, so that the typical over- and underextrusion at the beginning and end of a layer you often experience will be avoided. This feature can't be activated with the current stock firmware and the TMC2208 stepper drivers, so this is actually a huge plus for Klipper.  
Please refer to the official Klipper documentation of [Pressure Advance](https://www.klipper3d.org/Pressure_Advance.html) about how to calibrate and use it.  

### Resonance Compensation: Input Shaping
By using Klipper you can take advantage of using Resonance Compensation and a feature called "Input Shaping". This function compensates certain resonances (after provoking them while measuring the x and y axis), which avoids the artefacts of the printed model called 'ringing' and 'ghosting'. This is especially useful when printing at higher speeds. You can either calibrate it manually or by using additional hardware like ADXL345 acceleration sensors (recommended).  
Please refer to the official Klipper documentation of [Resonance Compensation](https://www.klipper3d.org/Resonance_Compensation.html#resonance-compensation) about how to calibrate and use it.
  
## Stock Control Unit
The stock control unit of both the **Go** and the **Neo** *don't* work with Klipper. So is that going to be an issue? Actually I thought the same initially and that was the only reason which was holding me back switching to Klipper right away at the beginning. Now that I did switch, I can say that I don't really miss the control unit. 

Just as an example:  

- Klipper *keeps* the z-offset, so you don't have to fiddle arount at the control unit for that before each and every print because the stcok-fw forgot your settings once again.   
- Setting temps for e.g. heating up the hotend to change a nozzle or load/unload filament can be done by using Mainsail.  
- Initiating the ABL procedure is also be done thru Mainsail, just like everything else.  

However, if you really do miss the option to control the printer right at that place later, you have several options to do so:  

- You can use your smartphone, tablet or laptop to just open the mainsail.local page at your browser and use the regular Mainsail frontend (which might be a bit 'uncomfortable' when using a smartphone though).  
- You can use an old smartphone or tablet and install [KlipperScreen](https://klipperscreen.readthedocs.io/en/latest/) onto it, which then gives you a nice adapted UI with control buttons.   
  I also set it up, printed a holder for it and mounted it where the original control unit was as shown in the picture below. <br> ![KlipperScreen Smartphone](../assets/images/KlipperScreen-smartphone_web.jpg) <br> Actually I unplugged the phone again as I just control the printer via my computer and the mainsail.local page anyway though. It also kinda bothers me that I have to boot up the phone all the time as I don't leave the printer on 24/7, so I'll probably go with the next solution I'll mention.   
- If you have a Raspberry Pi or other hardware you could connect a touchscreen to (e.g. by using a HMDI port) running for hosting Mainsail, you can add a touchscreen to that and use [KlipperScreen](https://klipperscreen.readthedocs.io/en/latest/). It's the same UI like using a smartphone or tablet.   
  This is actually a quite handy solution if you're using a RPi as you can set everything up in a dedicated case. I'll probably do that as well, just for the pure comfort of not having to take care about switching the smartphone on and off as the display is powered by the RPi. I just didn't want to spend money again when trying Klipper initially, that's why I used an old smartphone in first place.    
       
## Slicers
Due to the fact that Klipper uses extended G-code and macros, there are a few things to be aware of when using certain slicers like Cura, PrusaSlicer, SuperSlicer etc.  
In the following I'll just go over them really quick as it would be too much to discuss the slicers in detail. You'll find many resources online though where yuo'll find more information about them.    

### Cura  
Even though Cura and Klipper work perfectly together, there are a few things to be aware of.  
Certain classic G-code commands aren't directly supported by Klipper as it uses extended G-code and scripts for certain things. As an example the G-code command `M0` (unconditional stop) isn't recognized by Klipper, you'd have to use the extended G-code command `PAUSE` for that.  

Also there are a few functions of Cura which should improve the print quality which interfere with Klipper's own approaches for that (like Pressure Advance or Input Shaping).  

You'll find a good overview of what to be aware of in the tutorial from [All3DP: Cura & Klipper: How to Make Them Work Together](https://www.all3dp.com/2/cura-klipper-tutorial).  
 
However, there's a ["Klipper Settings Plugin"](https://github.com/jjgraphix/KlipperSettingsPlugin) available which adds a category to Cura called "Klipper Settings" and offers Klipper specific settings and features.  
 
### PrusaSlicer and SuperSlicer 
My personal favourites after using Cura for some time. In both slicers you can set the G-code flavor depending on the firmware of the printer (menu "Printer Settings") as shown in the screenshot of SuperSlicer below, so it's already everything set up correctly within the G-code of the sliced files.  
  
![SuperSlicer firmware](../assets/images/klipperfw_superslicer-flavor.png)
  
Both slicers have many functionalities to finetune and control the output - you can even choose between different patterns for the top layer finish. They're both pretty identical overall, yet they differ in certain functions. One of the worth mentioning is a handy set of calibration tools that comes with SuperSlicer. This function actually guides you step by step through the calibration process and allows you to generate calibration models like temperature or retraction towers with individual settings by just a few clicks.  

*I personally would suppose to use the "Arachne Edition" of SuperSlicer (already implemented in the recent version of PrusaSlicer) and enable that function (Print Settings -> Perimeters) as it improves the quality of the printed parts.* 

I can't go into all the possibilities of SuperSlicer and PrusaSlicer deeper though as it's just too complex, so just do a research on it. I'd recommend to give both Slicers a try tho if you're using Cura right now. Especially the calibration tools of SuperSlicer really are worth a try.   

## OctoPrint, Mainsail or Fluidd?
To find out what's the best solution for you, either do a little research on that, watch some YouTube videos or just get another mSD card for your RPi, install e.g. MainsailOS onto it and then just give it a try.  
Due to the fact that I personally use and recommend Mainsail, I'll always refer to it when it comes down to describe or show certain things in this chapter.  

### OctoPrint
OctoPrint is mentioned and referred to at the Klipper page, so you can use it just fine.  
You'd need to SSH to the host (e.g. the RPi) to upload edited files like the `printer.cfg` though - if there isn't a plugin for that which allows you to do so within the interface of OctoPrint (I don't know actually).  
  
### Mainsail
I personally prefer to use Mainsail with Klipper as it's tailored for the usage of/with Klipper and gives you more tools made for Klipper rightaway.  
Just to mention a few here: 

- You can edit the `printer.cfg` and every other file just directly within Mainsail and don't have to SSH to the Raspberry Pi.   
- You already have a heightmap function included which allows you to create and display the meshview after executing an ABL.   
- If your slicer does support it (SuperSlicer does), you can have thumbnails of your models displayed.   
- There's also a G-Code viewer already built in.   
- You have the possibilty to create custom macros for e.g. executing backups and activate them with one click.   
- And much more..   
  
### Fluidd
Fluidd is kinda similar to Mainsail, but it doesn't seem to be maintained as much as Mainsail (afaik). I personally didn't use it, so I can't say anything more to it than do a bit of a research by your own.  
    

