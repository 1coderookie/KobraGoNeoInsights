<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Printers
The Anycubic [Kobra **Go**](https://www.anycubic.com/collections/3d-printers/products/kobra-go) and [Kobra **Neo**](https://www.anycubic.com/collections/3d-printers/products/kobra-neo) are pretty much identical FDM bed slinger printers, the only *real* difference seems to be the different type of extruder and the different home position:  
  
- The Kobra **Go** uses a bowden drive extruder ([user manual Kobra **Go**](https://cdn.shopify.com/s/files/1/0245/5519/2380/files/Anycubic_Kobra_Go_User_Manual_221102_V0.0.4.pdf?v=1667812989)), the home position is the front right corner of the bed.  
- The Kobra **Neo** uses a direct drive extruder ([user manual Kobra **Neo**](https://cdn.shopify.com/s/files/1/0245/5519/2380/files/Anycubic_Kobra_Neo_20230109_V0.1.0_English.pdf?v=1673859391)), the home position is the front left corner of the bed.  
  
??? tip "Be Aware of Different Settings"

    Because of the different types of extruder systems and a different home position you have to be aware of certain settings like in the slicer and also in alternative firmware like Klipper.  
    In the *slicer* (e.g. Cura) you need to keep an eye on the rectration distance, which is set to a higher value at the **Go** (~6mm) than at the **Neo** (~1mm). This is especially important when you're asking in a forum and get tips from other users - they might not be the right ones when it comes down to retraction distance!  
    If you want to use other *firmware* than the stock one like Klipper and you're looking out for about how other users set the configuration, be aware of the fact that the **Go** has its home position with the printhead above the right front corner and the **Neo** at the left front corner of the bed (which is driven completely to the back at that time).    
  
The **Go** comes completely unmounted so you have to mount everything together by yourself. Therefore the price of the **Go** usually is a bit lower than the price of the **Neo**.  
The Kobra **Neo** comes pre-mounted, you only have to mount a few parts like the 'upstanding' frame onto the base frame.  
  
See [Anycubic's support page](https://www.anycubic.com/pages/firmware-software) or [Anycubic's support page of the blog](https://www.anycubic.com/blogs/news/all-you-need-to-know-about-kobra-series) of the Kobra series to find manuals, firmware, video tutorials and more of both the **Go** and the **Neo**.    
  
The following list gives an overview of the most important specifications:    
  
- Printing dimensions: 250 x 220 x 220 mm (HxWxD)  
- Machine dimensions: 490 x 445 x 443 mm (plus filament holder mounted to the upper frame = approx. 630 mm height) 
- Machine weight: approx. 7.5 kg  
- Aluminum frame  
- X-axis and Y-axis: belt driven, belt tension can be adjusted by knobs  
- Z-axis: single threaded rod  
- Printing speed: ≤100 mm/s (Max speed)  
- Control panel: 2.4" LCD screen with a control knob  
- Mainboard: TriGorilla V_3.0.6, 32bit, TMC2208 silent stepper drivers (soldered), microSD card reader, USB-C connector 
- Extruder / feeder system:  
    - Bowden separated at Kobra **Go**  
    - Direct drive at Kobra **Neo**  
- Printing platform: 8.7 x 8.7 inches / 220 x 220 mm  
- Heated and magnetic bed with removable PEI-coated spring steel plate (one-sided coated at **Go**, double-sided coated at **Neo**)  
- Hot bed temperature: ≤ 230 °F / 110 °C  
- Bed leveling: "Anycubic LeviQ", which is a 25-point automatic bed leveling  
- Printing material: PLA / ABS / PETG & TPU (optional housing recommended for certain material)  
- Single nozzle in a V5 heater block, filament diameter 1.75 mm  
- Comes with a E3D V6 compatible 0.4 mm brass nozzle which is replaceable  
- Nozzle temperature: ≤ 500 °F / 260 °C  
- Optional filament run-out detection sensor  

Because a picture says more than thousand words - let me introduce you to my first 3D printer ever, the Kobra **Neo** in it's home position:  
![Kobra Neo](assets/images/printers_neo_web.jpg)

