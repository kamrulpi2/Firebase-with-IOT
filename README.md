🔥 ESP32 Firebase LED Control
<p align="center">

A Beginner IoT Project using ESP32 and Firebase

Control ESP32 Built-in LED from anywhere using Firebase Realtime Database.

</p>

| Item           | Details           |
| -------------- | ----------------- |
| Board          | ESP32             |
| Cloud Platform | Firebase          |
| Communication  | WiFi              |
| Database       | Realtime Database |
| Programming    | Arduino C++       |


      User

       |
       ↓

 Firebase Database

       |
       ↓

     WiFi

       |
       ↓

     ESP32

       |
       ↓

 Built-in LED

┌────────────────────┐
│ ESP32 Board        │
├────────────────────┤
│ USB Cable          │
├────────────────────┤
│ WiFi Connection    │
└────────────────────┘
 LED
│
└── state

    0 → OFF
    1 → ON
