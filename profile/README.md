# Welcome to Smart Trash Bin project

This is a project for the **Integrated Design Project** (`MCTE 3412`) (Mechatronics engineering)

## Group members

- Fareez
- Khairul
- Muadz
- Aiman

## Repositories

This organization host several repository for this project. All of the repository is **only visible** to group members only as they might contain sensitive information e.g. API keys.

### [flutter_idp_project](https://github.com/IDP-Smart-Trash-Bin/flutter_idp_project/)

Frontend mobile application for the trash bin. Monitor the current trash level etc. The application is build using [**Flutter**](https://flutter.dev/). Installable to [Android](https://github.com/IDP-Smart-Trash-Bin/flutter_idp_project/releases) and accessible on the [Web](https://idp-smart-bin.web.app/).

![screenshots](https://imgur.com/Ms5H3sG.png)

### [New-Arduino](https://github.com/IDP-Smart-Trash-Bin/New-Arduino)

Client-side Arduino program. Uses **Arduino Mega 2560**. Interfacing all the sensors and actuators eg ultrasonic sensors, linear actuator, servo motor etc. Also including the user interface ie LCD display and LED indicator.

![circuit diagram](https://imgur.com/R3vvOXt.png)

### [esp-new](https://github.com/IDP-Smart-Trash-Bin/esp-new)

Client-side ESP32 program. Using the WiFi capabilities of the chip, its purpose is to a) Update the trash value to the server, and b) Send notification through Telegram.

Programmed in C++ using [PlatformIO IDE](https://platformio.org/).

Also, we've learned that some ESP32 may having trouble communicate via https. I've include some SSL certificates bundles to the program.

### [server](https://github.com/IDP-Smart-Trash-Bin/server)

Server-side API server uses by the ESP32. To handle CRUD operation to the Firebase database and Telegram message formatting.

Deployed on [Heroku](https://idp-smart-trash-bin-server.herokuapp.com/).

<!-- ### [bot]() -->








