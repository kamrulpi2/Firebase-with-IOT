
### 1. Open Firebase Console

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
