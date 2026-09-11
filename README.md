🔥 ESP32 Firebase LED Control
<p align="center">

A Beginner IoT Project using ESP32 and Firebase

Control ESP32 Built-in LED from anywhere using Firebase Realtime Database.

</p>
<img width="462" height="300" alt="image" src="https://github.com/user-attachments/assets/3a55fc7a-380d-4186-8a6a-d422e93c99c9" />


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


 1. Open Firebase Console

Go to [Firebase Console](https://console.firebase.google.com/?utm_source=chatgpt.com)

Then:

**Your Project → Build → Realtime Database**

### 2. Open Database

Click **Realtime Database**.

If you haven't created it yet:

**Create Database → choose location → Start in test mode** *(only for temporary testing)*.

### 3. Set your data

Inside the **Data** tab, you will see:

```text
Realtime Database
└── Data
```

Click the **⋮ (three dots)** menu → **Import JSON**.

Paste:

```json
{
  "LED": {
    "state": 0
  }
}
```

Then click **Import**.

### 4. Now you'll see

```text
LED
└── state    0
```

To turn your ESP32 LED **ON**, click the `state` value and change:

```text
0 → 1
```

To turn it **OFF**:

```text
1 → 0
```

Your ESP32 code reads exactly:

```text
/LED/state
```

### If you mean “Open read/write access”

Go to:

**Realtime Database → Rules**

For temporary testing, you can use:

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

⚠️ **Don't leave this open for a real/public project.** It allows anyone with access to your database URL to read/write your database. For your Firebase email/password setup, it's better to use authenticated rules.

If you send me a **screenshot of your Firebase Console**, I can point out exactly where to click.
