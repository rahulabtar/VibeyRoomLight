# 💡 VibeyRoomLight 
A catalog of my work with the WS2812B LED Strips. Here I'll put any electrical, programming, or music reactive work I have going with this LED Strips. 

# 🟢 **WLED Dorm Light** (December 2024)
Utilizing a SWPS @ 5V 15A, two WS2812B LED strips, and four power injections with proper fusing for safety. WLED utilized for animations. Very Bright!
## ▶️ **Click the image below to watch the demo!**
<p align="center">
  <a href="https://www.youtube.com/watch?v=jh-RSyLiC5o">
    <img src="https://img.youtube.com/vi/jh-RSyLiC5o/hqdefault.jpg" width="600" alt="Watch on YouTube">
  </a>
</p>

##### Backup link: https://www.youtube.com/watch?v=jh-RSyLiC5o

## ⚡ **Or see the setup Below...**

<p align="center">
  <img src="wiring.png" width="600" alt="Wiring diagram">
</p>

This setup includes a BTF-100-5 SWPS, rated for mains voltage as an input and 5V 20A on output. I did not use these full capabilities. stopping around 16A. 
Automotive Fuses were utilized as a safety precaution to prevent a fire!
Power injections at the ends of the strip are 2A while middle of the strip is 4A. This is due to the power needs in the middle are greater. 
It's important to note this may not be the best wiring diagram circuit wise, due to the routing restricions I had to undertake while haning this up on the wall. 
In other words, theoretically not effective, but in real life it's practical. 


# 🟡 **Arduino / Raspberry Pi Dorm Light** (September 2023)
Utilizes a Rasberry Pi 4b for custom made animations on a WS2812B LED strip. Communicates via Serial to an Arduino Uno controller board, with an LCD interface and buttons for animation selection. Powered via Pi's 5v rail.
## ▶️ **Click the image below to watch the demo!**
<p align="center">
  <a href="https://youtube.com/shorts/rE3yTOF5lLg">
    <img src="https://img.youtube.com/vi/rE3yTOF5lLg/hqdefault.jpg" width="400" alt="Watch the demo">
  </a>
</p>

##### Backup Link: https://drive.google.com/file/d/1nCgGHZAg6cg-lvnDBANqvG6rShFJDbFf/view?usp=sharing

## **⌨️ More about the code:**
All code for this task can be found in LED_room
### Raspberry Pi:
The strip class consists of all the effects I have programmed using the neopixel library. Many of the workings of these effects take artistic or programming inspiration from the FASTLed library. 
The SerialCom class is the raspberry pi end of the communication with the Arudino, while the controller class connects all these different classes together. (This is inspired by the Model View Controller method)

### Arduino:
All the classes for the arduino are in the LEDRoom.ino file. 
The ArudinoUserDis class handles any actions that displays informations or actions to the user via the lcd display. Ex: Color selection Screen, Brightness Screen, Error Screens
The UserData class is in charge of handling gather user inputs and sending via serial communication to raspberry pi
