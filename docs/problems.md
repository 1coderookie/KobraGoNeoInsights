<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Problems  
In this chapter I'll list some of the most common problems people seem to have and what to do about them.  
(Note: WIP, so maybe come back another time as well ;) )   

## First Layer Problems / Print Comes Off
If you're having the problem that the print doesn't stick on the plate (even though you really cleaned the PEI plate), then it's most likely that your z-offset isn't right.   
As a rule of thumb you can keep in mind that if the nozzle is too far above the bed, the prints won't stick and (depending on how far above the nozzle actually is) may result in a spaghetti incident (which is filament all over the place) or a blob of fear (which is a large clump of filament built up around the hotend).  
If the nozzle is too close to the bed, the filament will get squished into the plate too much and that will (depending on *how* close the nozzle actually is) provoke clogging as well as it makes it difficult to remove the printed model later.  
*The first layer is crucial for a perfect print, so take your time and get your z-offset dialed in well.*   
See the section ["Z-Offset"](calibration.md#z-offset) for further tips.   
  
Also make sure that you trammed the [x-axis gantry](hardware/axes.md#x-axis-gantry), so that the nozzle has the same distance to the plate across the whole area.  
I'd recommend to get some [adjustable spacers](hardware/bed.md#different-spacers) for the bed for being able to tram the bed itself as well.  
  
Of course you have to pay attention that you really cleaned the PEI plate of the [bed](hardware/bed.md) properly using e.g. simple dishwasher soap (no balm or 'soft' soap as they often contain some oily ingredients) and IPA. I personally prefer silicone remover spray, it just works great. Avoid touching the plate with your bare hands and fingers as that'll leave a tiny amount of grease onto the plate as well.  

Also make sure that you chose the correct temperature of the bed for the filament you're using. For PLA for example it should be around 55°-60°C. If the bed is too hot, then the print won't stick to it either.    

## Holes And/Or Bulges In Layers 
These are mostly signs of under- / overextrusion and/or a clogged nozzle.  

If you observe a **regular pattern** like a vertical line where these gaps and bulges occurs, then it's the z-seam. You could change the setting of your slicer for the z-seam to "random", but that'll lead to random artefacts all over the print. In that case you'll most likely also note these artefacts in other spots of your model where layers start or end. As you can't use Linear Advance with the stock firmware, there isn't that much you can do about this under- and overextrusion an the beginning and the end of a layer besides making sure that you [calibrated the e-steps](calibration.md#calibrating-e-steps) correctly.   
  
If you observe **holes in layers**, or even longer lines in layers where filament is missing, then it's most likely a (partial) clog you're dealing with. So I'd recommend to clean the nozzle by e.g. doing some cold pulls. If the problem gets a bit better but persists, I'd recommend to disassemble the hotend, clean everything, inspect and maintain it and reassemble it again. Also pay attention to the PTFE tube and make sure you reassembled the hotend correctly. Check out the chapter ["Printhead"](hardware/printhead.md) for more informations.   

## Zits And Blobs
If you're printing from an SD card and you notice zits and blobs all over the print in a regular pattern, then turn off the resume function. It makes the printer stop regularly for a tiny moment when saving to the card which results in those artefacts due to the leaking filament. Best would be to not print from the SD card and use an [extra host](printserver.md) running e.g. OctoPrint on.  
  
## 'Rough' Look, Uneven And 'Bubbly' Surface
This is mostly caused by moist filament. When the filament gets heated up in the hotend and gets extruded, the water 'boils' up and the damp releases which results in a pretty 'rough' look. Even tho PLA isn't *that* sensitive to moisture like e.g. Nylon, it still may be moist - even a fresh and sealed spool can be moist (due to the production procedure).  
It's actually kinda difficult for me to describe the look of the surface to give you an exact impression, so I'll keep my eyes open for a good picture I might use to illustrate it.  
The solution for this would be to dry your filament. You can either get yourself one of those (imho overpriced) filament dryers, put the spool in the oven in your kitchen (don't go over 50°C for PLA tho!) or use a food dehydrator. I personally don't use any of that - I just use the well-controlled solution we all already have: the heated bed! Just lay your spool flat onto the bed, cover it with e.g. a cardboard box or so and heat it up to about 45°C. Then let it sit for a few hours.  
When storing your filament, use e.g. some vaccum sealed bags and add dessicant.  

## Layer Shifts And/Or Pushed Off Prints
If you're experiencing layer shifts at either the x- or y-axis, control the position of the wheels and the belt tension.  
If you're experiencing problems in the height or if your prints get pushed off the bed because the nozzle hit them at a certain height, check the wheels of the x-axis gantry as well as the whole z-axis.  
See the chapter ["Axes"](hardware/axes.md) for more informations.  

## Error Messages
..
