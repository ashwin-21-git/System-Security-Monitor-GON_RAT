# GON_RAT - Android Security & Remote Management Tool

GON_RAT is an Android application designed for security testing and remote device management. It functions as a standard flashlight app while providing extensive remote control capabilities via a Telegram bot and a reverse shell.

**⚠️ DISCLAIMER:** This tool is for educational and authorized security testing purposes ONLY. Unauthorized use on devices you do not own or have explicit permission to test is illegal.

## Features

### 🔦 Frontend
*   Functional Flashlight (Torch) toggle.
*   Request for necessary Android permissions.

### 🤖 Telegram Bot Control
Manage the device remotely using simple commands:
*   **Data Extraction:** `/dump_calls`, `/dump_contacts`, `/dump_sms`.
*   **Surveillance:** `/camera_back`, `/camera_front`, `/record <sec>`, `/screenshot`, `/screenshot_multiple <count> <interval>`, `/location`.
*   **System Info:** `/ping`, `/status`, `/battery`, `/help`.
*   **File Management:** `/logs` (Keylogger), `/download <path>`.
*   **Remote Execution:** `/shell <cmd>`.

### 🛡️ Persistence & Stealth
*   **Foreground Service:** Runs as a "System Background Process" to avoid being killed by the OS.
*   **Accessibility Service:** Includes a built-in Keylogger to capture keystrokes.
*   **Device Admin:** Requests admin privileges to prevent easy uninstallation.
*   **Boot Persistence:** Automatically starts on device boot.
*   **Reverse Shell:** Maintains a persistent connection to a remote listener for full terminal access.
*   **Gallery Observer:** Automatically monitors and sends new photos taken on the device.

## Setup Instructions

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/YOUR_USERNAME/GON_RAT.git
    ```

2.  **Configure Credentials:**
    Open `app/src/main/java/com/pentest/torch/PersistenceService.kt` and replace the following placeholders:
    *   `YOUR_BOT_TOKEN_HERE`: Your Telegram Bot API Token (from @BotFather).
    *   `YOUR_CHAT_ID_HERE`: Your Telegram Chat ID.
    *   `YOUR_IP_HERE`: Your server IP for the reverse shell.

3.  **Build the APK:**
    Import the project into Android Studio and build the project, or use Gradle:
    ```bash
    ./gradlew assembleDebug
    ```

4.  **Deployment:**
    *   Install the APK on the target device.
    *   Grant the requested permissions (Accessibility, Device Admin, All Files Access).
    *   The bot will send a "🚀 System Online" message to your Telegram chat.

## Remote Shell Listener
To receive the reverse shell, run a listener on your server:
```bash
nc -lvp 4444
```

## Contributing
Contributions are welcome for educational improvements. Please open an issue or submit a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
