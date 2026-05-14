# 🌐 EchoCustom Pro: Intelligent Android Personalization Suite

[![Android 16](https://img.shields.io/badge/Android-16%20(API%2036)-green.svg)](https://developer.android.com/about/versions/16)
[![Kotlin 2.1](https://img.shields.io/badge/Kotlin-2.1-purple.svg)](https://kotlinlang.org/)
[![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-blue.svg)](https://developer.android.com/jetpack/compose)
[![Hilt](https://img.shields.io/badge/DI-Hilt-yellow.svg)](https://dagger.dev/hilt/)
[![License](https://img.shields.io/badge/License-MIT-lightgrey.svg)](LICENSE)

**EchoCustom Pro** is a next-generation Android assistant and customization engine. It transforms the mobile experience by blending sophisticated system monitoring with a personality-driven interface, featuring an interactive "Maid" character and a modular Sword Art Online (SAO) inspired HUD.

---

## ✨ Key Features

### 🤖 Maid Assistant
- **Interactive Personality:** A character-driven interface that reacts to your device state (battery, RAM, network) with dynamic, context-aware dialogues.
- **Poke System:** Multi-tap reactions with escalating dialogue responses.
- **Smart Reminders:** Contextual notifications for overdue tasks, hydration, and system optimization.

### ⚔️ SAO-Inspired HUD & UI
- **Modular Dashboard:** Real-time telemetry blocks for CPU (Wave chart), RAM, Storage, and Battery.
- **Glassmorphism & Glow:** A high-fidelity aesthetic featuring neon borders and semi-transparent layers.
- **Adaptive Layouts:** Fully optimized for both Portrait and Landscape orientations, featuring a 2-column resource grid on wide screens.

### 🚀 Performance Navigation
- **Niagara-Style App Drawer:** Ultra-fast, alphabetical navigation with a fluid vertical sidebar.
- **Pinned Apps Dock:** An adaptive dock that repositions based on screen orientation (Horizontal on bottom for portrait, Vertical on side for landscape).
- **Gesture Control:** Advanced edge-swiping and double-tap gestures powered by an integrated Accessibility Service.

### 🎧 Smart Utilities
- **Granular Audio Profiles:** Map unique soundscapes and notification tones to specific apps and VIP contacts.
- **Call & Notification Intelligence:** Sentiment analysis of incoming notifications to drive assistant reactions.
- **Todo & Messaging:** Integrated productivity suite directly accessible from the dashboard.

---

## 🛠️ Technical Stack

| Component | Technology |
| :--- | :--- |
| **Language** | Kotlin 2.1 |
| **UI Framework** | Jetpack Compose (Material 3) |
| **Dependency Injection** | Hilt (Dagger) |
| **Local Database** | Room (with KSP) |
| **Preferences** | Jetpack DataStore |
| **Background Tasks** | WorkManager |
| **System Monitoring** | Custom `SystemRepository` (/proc/stat, TrafficStats) |

---

## ⚙️ Development Automation

The project includes several automation scripts to streamline deployment and resource management.

### 📱 Deployment
Use the provided shell script to quickly deploy the debug APK to a connected device via ADB.
```bash
# First, build the APK
./gradlew assembleDebug

# Then, run the deployment script
./scripts/deploy.sh
```

### 🎨 Resource Management
The project uses Python scripts to sanitize and import external assets into the Android resource system.

-   **Importing Fonts:** Standardizes TTF/OTF files and moves them to `res/font`.
    ```bash
    python3 scripts/import_fonts.py
    ```
-   **Importing Icons:** Standardizes SVG/PNG/XML icons with the `ic_` prefix and moves them to `drawable-nodpi`.
    ```bash
    python3 scripts/import_icons.py
    ```

---

## 📂 Project Structure

```text
.
├── app/                  # Main Android Application module
│   ├── src/main/
│   │   ├── java/         # Kotlin Source Code (MVVM, Hilt, Room)
│   │   ├── assets/       # Icons and application assets
│   │   └── res/          # Android resources (Layouts, Themes, Fonts)
│   └── schemas/          # Room database schema exports
├── docs/                 # Detailed documentation and API examples
├── scripts/              # Automation (Deploy, Asset Imports)
├── README.md             # Project overview
└── build.gradle.kts      # Project-level build configuration
```

---

## 🚀 Getting Started

### Prerequisites
- Android Studio Ladybug (2024.2.1) or newer.
- JDK 21.
- Android SDK 36 (Android 16).
- Python 3.x (for asset scripts).

### Installation
1.  **Clone the Repo:**
    ```bash
    git clone https://github.com/om12345679w0/Project_EchoCustom.git
    ```
2.  **Build:**
    Open the project in Android Studio and sync Gradle.
3.  **Permissions:**
    To enable all features (Gestures, Lock Screen, Notifications), ensure the **Echo Accessibility Service** and **Notification Listener** are enabled in your device settings.

---

## 🌍 Support & Documentation

Visit our [Official Documentation Hub](https://om12345679w0.github.io/Project_EchoCustom/) for:
- 📖 **[Comprehensive User Guide](app_info.html)**
- 📥 **[Latest APK Downloads](download.html)**
- 🛠️ **[Developer API Examples](docs/api-examples/README.md)**
- 🔒 **[Privacy Commitment](privacy.html)**

---
*Developed with ❤️ for the Android Community.*
