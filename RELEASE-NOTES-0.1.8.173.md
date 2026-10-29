# Blood Money VR — Alpha 4 (0.1.8.173)

This update focuses on Steam Link/SteamVR startup, OpenXR controller pointing, stereo frame pairing and headset audio. The settings launcher and the Alpha 3 gameplay/modifier profile remain available.

[Download Alpha 4](https://github.com/andreystashev/hitman-blood-money-vr-showcase/releases/tag/v0.1.8.173-alpha.4) · [Installation](INSTALLATION.md) · [Controls](CONTROLS.md) · [Troubleshooting](TROUBLESHOOTING.md)

## Install or update

Close Blood Money and its VR helpers, then run `BloodMoneyVR-0.1.8.173-Setup.exe`. Select the original game's executable and a separate writable mod folder. Setup replaces the previous registered copy and updates its shortcuts. Game files and saves are unchanged.

**Every install, update and same-version reinstall replaces all seven mod INIs with this release's defaults.** Modifier choices, manual VR/audio settings, calibration and weapon grips are reset. The selected game, launcher connection and language are kept; the play launcher now reapplies that saved connection after the reset.

## Launch with Steam Link

1. Install Steam/SteamVR on the PC and Steam Link on Quest. Connect to this PC from Steam Link in the headset and wake both controllers. Close other VR games.
2. Open **Blood Money VR Settings → Connection & game**, choose **SteamVR** and your game, then click **Save & play**.
3. The launcher opens SteamVR if necessary and checks the connected headset, tracking and compositor before starting Blood Money. If the connection is not ready, the game has not been started: complete the VR connection, put on the headset and choose **Retry**.
4. Close the dashboard/Desktop overlay and focus Blood Money. The menu is shown on a panel in VR; load a mission for stereo gameplay. Recenter by holding right stick click for about 0.65 seconds.

A streamed desktop alone is not a SteamVR VR connection. **Check headset** inspects an existing connection without starting SteamVR or the game; **Save & play** performs the launch sequence. Later launches can use **Blood Money VR** without reopening Settings.

No extra game entry in VD or SteamVR is required. An optional Steam/SteamVR library shortcut should target the installed `BloodMoneyVR.exe`, not the original game. The Steam edition starts through Steam when launched with the mod. For VD, select **Virtual Desktop (VDXR)** and connect to the PC in Virtual Desktop before playing. For Link/Air Link, enter its PC VR session and select that connection.

## Fixes in this update

- Saved connection choices are used after an update resets the rendering INI.
- VR module loading waits for the native game window and renderer. Loading DLLs successfully no longer counts as confirmation that VR output is working: pending or failed output is reported separately. Focus the running game and use F9 to retry headset output after restoring the connection.
- OpenXR controller pointing is corrected for SteamVR/VDXR, addressing hands and weapons angled upward by about 90 degrees.
- SteamVR receives matching left/right eye images from the same stereo pair.
- The OpenXR host supplies a headset playback hint when the runtime has no audio-device extension. Steam Link can select **Steam Streaming Speakers** even with Oculus/Virtual Desktop outputs installed and an older per-game preference. **Steam Streaming Microphone** is excluded from automatic playback. The mod checks active game audio sessions and leaves the global Windows output unchanged.

## Change modifiers

Open **Blood Money VR Settings → Modifiers**, choose **Verified** or **Experimental**, change the checkboxes and save. **Save & play** saves both pages and launches; **Save** saves the current page. Restart an already-running game to apply changes.

All 14 visible modifiers are enabled except **Physical crouching**. Disable **Automatic reload** for button-only empty-magazine reloads. Enable **Physical crouching** to crouch by lowering the headset; with it off, use B. For seated play, sit and recenter normally. Physical magazine reloads and body pouches remain disabled. See the [Alpha 3 notes](RELEASE-NOTES-0.1.8.172.md) for the retained combat, consumable and door changes.

This is still an alpha. Weapon-specific foregrips, experimental combat, civilian reporting and mission-specific interactions need more feedback. Local Quest/Touch connection checks do not establish compatibility with every headset or mission. Report the exact version, headset/connection, mission and steps. `Collect-Diagnostics.cmd` creates a local report for review and manual sharing; nothing is uploaded automatically.
