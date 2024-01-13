# Tilt Repeater ESP32
Tilt hydrometer repeater for ESP32 based devices
- Updated to Support Latest Ardunio IDE

## Hardware
- Teyleten Robot ESP32S ESP32 ESP-WROOM-32 Development Board 2.4GHz Dual-Core WiFi +Bluetooth 2 Function Microcontroller for Arduino (ESP32 30P, 3PCS) https://amzn.to/3vwreXF
- SMALLElectric Micro USB Cable (5-Pack, 6FT) Android Charger, Long Android Phone Charger Cord for Samsung Galaxy S7 S6 Edge J7 S5,Note 5 4,LG 4 K40 K20,MP3,Kindle,Tablet,White https://amzn.to/47AFs6S

### Install Guide
1. Download Ardunio IDE - https://www.arduino.cc/en/software
2. Download the ESP32-Tilt-Repeater.ino - click on the file in github and download the raw file.
3. Open the file in Ardunio
4. Next you want to edit line 8 to change your color. int repeatColour =  0; // Choose Tilt colour to repeat. 0=All, 1=Red, 2=Green, 3=Black, 4=Purple, 5=Orange, 6=Blue, 7=Yellow, 8=Pink.
5. Connect your ESP32 Board to your PC using your micro usb cable
6. Choose Select Board and Select other board and port
7. Type DOIT ESP32 DEVKIT V1 and click ok
8. Make sure you board is connected to the correct serial port
9. Press and Hold the Boot button on the back side of your board. This enables the upload
10. Press upload and you will see compiling sketch, continue holding boot button
11. A black window should open and you will see it compiling.
12. Once Compiled you will see Hard resetting via RTS pin.
13. Release the Boot button
14. Unplug it and plug it back in.
15. In Ardunio goto tools Serial Monitor
16. A window will open and you will see output and Serial Monitor
17. Click on Serial Monitor
18. You should see your ESP32 with Scanning...40 Devices Found. No Tilts Repeated.
19. Turn on your tilt and you will see it repeating.

### Tilt Repeater Case
- walgreens pill case
<img width="728" alt="Case" src="https://github.com/Route105/Tilt-Repeater-ESP32/assets/96628531/38e280b4-9aa3-4b2e-b4e7-b8b6f13611d5">

### TiltBridge on a ESP32
https://tiltbridge.readthedocs.io/en/master/installation.html

### Tilt 3 Point Calibration 
- 3 point device level Calibration for your tilt https://www.youtube.com/watch?v=sechzUDQKVs
- When you do the Calibration, Start with the 1.12 Solution and then 1.061 Solution then the water.  
