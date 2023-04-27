<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Problems  
In this chapter I'll list some of the most common problems people seem to have and what to do about them.  
(Note: WIP, so maybe come back another time as well ;) )   

## First Layer Problems / Print Comes Off
If you're having the problem that your first layer isn't consistent across the plate and/or the print doesn't stick on the plate (even though you really cleaned the PEI plate), then it's most likely that your [z-offset](calibration.md#z-offset) isn't right and/or you're dealing with a warped or tilted [bed](hardware/bed.md) and therefore experience certain areas where the distance between the nozzle and the plate will vary too much.   
  
- As a rule of thumb you can keep in mind that if the nozzle is too far above the bed, the prints won't stick and (depending on how far above the nozzle actually is) may result in a spaghetti incident (which is filament all over the place) or a blob of fear (which is a large clump of filament built up around the hotend).  
  If the nozzle is too close to the bed, the filament will get squished into the plate too much and that will (depending on *how* close the nozzle actually is) provoke clogging as well as it makes it difficult to remove the printed model later.  
  *The first layer is crucial for a perfect print, so take your time and get your z-offset dialed in well.*   
  See the section ["Z-Offset"](calibration.md#z-offset) for further tips.   
- Also make sure that you trammed the [x-axis gantry](hardware/axes.md#x-axis-gantry), so that the nozzle has the same distance to the plate across the whole area. This might not be enough though if you're encountering a tilted bed along the y-axis, so check the next listing. 
- If you're using the rigid stock spacers (the black round parts between the bedplate and the bedgantry) that came with the printer, then it's most likely that they're not all of the same height (at my Neo they *all* had a different height!). Of course that'll lead to a somewhat warped or tilted bed.  
  Before you start fiddling around with that either trying to get them all to the same height by e.g. sanding them down or by putting some sort of thin material underneath them to eaglize the height, I'd recommend to just get some [adjustable spacers](hardware/bed.md#different-spacers) for the bed for being able to tram the bed itself as well.  
- I'd recommend to check the bedmesh values (query M503 through a program like e.g. OctoPrint, Pronterface to get them listed) or use e.g. OctoPrint for getting a meshview out of it. By doing so you can see how 'flat' and trammed the bed is.  
  If it's tilted, tram it.  
  If it's warped or bent (like e.g. a bow) or if you're having certain spots which seem to be bulges or dents or if you have a certain area which is lower, you can use *Kapton tape* to egalize those areas/spots. Just take off the PEI plate, stick pieces of the Kapton tape right onto the magnetic foil of the bed, put the PEI plate back on and do another ABL sequence. Then check the values or the meshview again. By doing so step by step, you can get yourself a bed as flat as possible. Minor deviations should be compensated by the ABL function later when printing.  
  See the chapter ["Bed"](hardware/bed.md) (mind the expandable textboxes) as well for more informations.  
- Wiggle the bed and check if it moves in the vertical plane. If it does, check the bolts and nuts of the bedgantry and [check the v-slot wheels for perfect position](hardware/axes.md#v-slot-wheels-position_2). Most likely the wheels (or at least one) are a bit too far away from the aluminum frame. Adjust the position of the wheels then, but pay attention to not adjust them too tight as well.  
- Of course you have to pay attention that you really cleaned the PEI plate of the bed properly using e.g. simple dishwasher soap (no balm or 'soft' soap as they often contain some oily ingredients) and IPA to make the prints stick to it. I personally prefer silicone remover spray, it just works great.  
  Avoid touching the plate with your bare hands and fingers as that'll leave a tiny amount of grease onto the plate as well.  
- Also make sure that you chose the correct temperature of the bed for the filament you're using. For PLA for example it should be around 55°-60°C. If the bed is too hot, then the print won't reliably stick to it either.   
 

## Stringing
Stringing can be caused and affected by different factors and therefore can't always be avoided by adjusting retraction settings only. You can find countless articles about it, so maybe do a little research on it.  
Based on my own experiences, the following variables besides the retraction settings should be taken into account as well as one probably doesn't think about them in the first place:  
    
- The type of filament (PLA, ABS, PETG, TPU).  
- The quality of filament.  
- The moisture of filament: moist filament increases stringing.  
- The printing temperature: too high as well as too low printing temperatures cause stringing.  
- The [feeder gear pressure](hardware/printhead.md#extruder-feeder): if it's too low, the gear can't grab the filament reliably and therefore can't retract reliably.  
- The state of the feeder gear: if the teeth of the feeder gear which grabs the filament is kinda clogged due to debris of the filament, then it might slip as well.   
- The quality and the state of the [nozzle](hardware/printhead.md#nozzle): low-quality nozzles as well as worn out and/or slightly clogged nozzles can increase stringing. Also the diameter of the nozzle has an impact as it determines how much filament gets extruded.   
- The quality and the state of the PTFE tube inside of the heatbreak (Neo) or the bowden tube overall (Go).  
  As an example: stringing got way better after I replaced the stock PTFE tube with a Capricorn one, it seems that the lower friction of the Capricorn tube affected the retraction capability. Also a slightly clogged and/or deformed tip of the PTFE tube affected this a lot.  
- [Retraction settings](calibration.md#retraction-settings), so the retraction *distance* and the retraction *speed*.  
  Even though one would usually assume that higher values should/would be better to avoid or at least deal with stringing, it's not always the case. So instead of e.g. going higher than 1mm retraction distance at the direct drive of the Neo (which would provoke clogging), go much lower and see how it goes.  
  This seems to be affected not only by the *type* of filament (flexible filament like TPU needs completely different settings than pretty hard filament like PLA for example), but also by the *quality* of filament. Often cheap filament is lighter and more flexible than high quality filament and therefore it needs lower retraction settings overall to achieve good results.   
- The object one wants to print: certain objects just caused stringing, even tho I usually printed without any stringing. I'd recommend to print retraction towers with two cone-shaped towers as well, to get the different diameter into account as well.  
- The settings of the slicer, like wiping, z-hop, outer- vs. inner perimeter and so on. There are many articles and videos about this topic, so I'd recommend to do some research on it for your specific slicer.  
    

## Holes And/Or Bulges In Layers 
These are mostly signs of under- / overextrusion and/or a clogged nozzle.  

- If you observe a **regular pattern** like a vertical line where these **gaps and bulges** occur, then it's the z-seam. You could change the setting of your slicer for the z-seam to "random", but that'll lead to random artefacts all over the print. In that case you'll most likely also note these artefacts in other spots of your model where layers start or end.  
  As you can't use Linear Advance with the stock firmware, there isn't that much you can do about this under- and overextrusion an the beginning and the end of a layer besides making sure that you [calibrated the e-steps](calibration.md#calibrating-e-steps) correctly. You might be able to tweak some settings in your slicer though and optimize it a bit.    
- If you observe **holes in layers**, or even longer **lines in layers where filament is missing**, then it's most likely a (partial) clog you're dealing with.  
  So I'd recommend to [clean the nozzle](hardware/printhead.md#cleaning-the-nozzle) by e.g. doing some cold pulls. If the problem gets a bit better but persists, I'd recommend to disassemble the hotend, clean everything, inspect and maintain it and reassemble it again.  
  Also pay attention to the PTFE tube and make sure you reassembled the hotend correctly.  
  Check out the chapter ["Printhead"](hardware/printhead.md) for more informations.   

## Zits And Blobs
If you're printing from an SD card and you notice zits and blobs all over the print in a regular pattern, then turn off the resume function. It makes the printer stop regularly for a tiny moment when saving to the card which results in those artefacts due to the leaking filament.  
Best would be to not print from the SD card and use an [extra host](printserver.md) running e.g. OctoPrint on.  
  
## 'Rough' Look, Uneven And 'Bubbly' Surface
This is mostly caused by moist filament. When the filament gets heated up in the hotend and gets extruded, the water 'boils' up and the damp releases which results in a pretty 'rough' look. Even tho PLA isn't *that* sensitive to moisture like e.g. Nylon, it still may be moist - even a fresh and sealed spool can be moist (due to the production procedure).  
It's actually kinda difficult for me to describe the look of the surface to give you an exact impression, so I'll keep my eyes open for a good picture I might use to illustrate it.  You can check if the filament is (way) too moist by extruding with the nozzle up in the air. Watch the string of melted filament which comes out of the hotend, right at the nozzle. Does it seem to be 'bubbly'? Do those bubbles even pop? If so, then it's definitely too moist.  

The solution for this would be to dry your filament. You can either get yourself one of those (imho overpriced) filament dryers, put the spool in the oven in your kitchen (don't go over 50°C for PLA tho!) or use a food dehydrator. I personally don't use any of that - I just use the well-controlled solution we all already have: the heated bed! Just lay your spool flat onto the bed, cover it with e.g. a cardboard box or so and heat it up to about 45°C. Then let it sit for a few hours.  
When storing your filament, use e.g. some vaccum sealed bags and add dessicant.  

## Dark Pieces Of Melted Filament
If you see dark (like honey or even brown or black) pieces of melted filament somewhere on your print, then this is a sign of a clogged or (most likely) even wrong assembled hotend. It's caused by filament which stays in the hotend somewhere, gets burned and when it comes out it's dark. Most of the time there is a little gap where the filament gets collected, like between the nozzle and the PTFE tube when not being cut or assembled properly.  
  
The solution here would be to do some cold pulls first to get as much filament out as possible, then disassemble the hotend and inspect it. Pay attention to the PTFE tube as well. When reassembling, make sure everything sits in place as it should and the tube is long enough to hit the nozzle (and at the Neo it also has to go up to the extruder gear as well). The tube needs to be cut perpendicular as well. *If any gap occurs, the melted filament will stick there again and get burned and the problem will occur again.*    

## Layer Shifts And/Or Pushed Off Prints
If you're experiencing layer shifts at either the x- or y-axis, control the position of the wheels and the belt tension.  
If you're experiencing problems in the height or if your prints get pushed off the bed because the nozzle hit them at a certain height, check the wheels of the x-axis gantry as well as the whole z-axis.  
See the chapter ["Axes"](hardware/axes.md) for more informations.  

## Error Messages
..