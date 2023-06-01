<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Other

Here you can find whatever didn't seem to fit in one of the other chapters.  
  
## MicroSD Card
The printers are shipped with a 8GB microSD card. If you need to replace that card with a new one, make sure to format it as FAT32. Cards up to 32GB should work.  
It might happen though that several cards won't be accepted and the error message "SD init fail" will be reported. In that case, try to completely format it again (full format, not fast format) as FAT32. If that still doesn't solve the problem, try a different card. I personally had to try five(!) different cards of different sizes until the printer finally accepted one (actually the oldest 4GB I had laying around).  
  
## Spool Holder
The spool holder of both models is mounted to the top frame.  

However, due to the construction of the frame itself, the additional weight being put on top of it, the resulting impact of the (changing) weight on vibrations while printing (especially at higher speeds) and because of the poor roll-off behavior of the spool itself I'd suppose to create a spool holder which isn't attached to the printer itself and which uses ball bearings as well.  

If you don't have the space for it or want to keep the spool being attached at the top of the frame because of other reasons, then at least print a holder which uses ball bearings, so that the spool can turn better while the filament gets pulled off of it. Look around at e.g. Thingiverse, there are many models to find.  

??? tip "Boxed Spool Holder"

    If you'd use a box with a lid which closes really well (best would be this kind of plastic box with the silicone sealing in the lid) and put a bag of desiccant in the box as well, you could also can keep the filament dry and dust-free. Just print yourself one of those ball bearing spool holders where you place the spool onto, drill a hole in the side of the box and feed the filament through. Then place it next to the printer or onto a shelf above it and you're good. Putting one of these cheap digital hygrometers in the box as well helps keeping an eye on the actual humidity inside of the box.  

    I personally used a cakebox with a lid which I mounted to an adjustable construction to the wall (cuz I couldn't get my hands on a decent box and ran across that cheap cakebox, so I couldn't resist). The spool itself is held by a bolt with some ball bearing spool holder. Of course I put a bag of desiccant and a cheap hygrometer in there as well.  

    ![Cakebox holder front](../assets/images/cakebox-holder_front_web.jpg)

    ![Cakebox holder open](../assets/images/cakebox-holder_open_web.jpg)

    ![Cakebox holder back](../assets/images/cakebox-holder_back_web.jpg)

??? info "Influence Of The Spool Weight On Vibrations"  

    I personally don't like the spool being attached to the top of the frame. Even though I do see the 'value' of it in saving space around the printer, I personally think that adding 1kg (or even 2kg as some people mount a second one on top as well) to this kind of construction isn't the best idea.  
    
    The construction itself isn't the most rigid one anyway, and the higher the x-axis gantry rises along the z-axis, the stronger the vibrations become which are caused by the moving parts. Adding another kilogram or even more to the top now will enhance this effect, which will become even bigger when printing with higher speeds. Plus, the changing weight of the spool (due to the filament being used) causes a changing pattern of these vibrations.  
    
    By using Klipper and the Input Shaper functionality, we can measure the vibrations and apply certain algorithms to compensate them. But due to the fact that the patterns of these vibrations alter with the changing weight of the spool(s), it's kinda counterproductive to mount the spool(s) on top.  
    As I didn't had an empty and a full spool to test the vibrations for investigating this problem, a friend of mine was so kind to run these tests. Even though he uses a Creality Ender3 V2 Neo and not a Kobra Go or Neo, the results are pretty impressive and allow to assume that the behaviour will be somewhat similar due to the same constructions of the printers.  
    I don't know *how much* this affects the outcome of the printed model in real life at the end, but as we try to eliminate factors that might have a negative effect anyway, I just wanted to show you this for making you aware of it.  
    So the following images show the outcomes of the Input Shaper measurements with an ADXL345 sensor being used. The first two images show the vibrations of the x-axis test with a full 1kg spool and an empty spool, the next two images show the belonging results for the y-axis.  
    
    ![Full X](../assets/images/Full_X.png)  
    
    ![Empty X](../assets/images/Empty_X.png) 
    
    ![Full Y](../assets/images/Full_Y.png)
    
    ![Empty Y](../assets/images/Empty_Y.png)
    
    
  
## Mods
In the following I'll list mods or STL files I found which could be interesting in general. Keep in mind that they mostly should fit for both printers in general due to the identical design and contruction itself, so (right now) I don't separate them into **Go** and **Neo** like usually.    

- [Gregg Bennett](https://www.printables.com/de/social/221278-greg-bennett) created [risers](https://www.printables.com/de/model/394918-anycubic-kobra-neo-risers) which slip on the feet of the printer to rise up the whole construction allowing a better airflow for the fans of the mainboard and the power supply unit.  
- [Lohtex](https://www.printables.com/de/social/546846-lohtex) created [bed spacers](https://www.printables.com/de/model/376710-anycubic-kobra-go-bed-spacers) which could be used to replace the stock ones if they're completely different in their size.  
  However, keep in mind though that also the bottomside of the bed will get warm and therefore the spacers might become deformed if using PLA, so make sure you're printing them with e.g. ABS. Also keep in mind that prints aren't 100% correct in their dimensions, so that printing spacers won't be the final solution to get your bed perfectly trammed.   
- [Stellar5](https://www.printables.com/de/social/407998-stellar5) created a [purge/drip tray](https://www.printables.com/de/model/351007-anycubic-kobra-go-purgedrip-tray) which can be mounted to the frame and prevents filament from falling underneath the printer while heating up in home position.
- [ZAch Goldberg](https://www.printables.com/de/social/457330-zach-goldberg) created a [sidemount](https://www.printables.com/de/model/334261-anycubic-kobra-go-side-mount) which can be mounted underneath the holder of the control unit and offers some mounting options for e.g. a Raspberry Pi.   
