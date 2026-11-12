# JARVIS - Native Android AI Assistant (Kotlin 2.0 & Jetpack Compose)

This is the genuine, complete native Android project for **JARVIS**, built using modern **Kotlin 2.0.0**, **Jetpack Compose Material 3**, and **Android SDK 35**.

---

## 📱 Working from an Android Mobile Phone (e.g. Vivo Y21d)

You do **NOT** need a computer or laptop to build this project into an APK! Below are the 3 best, free ways to build and install JARVIS directly from your Android phone:

---

### Option 1: Automated Free Cloud Build via GitHub (Recommended for Mobile)
This project includes a pre-configured GitHub Actions workflow in `.github/workflows/build-apk.yml`.
1. On your Vivo Y21d mobile browser (Chrome/Brave), open [github.com](https://github.com) and create a free account if you don't have one.
2. Create a new repository named `JARVIS-Android`.
3. Extract this ZIP on your phone (using "Files by Google" or "ZArchiver") and upload the files to your GitHub repository.
4. Go to the **Actions** tab on your GitHub repository. The workflow `Build JARVIS Android APK` will trigger automatically.
5. In ~2 minutes, GitHub builds the clean APK. Tap on the completed build run, scroll to **Artifacts**, and tap `jarvis-debug-apk` to download the installable APK directly to your phone!

---

### Option 2: Build Locally on Your Phone Using "AndroidIDE" (No PC Needed)
**AndroidIDE** is a full-featured native Android Studio environment that runs directly on Android devices.
1. Download **AndroidIDE** on your Vivo Y21d from [androidide.com](https://androidide.com) or F-Droid.
2. Open AndroidIDE and let it download JDK 17 and Android SDK Platform 35 tools.
3. Extract this JARVIS ZIP into your phone's storage (e.g., `/storage/emulated/0/Projects/JARVIS`).
4. In AndroidIDE, tap **Open Project** and select the `JARVIS` folder.
5. Tap the **Play / Build** button. AndroidIDE will compile the Kotlin Compose code and install the debug APK directly on your phone!

---

### Option 3: Build Locally Using Termux (Advanced Mobile Terminal)
1. Install **Termux** from F-Droid.
2. In Termux, run:
   ```bash
   pkg update
   pkg install openjdk-17 gradle
   ```
3. Navigate to the extracted project folder:
   ```bash
   cd /sdcard/Download/JARVIS
   chmod +x gradlew
   ./gradlew assembleDebug
   ```
4. The generated APK will be located at:
   `app/build/outputs/apk/debug/app-debug.apk`

---

## 💻 Building on a PC / Laptop (Standard Android Studio)
1. Extract this ZIP archive to your computer.
2. Launch **Android Studio** (Koala, Ladybug, or newer).
3. Select **File > Open** and choose the `JARVIS` folder.
4. Allow Gradle to automatically sync dependencies from Google & Maven Central.
5. Run on your physical Android phone (with USB debugging enabled) or emulator:
   ```bash
   ./gradlew assembleDebug
   ```

---

## ✅ Verified Project Structure & Compatibility:
- **Target Device**: Vivo Y21d (Android 11/12, MediaTek Helio P35, 4GB RAM)
- **Minimum SDK**: 24 (Android 7.0+)
- **Target SDK**: 35 (Android 15)
- **Kotlin Version**: 2.0.0 with Compose Compiler plugin
- **Gradle Version**: 8.7 (includes verified official `gradle-wrapper.jar`)
- **ProGuard**: Production R8 / ProGuard rules in `app/proguard-rules.pro`
- **Launcher Icons**: Adaptive icons + pre-API 26 vector drawables in `app/src/main/res/`
- **Memory Optimization**: Tuned to 1.5GB max heap in `gradle.properties` to prevent OOM on 4GB mobile phones.
