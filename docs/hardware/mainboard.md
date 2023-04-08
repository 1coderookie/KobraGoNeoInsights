<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Mainboard

## TriGorilla V_3.0.6 (Stock) 
  
The stock mainboard of both the **Go** and the **Neo** is the "TriGorilla V_3.0.6" (it's the same board, it's just flashed with the respective fimware of either model).  
It is a 32bit mainboard with a Huada HC32F460 KCTA ARM Cortex-M4 with 192KB SRAM and 512KB Flash. The speed  of the ARM chip is listed as 200MHz by the manufacturer, Klipper states 168MHz though. The mainboard comes with TMC2208 silent stepper drivers soldered onto the board. It offers a microSD card reader, a USB-C connector and a 10 pin connector for adding the control unit. It operates at 24V DC.   
  
![Mainboard TriGorilla front](../assets/images/mainboard_front_web.jpg)  
  
![Mainboard TriGorilla back](../assets/images/mainboard_back_web.jpg)  

![Mainboard labeled](../assets/images/mainboard_complete_labeled_web.jpg)
  
The following picture shows the fan of the mainboard.  

![MCU fan](../assets/images/fan-mainboard_web.jpg)  

  
??? tip "Need To Get A New Mainboard?" 
  
    - As both the **Go** and the **Neo** use the same mainboard, you can just get yourself the mainboard for the **Go** if you e.g. own a **Neo** and can't get a mainboard for it (at the time of writing this, Anycubic only offers the mainboard for the **Go** in their shop) or if you find a seller but he charges more for the **Neo** version. You just need to flash the specific firmware for the **Neo** before using the printer. 
  
??? example "Add Ferrules To The 24V Wires!" 

    - *It's advisable to cut off the soldered tips of the wires without a plug (power supply and heated bed) and add ferrules to them.*  
    When you are screwing down the soldered tip inside the clamp, the solder will get cracked a bit and may get deformed a bit as well. When the wire gets warm due to the current and the solder gets softer, the contact may become loose which could lead to malfunction or even cause fire in the last consequence. So it's always a good idea to just use proper ferrules. <br> ![Ferrules instead of soldered tips](../assets/images/mainboard_ferrules_web.jpg)  
  
!!! warning "Avoid Shortcuts!"  
  
    - *Shortcuts coming from the cartridge heater for example can/will damage your mainboard, so be careful to never cause a shortcut somehow!*  
    A common misbehaviour is to clean the nozzle with a little brass brush during the print process or while everything is heating up. Also grabbing the heater block to e.g. change the nozzle while everything is heating up and electrical current is flowing is another common mistake. When using pliers to hold the heater block, the tips of the pliers may touch the contacts of the wires at the cartridge heater and you cause a shortcut. As a result you can/will get blown up part at the mainboard, like the melted part "D4" for example as shown in the picture below. <br> ![Melted D4 caused by a shortcut](../assets/images/mainboard_melted-D4_web.jpg)  
  
---
  
## SKR3 (Mod)
??? question "Got a SKR3?"  

    Did you already replace the stock mainboard with a BTT SKR3? If so, it would be great if you'd share your knowledge and contribute a little description and probably a picture of the built in board. <br> Just send me an email to <br> `3dneo (at) quantentunnel.de` <br> Thank you!
    
