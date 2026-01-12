# VibeyRoomLight
A catalog of my work with the WS2812B LED Strips

## ▶️ **Click below to watch the demo!**

<p align="center">
  <a href="https://www.youtube.com/watch?v=jh-RSyLiC5o">
    <img src="https://img.youtube.com/watch?v=jh-RSyLiC5o/hqdefault.jpg" width="600" alt="Watch on YouTube">
  </a>
</p>

https://www.youtube.com/watch?v=jh-RSyLiC5o


QUICK VIDEO SHOWCASE:
https://drive.google.com/file/d/1nCgGHZAg6cg-lvnDBANqvG6rShFJDbFf/view?usp=sharing


The project consists of an arduino uno connected to several potentiometers allowing the user to input desired patterns and colors. This data is then communicated to a raspberry pi 4b via USB serial bus, which then displays the desired inputs on a WS2812B strip.


Raspberry pi:
The strip class consists of all the effects I have programmed using the neopixel library. Many of the workings of these effects take artistic or programming inspiration from the FASTLed library. 

The SerialCom class is the raspberry pi end of the communication with the Arudino, while the controller class connects all these different classes together. (This is inspired by the Model View Controller method)

The folder labeled "Old Stuff" contains prototype code for an HTTPs server user interface that we orginally planned to use and other code to help us learn and experiment. We decided to not use a web server interface due to dorm wifi security issues. 


Arduino:
All the classes for the arduino are in the LEDRoom.ino file. 

The ArudinoUserDis class handles any actions that displays informations or actions to the user via the lcd display. Ex: Color selection Screen, Brightness Screen, Error Screens

The UserData class is in charge of handling gather user inputs and sending via serial communication to raspberry pi
