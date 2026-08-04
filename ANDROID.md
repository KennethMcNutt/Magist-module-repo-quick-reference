# Android Module Quick Reference (Android-first)

This file lists Android-focused modules and libraries. Use your browser Find (Ctrl/Cmd+F) to search by module name, tags, or repo owner.

Template for each module entry

## Module: <module-name>
Short description: One-line summary of what the module does.

Repo: https://github.com/owner/repo  
Original author/maintainer: name (email/handle)  
Status: Active / WIP / Archived / Deprecated  
Tags: android, kotlin, flutter, ndk, etc.  
Capabilities (searchable): authentication, image-filtering, offline-storage  
Last updated: YYYY-MM-DD

Supported Android (mandatory)
- API level: e.g., 21+ (Android 5.0+)
- Architectures tested: armeabi-v7a, arm64-v8a, x86_64
- Min SDK / target SDK
- Requires Play services / proprietary SDKs? (yes/no)

Per-system prerequisites (Android — mandatory)
- Java JDK 11+ — verification: `java -version`
- Android SDK cmdline-tools & platform-tools — verification: `sdkmanager --list`
- Gradle or Android Studio (Gradle wrapper recommended) — verification: `./gradlew -v`
- NDK version if native code used — verification: `ndk-build --version` or `cat local.properties`
- Required environment variables (e.g., ANDROID_HOME)

Install / build / run (one-liners)
- Clone & build AAR/APK: `git clone <repo> && cd <repo> && ./gradlew assembleDebug`
- Install on device/emulator: `adb install -r app/build/outputs/apk/debug/app-debug.apk`

Quick verification
- Check package present: `adb shell pm list packages | grep <package>`
- Run sample app and verify UI/feature

Key files
- app/src/main/AndroidManifest.xml, app/build.gradle, src/main/java/.../MainActivity.kt

Known limitations
- e.g., "32-bit devices not supported" or "requires proprietary SDK key"

Attribution
- Link issues/PRs to the original repo. This index does not copy source — please open issues/PRs on the original repository for code changes.

---

### Example entry

## Module: example-android-lib
Short description: Example Android library providing image filtering.

Repo: https://github.com/example/example-android-lib  
Original author: alice@example.com  
Status: Active  
Tags: android, kotlin, image-processing  
Capabilities (searchable): image-filtering, hardware-acceleration
Last updated: 2026-07-30

Supported Android
- API 21+ (Android 5.0+)
- Tested on arm64-v8a and armeabi-v7a
- Requires AndroidX and Kotlin 1.8

Prerequisites
- JDK 11+ — `java -version`
- Android SDK Platform 31 — `sdkmanager "platforms;android-31"`
- Gradle wrapper — `./gradlew -v`

Install / run
- Build AAR: `./gradlew assembleRelease`
- Test on device: `./gradlew installDebug`

Verify
- `adb shell pm list packages | grep example` — should show installed package
