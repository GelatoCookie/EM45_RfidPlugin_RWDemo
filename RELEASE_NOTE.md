# Release Notes - init

## Version: init

### Features
- Initial release of EM45 RFID RWDemo Android application
- DataWedge profile management and auto-creation
- Real-time RFID tag reading and deduplication
- UI status for scanner, RFID, and reader
- Beep feedback for connect/disconnect and ready events
- Modular intent handling for future extensibility

### Documentation
- DESIGN.md: Architecture and design overview
- flowchart TD.mmd: Application flowchart
- TODO.md: Planned improvements and refactoring

---
This is the initial release and codebase import.
# Release Note: 1.0.6.2

## Version: 1.0.6.2

- Added unique-tag display behavior in the result output (`output_view`) to prevent duplicate rows.
- Added read counters in UI (`Total` and `Unique`) and live status updates during decode.
- Added new read-session behavior to clear previous data automatically when reading starts.
- Updated dedupe normalization to ignore case, whitespace, and hyphens for tag uniqueness.
- Updated project/app version to 1.0.6.2 and refreshed copyright year to 2026.
- Updated `README.md` and `DESIGN.md` with current architecture, behavior, and troubleshooting.

---

# Release Note: 1.0.6.1

## Version: 1.0.6.1

- Fixed SecurityException on Android 13+ by adding RECEIVER_EXPORTED flag when registering datawedgeBroadcastReceiver.
- Updated app versioning to 1.0.6.1.
- Updated build/deploy launch flow to use debug package (`com.zebra.rfid.rwdemo.debug`) to avoid persistent system app update conflicts.
- Removed deprecated manifest package usage and cleaned Gradle property deprecations for cleaner build output.

---

# Release Note: init

## Version: init

- Initial project import and cleanup
- Added automation script for build, deploy, and launch
- Project structure for Zebra RFID RWDemo
- Ready for development and deployment on TC22R
