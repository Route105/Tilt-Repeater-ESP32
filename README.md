# ESP32 Tilt Bluetooth Repeater :beers:
Tilt hydrometer bluetooth repeater for ESP32 based devices
- Forked from Repo By David Gray - https://github.com/N3MIS15/ESP32-Tilt-Repeater
- Supports the Latest verison of Arudion IDE
- Tilt Repeater dropping bluetooth connetion is now fixed

<img width="225" alt="Case" src="https://github.com/Route105/Tilt-Repeater-ESP32/assets/96628531/38e280b4-9aa3-4b2e-b4e7-b8b6f13611d5">

-----
### Tilt Repeater Hardware
- 1 Pack HiLetgo ESP-WROOM-32 ESP32 ESP-32D Development Board 2.4GHz for Arduino: https://amzn.to/3O3r4x3
- 3 Pack Teyleten Robot ESP32S ESP32 ESP-WROOM-32 Development Board for Arduino: https://amzn.to/3vwreXF
- Micro USB Cable (5-Pack, 6FT): https://amzn.to/47AFs6S
- Tilt Wireless Hydrometer: https://amzn.to/3SitcDE
- Raspberry Pi 4 8GB Starter Kit: https://amzn.to/4903CcI
- Streamlight 85175 CR123A Lithium Batteries, 2-Pack: https://amzn.to/41Um6Zn
- Tilt Standard Wrench + Bottle Opener: https://amzn.to/3vE9zNK
- Pharmacy Medicine Container Pill Bottle: https://amzn.to/3Siu8rE

-----
### Tilt Repeater Install Guide
1. Download Ardunio IDE - https://www.arduino.cc/en/software
2. Download the ESP32-Tilt-Repeater.ino - click on the file in github and download the raw file.
3. Open the file in Ardunio
> [!IMPORTANT]
> 4. Next you want to edit line 8 to change your color. int repeatColour =  0;
>    - Choose Tilt color to repeat. 0=All, 1=Red, 2=Green, 3=Black, 4=Purple, 5=Orange, 6=Blue, 7=Yellow, 8=Pink.
5. Connect your ESP32 Board to your computer using your micro usb cable
6. Choose Select Board and Select other board and port
7. Arduino IDE Board Types try either:
   - ESP32-WROOM-DA 
   - ESP32 DEVKIT V1 
11. In Arduino IDE Click Tools
12. Set Core Debug Level: "None"
13. Set Erase All Flash Before Sketch Upload:"Disabled"
14. Set Flash Frequency: 80Mhz
15. Set your Upload Speed to: 115200
17. Press and Hold the Boot button on the back side of your board. This enables the upload
18. Press upload and you will see compiling sketch, continue holding boot button
19. A black window should open and you will see it compiling.
20. Once Compiled you will see Hard resetting via RTS pin.
21. Release the Boot button
22. Unplug it and plug it back in.
23. In Ardunio goto tools Serial Monitor
24. A window will open and you will see output and Serial Monitor
25. Click on Serial Monitor
26. You should see your ESP32 with Scanning...40 Devices Found. No Tilts Repeated.
27. Turn on your tilt and you will see it repeating.

> [!TIP]
> Use clip to press and hold the boot button while uploading your sketch. 

<img width="225" alt="Case" src="https://github.com/Route105/Tilt-Repeater-ESP32/assets/96628531/b1b991fb-9908-4514-91d6-6e1cf54f8588">


-----
### Tilt Repeater ESP32 dropping bluetooth connections
The esp32 scans for bluetooth devices for a period of time determined by the "SCAN_TIME" variable. By default this is 5 seconds. Increasing the "SCAN_TIME" variable will give the esp32 a better chance of finding bluetooth devices with a weak signal.

The esp32 then goes through all the bluetooth devices is found and filters out any that are not Tilt hydrometers. If any Tilts are found, the esp32 checks if they are the desired colour to repeat (determined by the "repeatColour" variable, 0 being all colours). It then takes that information the Tilt sent and repeats it. After repeating the esp32 goes to sleep for an amount of time, which is determined by the "TIME_TO_SLEEP" variable. The esp resets at this point and starts this sequence of events all over again.

If no Tilts are found by the scan, the "TIME_TO_SLEEP" variable gets divided by the "fastSleep" variable (with the default settings the result would be 15). This forces the esp32 to scan more often when no tilts are found by the scan.

> [!TIP]
>  Increase the scan time to 20 and decrease the time to Sleep to 10

-----
### Tilt Pi
Tilt Pi is like a local server "Rasberry PI" that uses Bluetooth to log Tilt readings on a regular cadence. For example, I have set mine up to run every 15 minutes and log data to Brewfather. My Fermenters are on one side of my brewery while the rasberry pie is on the other connected to a tv. The ESp32 Tilt Repeater allows me to put the Tilt Pi at least 10 - 12ft from my fermenters. Follow the steps listed on the Tilt website to get started. 
https://tilthydrometer.com/blogs/news/introducing-tilt-pi-an-sd-card-image-download-for-your-raspberry-pi-3-or-zero-w
<img width="500" alt="Case" src="https://github.com/Route105/Tilt-Repeater-ESP32/assets/96628531/e0f47135-858c-4500-b0e6-0309b69503f1">


<img width="500" alt="Case" src="https://github.com/Route105/Tilt-Repeater-ESP32/assets/96628531/58ff2b88-3f0e-4859-9a33-62917d62bff5">


-----
### Tilt 3 Point Device Level Calibration 
Doing a Tilt Device Level Calibration stores the calibration data in the tilt. You don't need to add the calibration values to the APP or Software you use. 
- 3 point device level Calibration for your tilt: https://www.youtube.com/watch?v=sechzUDQKVs
> [!TIP]
> When you do the calibration, Start with the 1.12 Solution then 1.061 Solution then the water.  
