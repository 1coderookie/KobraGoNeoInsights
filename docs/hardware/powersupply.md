<link rel=”manifest” href=”docs/manifest.webmanifest”>

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/U6U5NPB51)  

---  
  
# Power Supply Unit

| Specifications |
|:---------------|
| **Input Voltage**: 115V and 230V AC (choose the correct voltage by setting a switch before turning on the printer!) |
| **Output Voltage**: 24V DC |
| **Power Rating**: 400W, 17A max. |
| **Fuse**: glass tube type, replaceable, located between the power plug and the power switch |
| **Fan**: 24V, 0.10A, 60x60x15mm, model "Cheng Liang CHA6024RL-15B" |  

---

The printer comes with a 400W power supply unit which can take 110V and 230V AC as well.  

![Sticker power supply front](../assets/images/powersupply_label_web.jpg)
![Sticker power supply itself](../assets/images/psu_label_web.jpg)  
  
The powerswitch and the plug are located at the left hand corner in the back at the side of the frame. There is also a fuse integrated in the powerswitch box which you can pull out and exchange if necessary. 

![Powerswitch and fuse location](../assets/images/printer_fuse_web.jpg)  
  
!!! danger 

    Before plugging in the powercord and switching on the printer, make sure that you set the little switch for choosing the voltage to the correct value! You can access it from the back of the printer and either set it to 110V or 230V - so make sure everything is set correctly first! <br> ![Voltage switch](../assets/images/powersupply_voltage-switch_web.jpg)  
  
The housing of the power supply unit is mounted at the back of the base frame underneath the bed. You can spot it from the front when you move the bed completely to the back as the following picture shows.  

![Housing underneath the bed](../assets/images/powersupply_case-front_web.jpg)
  
The following picture shows the location of the PSU (in the back, without the metal cover) and the mainboard (in the front, without the plastic cover) at the **Neo**.  

![Location PSU](../assets/images/neo_underside_mb-psu_web.jpg)  


!!! warning "Warning: Turn Off And Unplug The Machine Before Accessing The Connectors"  

    It must be said at this point that you shouldn't access the PSU's connectors.  
    However, *if* you have to do so, make sure that you switched it off AND that you have *unplugged it*!  

The following picture shows the connectors of the PSU with the three 115V/230V AC wires on the right side (L = brown, N = blue, earth = yellow/green) and the 24VDC on the left side (V+ = red and V- = black).  

![Connectors PSU](../assets/images/PSU_connectors_labeled_web.jpg)  

On the very left side you can see a green LED and right next to it a white potentiometer. With this potentiometer you can adjust the output voltage - so if you measure the voltage at the 24V DC connectors and you don't have 24V there, you can adjust the voltage to the correct value.  


!!! warning "Warning: Don't Open The PSU - And IF So, Don't Touch Any Parts Inside"  

    It must be said at this point that you shouldn't open the PSU.  
    However, *if* you have to do so, make sure to *not touch* any parts on the inside!  
    **There are capacitors built in which can give you severe eletrical shocks even if the machine isn't plugged in or switched on as they store electricity!** 

The following picture shows the PCB of the PSU - the fan isn't plugged in, the belonging connector is the white two-pin connector in the upper left edge area of the board.    

![PSU open](../assets/images/psu_open_web.jpg)  


---

## PSU Fan

The fan is a 60x60x15mm, 24V, 0.10A type ("Cheng Liang CHA6024RL-15B").  
  
![PSU fan](../assets/images/psu_fan_web.jpg) 


---

## MOD: Change The Cover Of The PSU Housing 

!!! warning "Warning: Don't Open The PSU - And IF So, Don't Touch Any Parts Inside"  

    It must be said at this point that you shouldn't open the PSU.  
    However, *if* you have to do so, make sure to *not touch* any parts on the inside!  
    **There are capacitors built in which can give you severe eletrical shocks even if the machine isn't plugged in or switched on as they store electricity!** 


The fan of the PSU is pretty loud, so one of the first things one wants to change is probably to mount a different fan. The fan itself isn't actually that loud though, the noise is mostly created by the way the cover of the PSU housing inhibits the airflow.  

I found a model for a different cover, which was actually made for using a different (bigger) fan. I remixed it and closed that cutout for using the stock fan instead.  
For making sure that nothing will get through those bigger holes, I hot-glued a piece of mosquito net to it from the inside. Instead of drilling holes for the stock fan, I just used two of the existing holes and added some washers for making the screws clamp the fan to the cover.  

*You can find my version at Printables.com: [Anycubic Kobra Go/Neo PSU Cover (Stock Fan!)](https://www.printables.com/model/559590-anycubic-kobra-goneo-psu-cover-stock-fan)*  


The following picture shows the stock cover plate and the 'custom' one (yes, they are the same size, it just doesn't look like that on the picture).  

![Stock vs custom lid](../assets/images/PSU_covers_web.jpg)  

The effect of changing the cover was actually massive, the noise reduction is tremendous - even with the stock fan being used. Suddenly I was able to clearly hear the part cooling fan kicking in when printing, I could barely notice that one before.    
I put a smartphone with an app for measuring the noise on the x-axis part of the baseframe, with the microphone facing the direction of the mounted PSU, then I turned on the printer (so that only the fan of the PSU was actually running). With the stock metal lid being installed it measured 66dB, with the modification it measured 49dB!  

The following picture shows the PSU mounted again.   

![Modded PSU mounted](../assets/images/PSU_altcover-mounted_web.jpg)  

As this lid sticks out a few milimeters and the clearance is already pretty low with the stock setup, I raised the printer a bit by mounting slightly taller feet I had laying around. You can also print some risers which can be plugged onto the existing feet.   
If you do so and you're using Klipper and resonance compensation (aka Input Shaping), keep in mind that the vibrational behaviour will change and you therefore should execute a new resonance measurement. 

**UPDATE:**  
*Since most people apparently don't use the mosquito net and don't use additional washers to mount the fan, I made a new remix of the model where I added struts in the hexagon cutouts as well as two holes for mounting the stock fan.*  
***This is the link of the new model: [Kobra 2 series PSU cover/lid (for stock fan and/or Noctua 6025) ](https://www.printables.com/model/783591-kobra-2-series-psu-coverlid-for-stock-fan-andor-no)*** 

The following picture shows the different versions.  

![New vs old vs stock](../assets/images/PSU_cover_v2_mounted_web.jpg)  

The following picture shows the new version mounted.  

![New version mounted](../assets/images/PSU_covers_v1-v2-stock_web.jpg)  

--- 

## MOD: How To Add A Step-Down Converter For Using 12V Fans 

When you want to add components which need a different voltage than the 24VDC the PSU offers, you can do so by using a step-down converter (or a step-up converter if you need a higher voltage than 24VDC). Simply connect the IN of the converter to one of the free 24VDC connectors of the PSU, dial in the voltage you need and then connect the belonging part to the OUT of the converter.  
The following picture shows a typical "LM2596S" type step-down converter which can be used.  

![Step-down](../assets/images/PSU_StepDown_web.jpg)
 

However, when you want to use e.g. 12V fans which speeds are usually controlled by PWM of the mainboard, you have to connect them differently. The following drawing shows how to proceed in that case, so that the PWM will still work.  

!!! warning 

    The following circuit diagram about how to connect a step-down converter wasn't tested by me yet. It's assumed that the mainboard controls the PWM of the fans by switching the belonging GND of the connector.  

![Step-down converter wiring diagram](../assets/images/stepdown-wiring.png)  


!!! warning "Add An Additional Fuse"

    It is highly recommended to add a suitable fuse to the 24V line, right after the connector of the PSU. If your additional parts like the converter will fail, the fuse will melt - which can save you from burning down your house. 

---

## MOD: Add Additional Fuses To The 24V DC Wiring 

It is highly recommended to add a fuse or a fusebox to each of the 24V lines. Pay attention to choose the correct 'size' of the fuse for the belonging part (ampere rating).  
Doing so can save you from burning down your house if components fail or if the wires somehow overheat and start to burn due to broken strands (which causes a higher resistance) or a shortcut.  

(..need to add pic..)

---

## MOD: Add An External MOSFET  

It's advisable to add an external MOSFET for driving the heated bed (if you like, you can also add one for the heater cartridge as well of course). Even though the MOSFET on the mainboard is sufficient, it's an upgrade worth doing as it not only leads to the fact that the bed will be heated up slightly faster, but it also increases the security of the hole printer.  
The MOSFET of the mainboard doesn't have a heatsink and it *may* caused by overheating due to an excessive amount of current being drawn, especially when using higher bed temperatures. Due to the low clearance between the fan of the moainboard and the ground the printer stands on, the cooling isn't the best as well. When using an enclosure which then heats up as well, cooling gets even worse.  
If the board's MOSTFET dies, you most likely have to get a whole new mainboard then. Even though it's possible to solder a new one onto the board (if you're skilled to do that), additional components might have been harmed.  
To avoid that, it's therefore adviseable to add an external MOSFET which then takes the load - the one on the mainboard only acts as a signal for the external one to switch.  

The 24V DC of the PSU will be connected to the belonging connector of the external MOSFET. The 24V DC line from the heated bed screw terminals will be connected with the belonging connector of the external MOSFET and the 24V DC wires of the heated bed will then be connected to the outlet of the external MOSFET. When the mainboard switches the onboard MOSFET, it will then trigger the external one to switch and lead the current to the heated bed.  
There are a few external MOSFETs on the market, most of them only have a "signal" connector. When using a mainboard with a dedicated 'signal' connector for this, it's then connected to that one. When using a mainboard that doesn't have this 'signal' connector like the one being used at these printers, then it's said to connect the 24V from the bed's connector of the mainboard to that.  

I personally prefer a certain type of MOSFET which also offers a dedicated connector for the 24V line besides the 'signal' connector as shown in the following picture.  

![MOSFET HW-300](../assets/images/MOSFET-HW300_web.jpg)  

The PSU and the wiring of the bedplate are connected to the belonging connectors shown in the following picture: 24V from the PSU belongs to the connector labeled as "Power", the 24V for the wiring of the bedplate belongs to the connector "Hotbed".  

![MOSFET PSU & bed connectors](../assets/images/MOSFET_connectors2_web.jpg)  

The 24V of the bed's connector of the mainboard will then be connected to the belonging connector "Bed" at the MOSFET (positioned next to the connector labeled as "Sig").  

![MOSFET HW-300](../assets/images/MOSFET_connectors1_web.jpg)  

If you're using this kind (or a different kind) of MOSFET, you should check if the manufacturer actually added some thermal paste between the MOSFET and the heatsink - it wasn't the case at the ones I got as shown in the picture below, so that actually completely counteracts the whole installation and makes it obsolete.  

![MOSFET disassembled](../assets/images/PSU_MOSFET_disassembled_web.jpg)


!!! warning "Mind The Polarity"  

    Pay attention to the polarity when connecting the components!  

!!! warning "Add An Additional Fuse"

    It is highly recommended to add a suitable fuse to the 24V line, right after the connector of the PSU. If your additional parts like the converter will fail, the fuse will melt - which can save you from burning down your house.  
    
The following picture shows the MOSFET being mounted to the rear left-hand side of the frame. I made an extension wire for the thermistor wires as well. 
  
As an additional benefit, now that it's mounted back there, the problem with the bed's wires being too short isn't given anymore.  

![MOSFET mounted](../assets/images/psu_mosfet-mounted_web.jpg)  

    
---

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/U6U5NPB51)  
