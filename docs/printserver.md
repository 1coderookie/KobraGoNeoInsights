<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Printserver
Sooner or later you'll come to the point that you want to use additional software like [Octoprint](https://octoprint.org/) or so to control your printer.  
Yes, it's not necessary as you can control it directly using the printers control unit and it's advisable to stay in the same room and monitor the printing process to be able to intervene as soon as something is going wrong - but we all know how it is..  
So having the possibility to not only send gcode commands directly to the printer but also to use certain plugins or additional hardware to e.g. monitor the printing process isn't the worst idea.  
  
## Raspberry Pi
When you start looking around for a system the desired software should run on, the first thing you'll come across surely will be the Raspberry Pi (in the following named as "RPi").  
The RPi is a little computer which became pretty famous since it entered the market.  
It's a Broadcom SoC 64bit ARM system with LAN (and WiFi within the newer versions) and a microSD card reader onboard which keeps the desired OS. It offers GPIOs to directly connect hardware like sensors to it and it draws only a little amount of power.  
Pretty much all of the regular software for 3D printing like the beforementioned [Octoprint](https://octoprint.org/) or [Mainsail](https://docs.mainsail.xyz/) or so are available as specific RPi image which makes it pretty easy and flawless to install even if you're not an expert. Just install the [Raspberry Pi Imager](https://www.raspberrypi.com/software/) and the installation will take a few minutes only.  
And as handy as it is - it might not be the best solution, especially these days.  
  
Prices for the RPi went up to a ridiculous level (afaik at least in Europe and the US) - *if* they're even available at all.  
Also you don't want to get yourself an old RPi2B for example, it should be a RPi3B+ at least, a RPi4 would be even better. Not only because of the pure processor power or the RAM - both is sufficient even with the RPi3 for example, but mostly because of the reason how the USB sockets are connected to the CPU. Afaik, up until the RPi3 the Broadcom BCM2837 only offers one(!) USB port itself. This one port is split up by using a SMSC LAN9514 hub chip to get four USB connectors out of it *and* it also uses the LAN port.  
  
If you're asking yourself now "What the heck is this guy talking about - I have four USB connectors available there, so what's the problem?" - well, let me try to explain it to you very simple:  
Imagine you connect your RPi3 to a monitor and plug in a mouse, keyboard, your 3D printer and a webcam to the USB sockets and maybe you also use the LAN connection (because everybody who knows wireless uses wires ;) ). Then you start your printing process sending the gcode file to the printer and start to observe the printing process using the camera. Then all of the informations are running across the same one and only USB port of the SoC (the main CPU). That means that most likely you'll find yourself noticing some kind of stumbling during the printing process and/or the stream of the webcam.  
That doesn't occur because of a lack of RAM or CPU power (what people use to assume) - that occurs because of the architecture and the bottleneck "one USB port at the SoC".  
  
??? tip "RPi and a (Web-)Cam"
However, if you're already running a RPi(3) and face those kind of problems as mentioned above due to a connected webcam to the RPi, I'd suggest the following:  

- Switch to a cheap/old type of webcam which only offers a low resolution like 640x480. You don't need 4K to see what's going on and by using a low resolution you can at least decrease the amount of informations that has to run through the mentioned bottleneck.  
- Get rid of the USB cam and set up a WiFi/LAN cam instead which isn't connected to the RPi. Up to me this is even a better solution then downgrading the webcam as the RPi doesn't have to deal with the data from the WiFi/LAN cam at all. If you like to tinker and don't mind the probable effort, get yourself one of those cheap ESP32-CAM modules and set it up. Or just go for a cheap WiFi/LAN camera.   

## Other SoC Boards
If you can't or don't want to get an RPi but still want to stick to one of those tiny tinker units, you can check out the market what's available and compareable to a RPi, like an "Orange Pi", a "Le Potato" or so on.  
I'm not going into further details here as I personally don't use them and prefer Thin Clients.  

## Old Hardware Like Laptops
If you have old hardware like a laptop laying around, you can also use that. Don't worry - even if it's pretty old in most of the cases it still would be sufficient. Install a Linux OS onto it and then install the desired software.  
You'll find some tips about how to get the software installed further below.  
  
However, as much as I appreciate and love to re-/up-cycle old hardware, one thing has to be mentioned: the amount of power they're drawing.  
It might not really come into account if your prints last only a few hours and after finishing them you turn everything off. But as soon as you think about running those machines pretty much 24/7 you should keep in mind that they draw a lot of power which sums up at the end. Right now here in Germany we're paying about 0,40€/kWh, so it really matters just looking at the financial side of that - not to mention the ecological aspect.    

## Thin Clients
Now - get ready for a real deal: Thin Clients!  
Ok, might be a bit exxagerated, but I really *love* those fellas.  
If you've never heard of them, let me give you a quick introduction. Thin Clients are computers which are often used by companies for e.g. setting up workstations for their employees or to have some kind of information desk or screen running somewhere. They have a small build factor, don't draw an excessive amount of power and usually come with connectors for LAN, USB, a monitor and so on. Especially newer models (like only a few years old) have hardware built in which would be even powerful enough to replace your daily driver for surfing the web or writing stuff. The newer they are, the more the yhave to offer usually. That means you can put in up to 32GB or even 64GB of RAM, swap in a SSD (2.5", m2 SATA or NVMe - that often depends on the age actually) and go crazy and even use VirtualMachines (ProxmoxVE) or containers (Docker). Of course you could also just install a LinuxOS like Ubuntu or Ubuntu Server. 
