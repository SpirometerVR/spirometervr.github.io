---
title: "Week 4: Dev Environment Setup & Management Change"
date: 2020-02-21T11:00:00+01:00

tags: ['Development', 'Setup', 'New Production Manager']
author: "CHLA Team"
noSummary: true

resizeImages: false
---
This week we lost our Production Manager. That being said, we have elected a new PM and are still full steam ahead! 

For this posting, we are stepping a back a bit to review development environment setup for the breathing games. Without further ado...

# Arduino Setup

* Connect the M5StickC to your computer via the micro USB cable
* Install and run the Arduino IDE from https://www.arduino.cc/en/main/software
* In the Arduino IDE install the appropriate board manager and libraries ESP32 (Board Manager)
* Go to File -> Preferences -> Settings
* Copy this link for the ESP32 Board Manager URL to Additional Boards Manager URLs input field and click OK: https://dl.espressif.com/dl/package_esp32_index.json
* Go to Tools -> Board: -> Boards Manager…
* Search for ESP32 and install it 
M5StickC (Library)
* Go to Sketch -> Include Library -> Manage Libraries and search for M5StickC and install it
OSC by Adrian Freed, Yotam Mann et.al (Library)
* Now Search for OSC and install it.
* Go to Tools -> Board: and select M5Stick-C
* Go to Tools -> Upload Speed and select 115200
* Go to Tools -> Port and find and select the USB port your M5StickC is connected to, e.g. COM3.

## WiFi network

Just power on the wireless router via a micro USB cable and connect to SpironmeterNet

* **Network name:** SpirometerNet
* **Pass:** CHLA2020
* **Router** admin site:
* **Address:** 192.168.0.1
* **User:** admin
* **Pass:** admin
> Take note of your network IP address (e.g., 192.168.0.101)


{{< figure src="img/digital_spirometer.jpeg" >}}
## Digital Spirometer
* Download the digital spirometer files
* In the Arduino IDE open the M5_Spirometer_2020.ino file
* On ~line 44, const char * udpAddress = "192.168.0.111"; change this to your IP address
* Verify/Compile the code (click the round checkmark icon)
* Now Upload the compiled code to the M5StickC (click the round arrow icon)
* No errors? Then the digital spirometer is all set. Congrats!

## Digital Spirometer OSC tool
* Now run the Digital spirometer OSC tool.exe
* Update the IP address to your IP and the port to 8000
* If all is setup probably blowing into your attached mouth piece on the Digital Spirometer should produce a signal in the OSC tool.
* Jump for joy! Pump your fist in victory! The sensor is working correctly!

## Unity + Oculus
Just follow this great medium article:

[__>> How to get started with Oculus Quest and Unity on macOS__](https://medium.com/@sofaracing/how-to-develop-for-oculus-quest-on-macos-with-unity-5aa487b80d13).



-- The CHLA Team


