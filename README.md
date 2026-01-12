# 💡 VibeyRoomLight 
A catalog of my work with the WS2812B LED Strips. Here I'll put any electrical, programming, or music reactive work I have going with this LED Strips. 

## 🟢 **WLED Dorm Light ** (December 2024)**
Utilizing a SWPS @ 5V 15A, two WS2812B LED strips, and four power injections with proper fusing for safety. WLED utilized for animations. Very Bright!
### ▶️ **Click below to watch the demo!**
<p align="center">
  <a href="https://www.youtube.com/watch?v=jh-RSyLiC5o">
    <img src="https://img.youtube.com/vi/jh-RSyLiC5o/hqdefault.jpg" width="600" alt="Watch on YouTube">
  </a>
</p>
#####Backup link: https://www.youtube.com/watch?v=jh-RSyLiC5o

### ⚡ **Or see the wiring Diagram Below...**
Todo: Make wiring diagram and place here. 

## 🟡 **Arduino / Raspi Dorm Light**
Utilizes a Rasberry Pi 4b for custom made animations on a WS2812B LED strip. Communicates via Serial to an Arduino Uno controller board, with an LCD interface and buttons for animation selection.
### ▶️ **Click below to watch the demo!**
To do: Put image here that links to youtube

##### Backup Link: https://drive.google.com/file/d/1nCgGHZAg6cg-lvnDBANqvG6rShFJDbFf/view?usp=sharing

### **⌨️ More about the code:**
#### Raspberry pi:
The strip class consists of all the effects I have programmed using the neopixel library. Many of the workings of these effects take artistic or programming inspiration from the FASTLed library. 
The SerialCom class is the raspberry pi end of the communication with the Arudino, while the controller class connects all these different classes together. (This is inspired by the Model View Controller method)
The folder labeled "Old Stuff" contains prototype code for an HTTPs server user interface that we orginally planned to use and other code to help us learn and experiment. We decided to not use a web server interface due to dorm wifi security issues. 

#### Arduino:
All the classes for the arduino are in the LEDRoom.ino file. 
The ArudinoUserDis class handles any actions that displays informations or actions to the user via the lcd display. Ex: Color selection Screen, Brightness Screen, Error Screens
The UserData class is in charge of handling gather user inputs and sending via serial communication to raspberry pi
