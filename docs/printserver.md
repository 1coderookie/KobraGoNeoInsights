<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Printserver
Sooner or later you'll come to the point that you want to use additional software like [Octoprint](https://octoprint.org/) or so to control your printer.  
Yes, it's not necessary as you can control it directly using the printers control unit and it's advisable to stay in the same room and monitor the printing process to be able to intervene as soon as something is going wrong - but we all know how it is..  
So having the possibility to not only send gcode commands directly to the printer but also to use certain plugins or additional hardware to e.g. monitor the printing process isn't the worst idea.  
In case you're already using some kind of home automation software, you could also send yourself a fancy notification when the printing process is done.  
Sounds tempting? Ok, so you'd need additional hardware for that to run the desired software on. So let's have a look what might be an interesting and reasonable priced solution for that.  
  
## Raspberry Pi
When you start looking around for a system the desired software should run on, the first thing you'll come across surely will be the Raspberry Pi (in the following named as "RPi").  
The RPi is a little computer which became pretty famous since it entered the market.  
It's a Broadcom SoC 64bit ARM system with LAN (and WiFi within the newer versions) and a microSD card reader onboard which keeps the desired OS. It offers GPIOs to directly connect hardware like sensors to it and it draws only a little amount of power.  
Pretty much all of the regular software for 3D printing like the beforementioned [Octoprint](https://octoprint.org/) or [Mainsail](https://docs.mainsail.xyz/) or so are available as specific RPi image which makes it pretty easy and flawless to install even if you're not an expert. Just install the [Raspberry Pi Imager](https://www.raspberrypi.com/software/), create the specific image, copy it to a sufficient microSD card and you're good to go - the installation will take a few minutes only.  
And as handy as it is - it might not be the best solution, especially these days.  
  
Prices for the RPi went up to a ridiculous level (afaik at least in Europe and the US) - *if* they're even available at all.  
Also you don't want to get yourself an old RPi2B for example, it should be a RPi3B at least (referring to Octoprint a RPi Zero 2W also works, it uses the same Broadcom SoC like the RPi3) - a RPi4 would be even better and advisable. Not only because of the pure processor power or the RAM - both is sufficient even with the RPi3 for example, but mostly because of the reason how the USB sockets are connected to the CPU. Afaik, up until the RPi3 the Broadcom BCM2837 only offers one(!) USB port itself. This one port is split up by using a SMSC LAN9514 hub chip to get four USB connectors out of it *and* it also uses the LAN port.  
  
If you're asking yourself now "What the heck is this guy talking about - I have four USB connectors available there, so what's the problem?" - well, let me try to explain it to you very simple:  
Imagine you connect your RPi3 to a monitor and plug in a mouse, keyboard, your 3D printer and a webcam to the USB sockets and maybe you also use the LAN connection (because everybody who knows wireless uses wires ;) ). Then you start your printing process sending the gcode file to the printer and start to observe the printing process using the camera. Then all of the informations are running across the same one and only USB port of the SoC (the main CPU). That means that most likely you'll find yourself noticing some kind of stuttering during the printing process and/or the stream of the webcam.  
That doesn't occur because of a lack of RAM or CPU power (what people use to assume) - that occurs because of the architecture and the bottleneck "one USB port at the SoC".  
So you can see it like a four lane street going down to one lane - as soon as there's (much) traffic on all of those four lanes, you'll get stuck in the traffic where it goes down to one lane.  
So does that mean you shouldn't use a RPi? No, not at all - just be aware of the fact that it might not be the best solution for your money. It works fine if you don't use the time lapse function of Octoprint or if you can avoid using an additional webcam at all. 
  
??? tip "RPi and a (Web-)Cam"

    However, if you're already running a RPi(3) and face those kind of problems as mentioned above which may be caused by a connected webcam to the RPi, I'd suggest the following:  

    - Switch to a cheap/old type of webcam which only offers a low resolution like 480p (640x480). You don't need 4K to see what's going on and by using a low resolution you can at least decrease the amount of informations that has to run through the mentioned bottleneck.  
    - Don't create a time lapse video as it really is consuming a lot of processor power and RAM.
    - Get rid of the USB cam and set up an IP cam (WiFi/LAN) instead which isn't connected to the RPi. Up to me this is even a better solution then downgrading the webcam as the RPi doesn't have to deal with the data from the IP cam at all. If you like to tinker and don't mind the probable effort, get yourself one of those cheap ESP32-CAM modules and set it up. Or just go for a cheap WiFi/LAN camera.   
    - If you're already using a RPi3/4 with a RPi cam and don't have a sufficient housing for that yet, have a look at the thing from [A_Leh](https://www.thingiverse.com/A_Leh): [Anycubic Vyper/ Kobra Raspberry 4b (+3b) housing with camera attachment](https://www.thingiverse.com/thing:4994599)
    - Last but not least: make sure you're using a good and fast microSD card and a good USB cable which connects the RPi to the printer.

## Other SoC Boards
If you can't or don't want to get an RPi but still want to stick to one of those tiny tinker units, you can check out the market what's available and compareable to a RPi, like an "Orange Pi", a "Le Potato" or so on.  
I'm not going into further details here as I personally don't use them and prefer Thin Clients mentioned further below.  

## Old Android Devices
Yes, you've read correct: certain software could also be installed onto your old Android device like your smartphone or your tablet. Namely especially Octoprint has to be mentioned here.  
I won't go deeper here though due to my lack of experience with this solution - you'll find many informations about this around the web. One of those sources of informations I'd like to mention though is the video of [Thomas Sanladerer: How to run OctoPrint on your phone!](https://www.youtube.com/watch?v=74xdib_-X38) and the GitHub repository of [feelfreelinux: octo4a](https://github.com/feelfreelinux/octo4a).  
  
??? tip "USB OTG"

    - I'd like to mention one of the probably biggest issues you might encouter: charging the device while having it connected to the printer at the same time. <br> While it shouldn't be a problem if you're having a device with a separate power plug or wireless charging, it might become a problem if you'd have to use some kind of solution which splits up the line for USB charging and OTG - not all devices work with that. <br> Additionally, I personally would be concerned about probably harming the printers mainboard due to a faulty cable or whatever. 
    - What also should be mentioned here as a **warning** is the fact that devices which are connected 24/7 to the charger might be a huge hazard as the battery could catch fire or even blow up. So keep that in mind if you're tempted to go this way.
  
## Old "Regular" Hardware 
If you have old hardware laying around like a laptop or so, you can also use that. Don't worry - even if it's pretty old in most of the cases it still would be sufficient. Install a Linux OS onto it and then install the desired software.  
You'll find some tips about how to get the software installed further below.  
  
However, as much as I appreciate and love to re- and upcycle old hardware in general, one thing has to be mentioned: the amount of power they're drawing due to their old and mostly energy inefficient chipsets.  
It might not really come into account if your prints last only a few hours and after finishing them you turn everything off. But as soon as you think about running those machines pretty much 24/7 you should keep in mind that they might draw a lot of power which sums up at the end. Right now here in Germany we're paying about 0,40€/kWh, so it really matters just looking at the financial side of that - not to mention the ecological aspect.    

## Thin Clients
Now - get ready for the real deal: Thin Clients!  
Ok, might be a bit exxagerated, but I really *love* those fellas.  
  
If you've never heard of them, let me give you a quick introduction:  
Thin Clients are computers which are often used by companies for e.g. setting up workstations for their employees or to have some kind of information desk or screen running somewhere.  
They have a small build factor, don't draw an excessive amount of power and usually come with connectors for LAN, USB, a monitor and so on.  
Especially newer models (like only a few years old) have hardware built in which would be even powerful enough to replace your daily driver for surfing the web, watching videos, writing stuff and so on. Generally speaking: the newer and bigger they are, the more they have to offer usually - I'm talking about energy efficient quadcore CPUs here and the possibility to put in up to 32GB or even 64GB of RAM, swapping in a SSD (2.5", m2.SATA or m2.NVMe - that often depends on the age actually) and even run virtual machines (tip: [ProxmoxVE](https://www.proxmox.com/en)) or containers (tip: [Docker](https://www.docker.com/)). Of course you could also just install a LinuxOS like Ubuntu or a headless Ubuntu Server and install your desired software directly there.  
  
The (imho great) point is: you can get a pretty powerful and energy efficient machine which is a true x86 platform for just a little amount of money as companies use to sell them pretty cheap most of the time. You probably have to look out for a certain model a bit longer sometimes as they use to be sold out quite fast, but it would be worth it.  
Anyway - even if they're usually available for a fair price, I want to mention that it's advisable to not buy the very first offer you can find. Even though they're still cheap most of the times compared to a RPi4 for example, certain companies know about the potential and that people like to use them for tinkering around, so some companies call for much higher prices than others.  

??? tip "Tips About Thin Clients"  

    - There are many different Thin Clients from different manufacturers available out there - a good site I'd like to recommend to gather around and check out the specs of different Thin Clients is [ParkyTowers](https://www.parkytowers.me.uk/thin/).  
    - If you're looking for something really small, maybe look out for a Dell Wyse 3040 or 3020. They do have limited power and RAM possibilities compared to bigger Thin Clients, but for just acting as a headless print server instead of a RPi they're powerful enough.   
    -  I personally like the HP Thin Client T6x0 series as you can upgrade them really well. The higer the number, the newer the model and the more powerful, energy efficient and compatible with modern parts it is (e.g. T610 uses a 2.5" SSD & DDR3 SO-DIMM RAM while the T630 uses a m2.SATA SSD & DDR4 SO-DIMM RAM). The 'downside' of them (if you even want to call it that way as they're still pretty small) is the bigger housing.   


## NAS / Server
If you have a NAS or a server up and running already, you could also install the printing software onto that. In this case I'd assume that you already know what you're doing and that you don't need any advise though.   
 
## How To Install
So in case you want to use hardware like the abovementioned Thin Clients, you probably don't know how to set it up and install the software. Right now I'd like to encourage you to search the web as there are many step by step guides and also videos out there about how to do it.  
However, I'd like to mention [Kiauh](https://github.com/th33xitus/kiauh) though as it's an installation script for software like Klipper and so on which makes everything a lot easier.

## Camera
As mentioned in the RPi section, if you connect a webcam directly to your printserver, I'd suggest to use a webcam which only offers a low resolution like 480p (640x480) as you don't need 4K for monitoring the printing process. Of course a more powerful hardware can also handle a higher resolution though.  
Preferably use a cam with a wide angle view and a fixed focus, so that you can see the whole area of the bed and there's no autofocus which gets irritated by the movement.  
If you want to create a time laps video from your printing process, keep in mind that it's a pretty resource consuming task (CPU power, RAM and storage usage). So also here using a low resolution like 480p is adviseable.    
  
However, I also would like to mention or even recommend general IP cameras (WiFi/LAN) which you could use. Also here it doesn't have to be a cam for a hundret bucks - a cheap one will do the job just fine. They often already come with the option to create time laps videos and store it onto a microSD card also.  
If you like to tinker a bit, maybe get yourself a cheap ESP32-CAM module.  
