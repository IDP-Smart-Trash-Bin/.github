# Welcome to Smart Trash Bin project

This is a project for the **Integrated Design Project** (`MCTE 3412`) (Mechatronics engineering)

## Group members

|                                 Name                                 |                                 Us                                  |
| :------------------------------------------------------------------: | :-----------------------------------------------------------------: |
| <ul><li>Fareez</li><li>Khairul</li><li>Muadz</li><li>Aiman</li></ul> | <img src="https://i.imgur.com/C61yJAX.png" alt="us :)" width="60%"> |

## Project description

This project is to design and build a smart trash bin that can be used in mahallah, kuliyyah or other places of attraction in IIUM. Some feature highlights of this product is:
a) Auto opening lid when person is present
b) Auto compress the trash to save space
c) Notify the cleaner when the trash bin is full
d) Monitor the trash level remotely (IoT)

<img src="https://i.imgur.com/uHTBzdO.png" alt="smart trash bin" width="80%">


## Repositories

This organization host several repository for this project. All of the repository is **only visible** to group members only as they might contain sensitive information e.g. API keys. However, you can ask for the source code if you are interested.

### [flutter_idp_project](https://github.com/IDP-Smart-Trash-Bin/flutter_idp_project/)

Frontend mobile application for the trash bin. Monitor the current trash level etc. The application is build using [**Flutter**](https://flutter.dev/). Installable to Android and accessible on the Web.

APK file(s): https://github.com/IDP-Smart-Trash-Bin/flutter_idp_project/releases

Web URL: https://idp-smart-bin.web.app/ (Hosted on Firebase Hosting)

![screenshots](https://imgur.com/Ms5H3sG.png)

### [New-Arduino](https://github.com/IDP-Smart-Trash-Bin/New-Arduino)

Client-side Arduino program. Uses **Arduino Mega 2560**. Interfacing all the sensors and actuators eg ultrasonic sensors, linear actuator, servo motor etc. Also including the user interface ie LCD display and LED indicator.

![circuit diagram](https://imgur.com/R3vvOXt.png)

<img src="https://i.imgur.com/sHNFEM7.png" alt="circuit head" width="70%">

_Sorry for the messy circuit :sweat_smile:_

### [esp-new](https://github.com/IDP-Smart-Trash-Bin/esp-new)

Client-side ESP32 program. Using the **WiFi capabilities** of the chip, its purpose is to a) Update the trash value to the server, and b) Send notification through Telegram.

Programmed in C++ using [PlatformIO IDE](https://platformio.org/).

Also, we've learned that some ESP32 may having trouble communicate via https. I've include some SSL certificates bundles to the program.

### [server](https://github.com/IDP-Smart-Trash-Bin/server)

Server-side API server uses by the ESP32. To handle CRUD operation to the Firebase database and Telegram message formatting.

Written in Node.js using [Express](https://expressjs.com/) framework.

Deployed on [Heroku](https://www.heroku.com/).

Server URL: https://idp-smart-trash-bin-server.herokuapp.com/

### [bot](https://github.com/IDP-Smart-Trash-Bin/bot)

Telegram bot that is used to send notification to the user (subscribers). It is also used to respond commands from the users.

Written in Python using [python-telegram-bot](https://github.com/python-telegram-bot/python-telegram-bot) version 13.x

<div style="display: flex;">
  <div style="flex: 1; margin-right: 20px;">
    <img src="https://i.imgur.com/pjFKcF9.png" alt="image1" style="max-width: 100%;">
  </div>
  <div style="flex: 1; margin-left: 20px;">
    <img src="https://i.imgur.com/wmBlofn.gif" alt="image2" style="max-width: 100%;">
  </div>
</div>

Also deployed on [Heroku](https://www.heroku.com/).

Bot URL: https://t.me/idptrashbin_bot

## Design

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 20px;">
  <div>
    <img src="https://i.imgur.com/YjpC9Dy.png" alt="image1" style="max-width: 100%;">
  </div>
  <div>
    <img src="https://i.imgur.com/JvZs3H8.png" alt="image2" style="max-width: 100%;">
  </div>
  <div>
    <img src="https://i.imgur.com/Um7JKqQ.png" alt="image3" style="max-width: 100%;">
  </div>
  <div>
    <img src="https://i.imgur.com/s5oigjq.png" alt="image4" style="max-width: 100%;">
  </div>
</div>

## Conclusion

This project about 90%-ish complete. All planned features are working as expected, eg the level sensor, LCD display, IoT integration etc.

Some features that are not fully achieved are:

- Auto opening lid - Some problems related to the servo. The system would reset itself if servo is triggered. We suspected it was the spontaneous current draw by the servo. So we've isolated the Servo power supply. However, the problem still persist.
- Trash compressing mechanism - We've bought a linear actuator that [cannot fit](https://imgur.com/QXBxPLk.png) properly inside the body.
