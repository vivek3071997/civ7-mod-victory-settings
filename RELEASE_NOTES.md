# Release Notes

## Version 1.4.0 Compatibility Update

This major update brings full compatibility with the Civilization VII "Test of Time" (v1.4.0) patch and resolves long-standing UI localization issues.

### 🌟 New Features
* **Natural English UI**: The Advanced Setup menu has been completely localized. You will now see proper English labels (e.g., "Military Victory", "Age Progression", "Turn Counter") instead of raw `LOC_` tags when configuring your game.

### 🛠️ Compatibility & Fixes (1.4.0)
* **Endless Turns Restored**: The mod has been fully rewritten to support the new point-based Age progression system introduced in 1.4.0. Turn counters, player milestones, and future era tech/civics have had their progression points correctly zeroed out to maintain the endless turns experience.
* **Database Syntax Fixes**: Removed deprecated `AgeProgressionMilestones` blocks across all victory disable files. This resolves the game-breaking `[gameplay] ERROR: no such column: AgeProgressionAmount` bug that caused database rollbacks.
* **Initialization Fixes**: Removed references to missing German localization text files that were preventing the mod from initializing correctly on launch.

### 👨‍💻 Developer & Modder Additions
* **Modder's Guide**: Added `MODDERS_GUIDE.md` containing architectural documentation on how the mod overrides shell localization.
