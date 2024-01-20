# Tilt Repeater ESP32
Tilt hydrometer repeater for ESP32 based devices
- Forked from Repo By David Gray - https://github.com/N3MIS15/ESP32-Tilt-Repeater
- Code was updated to support the Latest verison of Arudion IDE

<img width="225" alt="Case" src="https://github.com/Route105/Tilt-Repeater-ESP32/assets/96628531/38e280b4-9aa3-4b2e-b4e7-b8b6f13611d5">

## Tilt Repeater Hardware
- 1 Pack HiLetgo ESP-WROOM-32 ESP32 ESP-32D Development Board 2.4GHz for Arduino - https://amzn.to/3O3r4x3
- 3 Pack Teyleten Robot ESP32S ESP32 ESP-WROOM-32 Development Board for Arduino - https://amzn.to/3vwreXF
- Micro USB Cable (5-Pack, 6FT) https://amzn.to/47AFs6S
- Tilt Wireless Hydrometer - https://amzn.to/3SitcDE
- Streamlight 85175 CR123A Lithium Batteries, 2-Pack - https://amzn.to/41Um6Zn
- Tilt Standard Wrench + Bottle Opener - https://amzn.to/3vE9zNK
- Pharmacy Medicine Container Pill Bottle - https://amzn.to/3Siu8rE

### Tilt Repeater Install Guide
1. Download Ardunio IDE - https://www.arduino.cc/en/software
2. Download the ESP32-Tilt-Repeater.ino - click on the file in github and download the raw file.
3. Open the file in Ardunio
4. Next you want to edit line 8 to change your color. int repeatColour =  0; // Choose Tilt colour to repeat. 0=All, 1=Red, 2=Green, 3=Black, 4=Purple, 5=Orange, 6=Blue, 7=Yellow, 8=Pink.
5. Connect your ESP32 Board to your PC using your micro usb cable
6. Choose Select Board and Select other board and port
7. Arduino IDE Board Types:
   - HiLetgo ESP-WROOM-32 ESP32 ESP-32D use Board - DOIT ESP32 DEVKIT V1
   - Teyleten Robot ESP32S use Board - ESP32-WROOM-DA 
11. In Arduino IDE Click Tools
12. Set Core Debug Level: "None"
13. Set Erase All Flash Before Sketch Upload:"Disabled"
14. Set Flash Frequency: "80Mhz"
15. Set Upload Speed: "921600"
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

### TiltBridge on a ESP32
https://tiltbridge.readthedocs.io/en/master/installation.html

### Tilt 3 Point Calibration 
- 3 point device level Calibration for your tilt https://www.youtube.com/watch?v=sechzUDQKVs
- When you do the Calibration, Start with the 1.12 Solution and then 1.061 Solution then the water.  
