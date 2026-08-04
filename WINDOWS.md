# Windows Module Quick Reference

Template for each module entry

## Module: <module-name>
Short description: One-line summary.

Repo: https://github.com/owner/repo  
Original author/maintainer: name (email/handle)  
Status: Active / WIP / Archived / Deprecated  
Tags: windows, android-studio, electron, etc.  
Capabilities (searchable): description of provided capabilities (authentication, sync, media)
Last updated: YYYY-MM-DD

Supported systems (Windows)
- Windows versions: e.g., Windows 10 64-bit, Windows 11
- Windows Subsystem for Android / WSL notes if relevant

Per-system prerequisites (Windows)
- Android Studio (with SDK) — verify by opening Android Studio or `sdkmanager --list`
- OpenJDK/JDK 11+ — `java -version`
- Visual Studio Build Tools (if native/C++/NDK builds) — list installer URL
- PowerShell/Command Prompt tips

Install / run (one-liners)
- Build with Gradle (Windows): `./gradlew assembleDebug` (use Git Bash or PowerShell)
- Install on device: `adb install -r app/build/outputs/apk/debug/app-debug.apk`

Quick verification
- `adb devices` and `adb shell pm list packages | findstr /I <package>`

Key files
- app\\src\\main\\AndroidManifest.xml, build.gradle (Windows path examples)

Known limitations
- e.g., "MSVC required for some native libs" or "path length issues unless LONG_PATHS enabled"

Attribution
- This index thanks the original project authors — please open issues on the original repo for code fixes.
