# Linux Module Quick Reference

Template for each module entry

## Module: <module-name>
Short description: One-line summary.

Repo: https://github.com/owner/repo  
Original author/maintainer: name (email/handle)  
Status: Active / WIP / Archived / Deprecated  
Tags: linux, ubuntu, debian, android, server, etc.  
Capabilities (searchable): e.g., headless-server, adb-support
Last updated: YYYY-MM-DD

Supported systems (Linux)
- Recommended distros and versions: Ubuntu 20.04+, Debian 11+, Fedora 36+
- Notes about kernel or udev rules for adb

Per-system prerequisites (Linux)
- OpenJDK 11+ — `java -version`
- Android SDK cmdline-tools & platform-tools — `sdkmanager --list`
- adb and udev rules for device access — `adb devices`
- build-essential, libssl-dev for native builds

Install / run (one-liners)
- `sudo apt install openjdk-11-jdk adb build-essential`
- Build: `./gradlew assembleDebug`

Quick verification
- `adb devices` and `adb shell pm list packages | grep <package>`

Key files
- project Gradle files, native libs

Known limitations
- e.g., "needs extra udev rules for non-root adb access"

Attribution
- Link back to original project for code and issues.
