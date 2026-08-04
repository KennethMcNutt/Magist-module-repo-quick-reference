# macOS Module Quick Reference

Template for each module entry

## Module: <module-name>
Short description: One-line summary.

Repo: https://github.com/owner/repo  
Original author/maintainer: name (email/handle)  
Status: Active / WIP / Archived / Deprecated  
Tags: macos, android-emulator, xcode, etc.  
Capabilities (searchable): e.g., emulator-support, simulator-integration
Last updated: YYYY-MM-DD

Supported systems (macOS)
- macOS versions: e.g., macOS 11+ (Big Sur / Monterey / Ventura)
- Apple Silicon vs Intel notes (Rosetta for some tools)

Per-system prerequisites (macOS)
- Xcode + Command Line Tools — `xcodebuild -version`
- Homebrew packages (list): `brew install wget openssl` etc.
- Android Studio for emulator — `which studio` (or open app)

Install / run (one-liners)
- Build: `./gradlew assembleDebug`
- Run emulator: `emulator -list-avds && emulator -avd <name>`

Quick verification
- `adb devices` and `adb -s <device> shell pm list packages | grep <package>`

Key files
- Android project files, Dockerfile if present

Known limitations
- e.g., "emulator performance on Apple M1 requires specific system images"

Attribution
- Thanks to original project authors — links in each entry point back to the originals.
