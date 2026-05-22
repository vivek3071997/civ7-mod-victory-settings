# Victory Settings - Modder's Guide

Welcome to the internal documentation for the **Victory Settings (Endless Turns)** mod. This guide explains the core architecture of the mod, how it achieves compatibility with the Civilization VII 1.4.0 update, and how to use the new Test Mode features.

## Architecture & Overrides

### 1. The Endless Turns Implementation
With the 1.4.0 update, Civilization VII transitioned to a point-based Age progression system. To freeze the progression and achieve "endless turns":
- `data/age-progression-turn-counter-disabled.xml` is used to intercept the progression tables (`AgeProgressionTurns` and `AgeProgressionEvents`).
- We assign `Points="0"` to the baseline turn progression (`AGE_PROGRESSION_PER_TURN_BASE`) and all player milestone/future tech triggers.

### 2. Localization Injection
All configuration screen localization (e.g., the toggles you see when setting up a game) must be injected at the shell level. 
- In `victory-settings.modinfo`, we declare `PanelText.xml` and `ModuleText.xml` in the root `<LocalizedText>` block.
- Using the `<Replace>` database tag ensures that texts immediately overwrite the fallback `LOC_` tags in the UI before a game even starts.
