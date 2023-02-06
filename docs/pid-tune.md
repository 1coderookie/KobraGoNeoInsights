<link rel=”manifest” href=”docs/manifest.webmanifest”>

# PID Tuning
Without going into too much details here, PID stands for Proportion, Integral and Derivate. These are three variables of an algorith which is supposed to keep the temperature stable.  
By executing a PID tuning, the printer heats up the desired heating element (extruder or bed) to a given temperature for a given amount of circles and measures the fluctuation. After the process is done, you'll then get an output of three values P, I and D and write them to the memory.  

It's advisable to execute a PID tuning for both the extruder and the bed before you want to use your printer for the first time.  
Also after you changed the hotend, the cartridge heater or a thermistor or installed a new bed, you should execute a PID tuning.  
  
The best way to execute a PID tuning is by simply using certain G-code commands and send them to your printer. To do so, I'll show you an example of how to do it using OctoPrint - but you can do it with any other program that allows you to send G-code commands directly also.  
  
PID tuning needs to be done in two steps: one for the extruder and one for the bed.

## Extruder PID tuning
Because I use to print at 220°C, I want to use this temperature for the PID tuning of the extruder.  
I want the printer to execute seven cycles - the more the better the result will be.  

The belonging G-code is  
`M303 E0 S220 C7`  
where `M303` is the PID tune, `E0` is the extruder, `S220` is the temperature of 220°C and `C7` means seven cycles.  
      
After sending this command, the printer will reply and start the process:  
```
Send: M303 E0 S220 C7  
Recv: PID Autotune start
```
    
The printer will then display the process and values for each cycle. You don't need that later, but just that you saw that once I'll show you the output of one of those cycles:  
```
Recv:  T:217.71 /0.00 (255.00) B:54.25 /0.00 (3537.13) @:97 B@:0
Recv:  T:216.69 /0.00 (259.88) B:54.14 /0.00 (3539.13) @:97 B@:0
Recv:  T:216.61 /0.00 (260.25) B:54.03 /0.00 (3541.13) @:97 B@:0
Recv:  T:217.55 /0.00 (255.75) B:53.88 /0.00 (3543.63) @:97 B@:0
Recv:  T:219.06 /0.00 (248.50) B:53.79 /0.00 (3546.00) @:97 B@:0
Recv:  T:221.19 /0.00 (239.25) B:53.66 /0.00 (3547.50) @:0 B@:0
Recv:  T:222.91 /0.00 (232.38) B:53.55 /0.00 (3549.50) @:0 B@:0
Recv:  T:223.94 /0.00 (228.25) B:53.45 /0.00 (3551.25) @:0 B@:0
Recv:  T:223.47 /0.00 (230.13) B:53.36 /0.00 (3552.88) @:0 B@:0
Recv:  T:222.53 /0.00 (233.88) B:53.21 /0.00 (3555.50) @:0 B@:0
Recv:  T:220.75 /0.00 (241.00) B:53.13 /0.00 (3556.88) @:0 B@:0
Recv:  bias: 94 d: 94 min: 216.38 max: 224.03 T:218.93 /0.00 (249.13) B:52.98 /0.00 (3559.75) @:94 B@:0
```
As you can see looking at the first value "T:" which is the temperature of the extruder, it fluctuates around the desired 220°C, so the printer heats it up and let it cool down around the 220°C.  
  
You can see the process by looking at the temperature graph as shown below.  
![PID tuning extruder](assets/images/pid-tune-extruder.png)

After finishing the seven cycles, you'll receive a summarized output like the one below:  
``` 
Recv: PID Autotune finished! Put the last Kp, Ki and Kd constants from below into Configuration.h
Recv: #define DEFAULT_Kp 20.84
Recv: #define DEFAULT_Ki 1.86
Recv: #define DEFAULT_Kd 58.26
Recv: ok
```
You can see the values for P = Kp, I = Ki and D = Kd - these have to be sent to the printer.  
To do so, we take the values from above and send the following `M301` command, the printer will answer with a "received" message:  
```
Send: M301 P20.84 I1.86 D58.26
Recv: echo: p:20.84 i:1.86 d:58.26
Recv: ok
```
Now we need to save everything by sending the `M500` command:
```
Send: M500 
Recv: echo:Settings Stored (735 bytes; crc 9159)
Recv: ok
```
That's it!  
Congratulations, you just did the PID tuning for your extruder!
    
## Bed PID tuning
Now you want to do the same for your heated bed, but you have to use a different command.  
Because I use to print at a bed temperature of 60°C, I want to execute the PID tuning at that temperature also. Again it should be done seven times.  

The belonging code is  
`M303 E-1 S60 C7`
where `M303` is the PID tune, `E-1` is the bed, `S60` is the temperature of 60°C and `C7` means seven cycles.  
     
Because you already know the steps now, I'll just write down the commands and answers from the printer:  
```
Send: M303 E-1 S60 C7
Recv: PID Autotune start
(...)
Recv: PID Autotune finished! Put the last Kp, Ki and Kd constants from below into Configuration.h
Recv: #define DEFAULT_bedKp 124.24
Recv: #define DEFAULT_bedKi 21.69
Recv: #define DEFAULT_bedKd 474.49
Recv: ok
(...)
Send: M304 P124.24 I21.69 D474.49
Recv: echo: p:124.24 i:21.69 d:474.49
Recv: ok
(...)
Send: M500
Recv: echo:Settings Stored (735 bytes; crc 54612)
Recv: ok
```
That's it!  
Congratulations, you just did the PID tuning for your bed!
