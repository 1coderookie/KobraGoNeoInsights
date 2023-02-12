<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Stock Firmware (Marlin Based) 
The official stock firmware for both models is based on the [Marlin firmware](https://marlinfw.org/).  
  
You can either  

- download the necessary `firmware.bin` file at [Anycubic's firmware & software page](https://www.anycubic.com/pages/firmware-software) for the 
    - [Kobra Go v1.3.4](https://cdn.shopify.com/s/files/1/0245/5519/2380/files/Kobra_Go_v1.3.4_firmware.rar?v=1666159978)
    - [Kobra Neo v1.3.3](https://cdn.shopify.com/s/files/1/0245/5519/2380/files/Kobra_Neo_v1.3.3_firmware.rar?v=1675912197)  
- download the source code from their specific GitHub repositories to compile your own:  
    - [Kobra Go GitHub repository](https://github.com/ANYCUBIC-3D/Kobra_Go)  
    - [Kobra Neo GitHub repository](https://github.com/ANYCUBIC-3D/Kobra_Neo)  
     
In case you want to build and compile your own `firmware.bin` file, you can follow the instructions of @[jojos38](https://github.com/jojos38) [Tutorial: How to build Anycubic Marlin sourcecode into a firmware.bin](https://www.reddit.com/r/anycubic/comments/y2waxu/tutorial_how_to_build_anycubic_marlin_source_code/).
  
## Update Procedure

To update the firmware of your printer, copy the file `firmware.bin` onto the microSD card.  
Turn off the printer and plug the card into the cardreader which is located at the front of the frame (next to the USB connector). The card must be inserted with the contacs facing upwards.  
Then turn on your printer. You'll see a black screen with "Updating Firmware..." displayed.  
After a certain time the Anycubic logo will appear and shortly after that the regular main screen will appear.  
Shut down the printer again and take out the card (push it in a bit to unlock it and make it come out a bit, then just pull it out).  
Turn on the printer again, go to "Menu" and then "About" and check if the correct firmware version is displayed.  
If so, everything is fine. If not, check if you really copied the correct version onto the card and proceed the update again.   

---  
  
# Mods
There are a few compiled versions and also mods of the original firmwares available out there. Please let me know if you find more so that I can link to them. 
  
!!! warning

    Use at your own risk!  

  
## Go  
  
- @[Auburn](https://github.com/Auburn) offers a [modified Kobra **Go** firmware](https://github.com/Auburn/Kobra_Go) 
  
## Neo

- @[cringegnere](https://github.com/cringegnere) offers [his *compiled* version of the the *original* Kobra **Neo** firmware](https://github.com/cringegnere/Kobra_Neo/releases/tag/v1.3.3_original)
- @[sjorge](https://github.com/sjorge) offers a [modified Kobra **Neo** firmware](https://github.com/sjorge/Kobra_Neo_Fw)
