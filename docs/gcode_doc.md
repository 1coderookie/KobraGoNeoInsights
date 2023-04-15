<link rel=”manifest” href=”docs/manifest.webmanifest”>

# G-Code Documentation
If you're new to this whole 3D printing world, then you might want to start reading the article from [All3DP: 3D Printer G-code Commands: Main List & Quick Tutorial](https://all3dp.com/2/3d-printer-g-code-commands-list-tutorial/) to get an overview about what G-code is.  
  
For a complete reference of G-codes, you might want to have a look at the following 'official' sources.  
Of course there are countless sites to find which cover this topic, but the following ones are definitely the one I'd look up first.    
   
## RepRap
The first one to mention is the [RepRap Wiki](https://reprap.org/wiki/G-code), where you can find a general explanation about what G-code is, how it works and all the [G-commands](https://reprap.org/wiki/G-code#G-commands).  
*Within the G-commands section and the specific commands you'll also see tables which firmware (Marlin/Klipper/RepRap/Repetier/Smoothie) supports the specific command.* 
   
## Marlin 
The stock firmware is based on Marlin v2.0.x. You can find a complete reference at the belonging [Marlin website](https://marlinfw.org/meta/gcode/).  
  
## Klipper 
Besides most of the standard G-code Klipper does support (Attention: it doesn't support *all* of the standard commands!), Klipper uses so called "extended" G-code commands and scripts/macros for general status and configuration. These extended commands start with a command which may be followed by one or more parameters. You can find the whole reference at the [Klipper documentation page about G-codes](https://www.klipper3d.org/G-Codes.html).   
