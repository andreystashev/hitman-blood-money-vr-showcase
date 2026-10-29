# Hitman: Blood Money VR

An unofficial VR mod for the **original 2006 PC version of Hitman: Blood Money**. Play with head tracking, motion-controller aiming, tracked hands and physical item handling.

**Alpha 5 — 0.1.8.174.** Full-resolution VR capture, optional snap turning, and a fix for Settings taking focus after Save & play. Original remains the default renderer; DXVK is optional. Snap turn and performance recording are disabled by default. This remains an experimental alpha; mission and hardware coverage is incomplete. [Release notes](https://github.com/andreystashev/hitman-blood-money-vr-showcase/releases/tag/v0.1.8.174-alpha.5).

[Download Alpha 5](https://github.com/andreystashev/hitman-blood-money-vr-showcase/releases/tag/v0.1.8.174-alpha.5) · [Installation](INSTALLATION.md) · [Controls](CONTROLS.md) · [Known issues](STATUS.md) · [Report a bug](https://github.com/andreystashev/hitman-blood-money-vr-showcase/issues/new/choose)

## Features

- Positional head tracking, controller movement, turning and optional physical crouching.
- Aim firearms with either hand, dual-wield pistols and support long guns with a second hand.
- Grab, hold, transfer, drop and throw items using grip.
- Use supported optics by bringing the weapon toward your eye.
- Hand-adjacent action/item menus, inventory, map and briefing.
- Adapted mission interactions, outfit changes, body handling and scripted cameras.

The default profile uses **ordinary button reloads with automatic empty-magazine reload enabled**, plus independent grip selection for each hand in inventory. **Physical crouching and Snap turn are off by default.** Experimental combat modifiers can be changed separately in Settings. Physical magazine reloads, body pouches and debug weapon grants remain disabled. Individual grips and scripted actions can still behave incorrectly.

## Resolution and turning

The VR capture and transport preserve the game's source dimensions up to **4096×4096 per eye**; larger sources are reduced proportionally. Set resolution in the game. The final headset image also depends on runtime scaling and streaming quality. **Original** is the default game renderer; optional **DXVK** is selected independently of the headset connection in Settings.

Enable **Snap turn** in Settings → Modifiers for stepped right-stick turning. The default angle is 45°, configurable in `hands.ini` under `[Input]` with `SnapTurnDegrees` (5–180). Return the stick to center between turns. It also works during reload animations.

Performance recording is off by default. For diagnostics, set `mod.ini` → `[Diagnostics] PerformanceLogging=1`; set it back to `0` to stop recording without restarting.

## Requirements

| Component | Current support |
| --- | --- |
| OS | Windows x64, Windows 10 or later |
| Game | An installed, legally owned copy of the original PC game; Steam is the primary test edition |
| Tested setup | Meta Quest 3S, physical Touch controllers, Quest Link or Air Link |
| Virtual Desktop | VDXR head and hand tracking checked locally |
| Steam Link | Quest 3S through SteamVR checked locally; select SteamVR in Settings |
| Other headsets | OpenXR is experimental; compatibility requires individual testing |

The Meta path does not require SteamVR. This mod is **not for Blood Money — Reprisal**. Setup checks the executable and installs separately without replacing game files. The game and VR runtime are not bundled. Python and a compiler are not needed to play.

## Get started

1. Download **BloodMoneyVR-0.1.8.174-Setup.exe** from Releases, not GitHub's automatic source-code archives.
2. Launch the normal game once, then close it. Connect your headset and wake both controllers.
3. Run Setup, select `HitmanBloodMoney.exe`, and choose a separate writable mod folder.
4. Open **Blood Money VR Settings**, select your connection and game, then click **Save & play**. For Steam Link, select **SteamVR**: the launcher opens SteamVR if needed and checks the connected headset before starting the game. For later launches, use **Blood Money VR**. Keep the game window focused and close the VR desktop/dashboard overlay.
5. Load a mission, face forward and hold the right stick button for about 0.65 seconds to recenter.

With Steam Link, connect to this PC inside the headset first; a desktop stream alone is not a SteamVR VR connection. The game menu appears on a panel in VR; load a mission for the stereo gameplay view. No separate VD/SteamVR game entry is required.

See [Installation](INSTALLATION.md) and [Controls](CONTROLS.md). Use a separate test save and save before unfamiliar scripted interactions.

## Settings and updates

Open **Blood Money VR Settings** on the desktop or in Start, or run `Settings-BloodMoney-VR.cmd` inside the installed mod folder. In **Modifiers**, choose **Verified** or **Experimental**, change the checkboxes, and save. **Save & play** saves both pages and launches; **Save** saves the current page. Restart an already-running game to apply changes.

**Every install, update and same-version reinstall replaces all seven mod INIs with this release's defaults**, including modifiers, calibration, VR/audio and weapon grips. Setup also creates fresh launcher settings: the game and language selected in Setup, **Auto** connection and **Original** renderer. Check your connection choice again after updating. Copy any manual adjustments you want to reapply before updating. Game files and saves are unchanged.

## Before playing

- **Disable in-game V-Sync.** The mod renders the eyes on alternating game frames: at 60 game FPS, each eye receives only 30 new frames per second. Higher game frame rates help make the headset view smoother.
- **Keep grip held when closing inventory** to keep the selected item in your hand; releasing grip drops it.
- **Hold X/Y** for menus beside your hand, select with right stick up/down, then release X/Y to confirm.
- Movement direction can behave incorrectly on ledges, while passing through windows or climbing pipes; behavior may vary by headset/setup. These sections still need work.

## Feedback

Report the release version, mission, outfit, weapon/upgrades, headset/runtime and steps to reproduce. `Collect-Diagnostics.cmd` creates a local report you can review and attach. Nothing is uploaded automatically. Do not post raw dumps, saves or personal files publicly by default.

This repository hosts downloads, documentation and issue reports. Development source is maintained separately. See the [roadmap](ROADMAP.md) and [changelog](CHANGELOG.md).

## Credits

Created by [andreystashev](https://github.com/andreystashev). Reverse-engineering research builds on [ReGlacier / ReHitman](https://github.com/ReGlacier/ReHitman). Third-party components include MinHook, OpenVR, the OpenXR loader and Meta/Oculus SDK; audio policy interface references come from EarTrumpet. Their notices are included with the mod.

Hitman and Blood Money belong to their respective owners. This is an independent community project, not an official IO Interactive product.
