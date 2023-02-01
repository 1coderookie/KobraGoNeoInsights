<link rel=”manifest” href=”docs/manifest.webmanifest”>

# Control Panel  
Both printers come with the same control panel. It's a 2.4" LCD screen with a control knob.  
There is no additional microSD card slot located at this panel.  

![Image about to come soon]()

The control panel allows you to control the printer manually, so you don't necessarily need an additional computer connected to the printer running e.g. Octoprint (even though it's advisable to do so).  
You can e.g. initiate the bed leveling process, heat up the extruder, load and unload filament, adjust your z-offset or home one or all axes.  
The usage is pretty easy and self-explaining - you turn the knob to the desired icon of the menu or function and press it to enter the menu or initiate the function.  
See your manual for further informations of the possible actions you can take.  
It also displays status informations like the current temperatures and the temperatures that should be reached due to a certain function or during the printing process. 
However, it does *not* display a meshview after you proceeded the bed level function - if you'd like to see that, you'd have to use additional software like the beforementioned Octoprint.  
  
## Error Messages
The display also displays error messages if any severe errors occur.  
As an example, it showed "thermal runaway" as my friend was struggeling with the printer and as the silicone sock started to fall of, because it seems that the heater block got cooled and therefore the measured temperature dropped below an expected value (that's just a guess though, I'm still not 100% sure about it).  
  
When I was trying to get the printer up and running, at one point the display showed the following error message:  
![Error E1](../assets/images/controlunit_err_e1-max-temp_web.jpg)   

I wasn't able to bypass that message in any way - it just stayed onto the screen and never disappeared.  
I couldn't find a "reset button" on the mainboard and had no clue what was going on.   
After searching the web for solutions and trying different suggestions like unplugging the thermistor of the extruder and switching it off and on again to reset the message, I started to inspect the mainboard with a magnifying glass. This is what I spotted:  
![Melted D4 caused by a shortcut](../assets/images/mainboard_melted-D4_web.jpg)  
  
I still have no clue *how* this actually happened, but it must have been caused by a shortcut either of the cartridge heater and/or the thermistor of the extruder. However, this little melted fella named "D4" caused the error message - after I installed a new thermistor and cartridge heater and swapped out the broken mainboard to replace it with a new one, everything was fine again.  
So if you ever face an error message which just stays on the screen whatever steps you took - maybe grab a magnifying glass and take a closer look, it might be worth it..  
  
If I'll come across further error messages and know the solution for that, I'll post it here.
