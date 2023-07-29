<link rel=”manifest” href=”docs/manifest.webmanifest”>  
  
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
  
The following picture shows the location of the PSU (in the back) and the mainboard (in the front) at the **Neo** (should be similar at the **Go**).  

![Location PSU](../assets/images/neo_underside_mb-psu_web.jpg)  
  
The following picture shows the connectors of the PSU with the three 230VAC wires on the right side (L = brown, N = blue, earth = yellow/green) and the 24VDC on the left side (V+ = red and V- = black).  

![Connectors PSU](../assets/images/psu_connectors_web.jpg)  

The following picture shows the PCB of the PSU - the fan isn't plugged in, the belonging connector is the white two-pin connector in the upper left edge area of the board.    

![PSU open](../assets/images/psu_open_web.jpg)
  
The fan is a 60x60x15mm, 24V, 0.10A (Cheng Liang CHA6024RL-15B) type.  
  
![PSU fan](../assets/images/psu_fan_web.jpg) 

---

### Add A Fuse (MOD)

It is highly recommended to add a fuse or a fusebox to each of the 24V lines. Pay attention to choose the correct 'size' of the fuse for the belonging part (ampere rating).  
Doing so can save you from burning down your house if components fail or if the wires somehow overheat and start to burn due to broken strands (which causes a higher resistance) or a shortcut.  

(..need to add pic..)

---

## How To Add A Step-Down Converter For Using 12V Fans (MOD)

When you want to add components which need a different voltage than the 24VDC the PSU offers, you can do so by using a step-down converter (or a step-up converter if you need a higher voltage than 24VDC). Simply connect the IN of the converter to one of the free 24VDC connectors of the PSU, dial in the voltage you need and then connect the belonging part to the OUT of the converter.  

!!! warning "Add A Fuse"

    It is highly recommended to add a suitable fuse to the 24V line, right after the connector of the PSU. If your additional parts like the converter will fail, the fuse will melt - which can save you from burning down your house.  

However, when you want to use e.g. 12V fans which speeds are usually controlled by PWM of the mainboard, you have to connect them differently. The following drawing shows how to proceed in that case, so that the PWM will still work.  

!!! warning 

    The following circuit diagram about how to connect a step-down converter wasn't tested by me yet. It's assumed that the mainboard controls the PWM of the fans by switching the belonging GND of the connector.  

![Step-down converter wiring diagram](../assets/images/stepdown-wiring.png)  

---


