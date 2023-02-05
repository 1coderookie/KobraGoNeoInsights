<link rel=”manifest” href=”docs/manifest.webmanifest”>

# G-Code Documentation

Here you can find links to comprehensive and 'official' sources about the G-codes. Of course there are countless sites to find which cover this topic, but the following ones are definitely the one I'd look up first.    
   
## RepRap
The first one to mention is the [RepRap Wiki](https://reprap.org/wiki/G-code), where you can find a general explanation about what G-code is, how it works and all the [g-commands](https://reprap.org/wiki/G-code#G-commands).  
*Within the G-commands section and the specific commands you'll also see tables which firmware (Marlin/Klipper/RepRap/Repetier/Smoothie) supports the specific command.* 
   
## Marlin 
You can find a complete reference at the belonging [Marlin website](https://marlinfw.org/meta/gcode/).  
  
## Klipper 
Besides most of the standard G-code Klipper does support (Attention: it doesn't support ALL of the standard commands!), Klipper uses so called "extended" G-code commands and scripts for general status and configuration. These extended commands start with a command which may be followed by one or more parameters (e.g. using the command `SET_FAN_SPEED FAN=config_name SPEED=<speed>` you can set the desired speed of a certain fan).  
You can find the whole reference at the [Klipper documentation](https://www.klipper3d.org/G-Codes.html) page about G-codes.  
