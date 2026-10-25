# Installation

Use the original PC game, not Reprisal. Launch it normally once. Steam is the primary tested edition. Setup recognizes several other exact executable builds; recognition does not establish gameplay compatibility for every edition. Modified/unrecognized EXEs may be refused.

## Install and launch

1. Connect your headset through Quest Link/Air Link, Virtual Desktop/VDXR or your selected SteamVR/OpenXR connection. Wake both controllers; install the required PC runtime separately.
2. Download **BloodMoneyVR-0.1.8.172-Setup.exe** from [Alpha 3](https://github.com/andreystashev/hitman-blood-money-vr-showcase/releases/tag/v0.1.8.172-alpha.3).
3. Run Setup and select the detected game or browse to `HitmanBloodMoney.exe`.
4. Choose a writable mod folder separate from the game directory. Game files are not replaced.
5. Close the ordinary game. Open **Blood Money VR Settings**, select the matching connection and game, then click **Save & play**. The Steam edition starts through Steam.
6. Wear the headset, close dashboard/Desktop overlays and keep the game window active. F9 toggles headset output if needed.
7. Load a mission and recenter by holding the right stick button for about 0.65 seconds.

For later launches, use **Blood Money VR** without reopening settings. Read [Controls](CONTROLS.md) before playing.

## Settings and modifiers

Open **Blood Money VR Settings** from the desktop or Start menu, or run `Settings-BloodMoney-VR.cmd` in the installed folder. In **Modifiers**, switch between **Verified** and **Experimental** to find the checkbox you want. Each option has a description. **Save & play** saves both pages and launches the game; **Save** only saves the current page. Restart the game after saving changes.

All 14 visible modifiers are enabled except **Physical crouching**. Automatic reload and the Experimental physical combat options are enabled. Physical magazine reloads and body pouches remain disabled. Disable **Automatic reload** if you want empty magazines to wait for the reload button. Physical crouching is optional; with it off, use B. For seated play, sit and recenter with F7 or a held right-stick click.

## Before playing

**Disable in-game V-Sync.** The mod renders the eyes on alternating game frames: at 60 game FPS, each eye receives only 30 new frames per second. Higher game frame rates help make the headset view smoother.

Hold the right grip before closing inventory and keep it held to retain the selected item. Hold X/Y to select actions in the menus beside your hand, then release to confirm. See [Controls](CONTROLS.md).

Movement direction can behave incorrectly on ledges, while passing through windows or climbing pipes; behavior may vary by headset/setup. These sections still need work.

## Connection, runtimes and audio

Choose **Quest Link / Air Link**, **Virtual Desktop (VDXR)**, **SteamVR**, or **System OpenXR / custom runtime** in **Connection & game**. Connect through that application before launching. For Virtual Desktop, connect the headset to the PC and select VDXR. For SteamVR, connect the headset so SteamVR sees it, for example through Steam Link. Adding the mod to VD/SteamVR is optional; an optional shortcut should target the installed `BloodMoneyVR.exe`, not the original game EXE.

**Check headset** is a diagnostic, not a game launch: a runtime window may appear and close. The launcher checks executable compatibility and runtime availability. An unknown EXE path can be saved, but that does not permit injecting the mod into an unsupported game build. The Advanced section accepts a custom OpenXR JSON manifest when needed. No global Windows OpenXR runtime setting is changed.

`vr.ini`, section `[VR]`, accepts `Backend=Auto`, `Meta` or `OpenXR`. The new default is Auto. With `AllowBackendFallback=1`, persistent Meta startup errors can trigger one attempt with the active PC OpenXR runtime after the old session stops. The mod changes rendering and controller tracking together; it does not change Windows' active runtime. Set `AllowBackendFallback=0` to keep your selected backend. OpenXR and controller compatibility still need individual testing.

Audio defaults to `[Audio] Output=Auto` in the same file. The mod tries to select an available headset playback endpoint for the game and checks its active audio sessions. The global Windows default is unchanged. Set `Output=Default` and restart the game to restore the application's previous stored playback preference. Existing streams may still require a restart or manual output selection. This cannot create a missing Oculus audio device or repair its driver.

## Update and uninstall

Close the game and VR helpers, then run the newer Setup. Uninstalling first is not required. Setup removes the previous registered copy and updates its shortcuts, including when you choose a different mod folder. It does not wipe the entire folder or modify game files and saves. Updating an in-use mod folder is refused rather than forcibly closing the game.

**Every installation, update and same-version reinstall replaces all seven mod INIs with the supplied profile:** `camera.ini`, `vr.ini`, `hands.ini`, `reload.ini`, `mod.ini`, `weapon-grips.ini` and `grip-tuning.ini`. This resets modifiers, manual VR/audio choices, calibration and weapon-grip adjustments. Only `launcher.ini` preferences — game path, connection and language — are retained. Copy any manual adjustments you want before updating, then reapply them afterward. Logs and unknown user files are not erased.

Windows per-application audio preferences can remain after the game exits. The mod keeps a private recovery journal and can restore its own prior preference on the next launch with `Output=Default` or while VR is inactive. Later user changes take priority. To remove the mod permanently, select the desired output in Windows Volume mixer if needed.

If a folder contains manually mixed builds or third-party modifications, use a new empty mod folder for a clean comparison. Setup does not repair or reinstall Meta Horizon Link, and it does not replace game files.

Rerun Setup to change the selected game. Uninstall through Windows Installed Apps. Settings, logs and unrecognized user files remain; game files stay in place.

## Verify the download

A SHA256 file is provided beside Setup. Compare it with PowerShell's `Get-FileHash -Algorithm SHA256`. The alpha is unsigned; use files from this repository's release page.

The full [Alpha 3 release notes](RELEASE-NOTES-0.1.8.172.md) include the modifier workflow and recent gameplay changes. The ZIP contains the same installer and English/Russian instructions; it is not a portable game installation.
