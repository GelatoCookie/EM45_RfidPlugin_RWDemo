# Copilot Workspace Instructions for EM45_RWDemo

## Purpose
This file provides workspace-specific instructions and conventions for GitHub Copilot and AI agents working in this repository. It summarizes build, deploy, and troubleshooting steps, and links to key documentation. 

## Build & Deploy
- **Build APK:**
  - Run: `./gradlew assembleDebug`
  - Output: `app/build/outputs/apk/debug/app-debug.apk`
- **Deploy & Launch (Zebra device):**
  - One-command: `./build_deploy_launch.sh`
  - Manual:
    - `adb install -r app/build/outputs/apk/debug/app-debug.apk`
    - `adb shell am start -n com.zebra.rfid.rwdemo.debug/com.zebra.rfid.rwdemo.RWDemoActivity`

## Requirements
- Android SDK (API 26+)
- Java 8+
- `adb` in PATH
- Zebra device with DataWedge

## Key Files & Docs
- `README.md`: Project overview, build, deploy, troubleshooting
- `DESIGN.md`: Architecture and behavior notes
- `build_deploy_launch.sh`: Build/deploy helper script
- `app/`: Android app source and resources
- `libs/`: Bundled AAR dependencies

## Troubleshooting
- See `README.md` for common issues (Gradle, adb, DataWedge, device connection)
- If `gradle/wrapper/gradle-wrapper.jar` is missing, restore from Gradle release matching `gradle-wrapper.properties`

## Conventions
- Debug build uses package: `com.zebra.rfid.rwdemo.debug`
- Only unique RFID tags are shown per session; deduplication is case/space/hyphen insensitive
- Profile and receiver registration supports Android 13+

## Link, Don’t Embed
- For architecture, see `DESIGN.md`
- For flowchart, see `DW_mermaid_flowchart.md` or `flowchart TD.mmd`

## Example Prompts
- "How do I build and deploy the app?"
- "What are common troubleshooting steps for device connection?"
- "Where is the main activity entry point?"

---
For agent customization, see the [agent-customization skill](copilot-skill:/agent-customization/SKILL.md) for best practices.
