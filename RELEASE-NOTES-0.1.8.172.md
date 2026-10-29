# Blood Money VR — Alpha 3 (0.1.8.172)

This release brings the connection/settings launcher and recent gameplay fixes into one installer. Updating now installs the complete current settings profile, so disabled options from an older installation cannot silently carry over.

## Install or update

Close Blood Money and its VR helpers, then run `BloodMoneyVR-0.1.8.172-Setup.exe`. Select your game executable and a separate mod folder. The installer replaces the previous registered copy and updates its shortcuts, including when you choose a different folder. Game files and saves are unchanged.

**Every installation, update and same-version reinstall replaces all seven mod INIs with this release's defaults.** This resets modifier choices, manual VR/audio settings, calibration and weapon-grip adjustments. The game path, launcher connection choice and launcher language are kept. If you want to reuse a manual adjustment, make your own copy before updating and reapply that adjustment afterward.

The supplied profile enables all 14 visible modifiers except **Physical crouching**. Physical reload remains disabled; ordinary button reload is available.

## Change modifiers

1. Open **Blood Money VR Settings** from the desktop or Start menu, or run `Settings-BloodMoney-VR.cmd` in the installed mod folder.
2. Open **Modifiers**. Use **Verified** and **Experimental** to browse the two lists. Each checkbox has a description.
3. Enable or disable the options you want. For example, disable **Automatic reload** for manual button reloads, or enable **Physical crouching** to crouch by lowering the headset. With physical crouching off, use B; recenter with F7 or a held right-stick click when sitting down.
4. Click **Save & play** to save both pages and launch. **Save** only saves the current page. Restart an already-running game to apply changes.

For normal play, use **Blood Money VR**. It uses the selected game and connection without reopening settings. In **Connection & game**, choose Quest Link/Air Link, Virtual Desktop (VDXR), SteamVR or system OpenXR. Connect the headset through that application before launching. Optional Steam/SteamVR shortcuts should point to the installed `BloodMoneyVR.exe`.

## Changes since 0.1.8.171

- Settings shortcuts are available on the desktop and in Start, with a settings entry inside the installed folder. Connection checks and executable compatibility checks help identify missing runtimes or an unknown game build.
- Reload startup messages follow the active mode. A launch-error dialog contains output from that attempt, without old success messages from earlier runs.
- Punches, gun-butt strikes and non-blade object hits use nonlethal head/body handling: head hits can knock out; body hits react, deal small nonlethal damage and accumulate a knockout. Blade swings retain lethal damage. These physical combat options are in **Experimental**.
- Coins use the original distraction behavior and are excluded from the mod's added hit/damage/knockout logic.
- Painkillers and adrenaline can be used by selecting them in inventory, holding the chosen hand's grip and closing inventory. Releasing grip before closing cancels the selection.
- A right-held fiber wire accepts its own trigger without requiring a second grip. Ordinary unlocked doors offer **Open Door** while crouching alongside the keyhole action.
- Attack recognition has been revised for victims and witnesses. The latest delayed recognition/report-to-guard behavior for civilians still needs manual mission testing.

## Compatibility and feedback

Steam Blood Money with Quest/Touch remains the primary setup. Virtual Desktop/VDXR head and hand tracking were checked locally. This does not establish compatibility with every mission, headset or OpenXR runtime; experimental combat and civilian recognition still need gameplay feedback.

Report the version, mission, headset/connection and reproduction steps. `Collect-Diagnostics.cmd` creates a local report for you to review and share manually. No game files or automatic report uploads are included.
