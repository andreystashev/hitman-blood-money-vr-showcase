# Troubleshooting

## Game/headset output

Confirm normal game launch and the selected executable. In **Blood Money VR Settings → Connection & game**, select the connection you actually use: Quest Link/Air Link, Virtual Desktop/VDXR, SteamVR or system OpenXR. Connect through that application, wake both controllers, close the VR dashboard/Desktop and focus the game window. Use the mod shortcut; Steam starts the Steam edition. F9 toggles headset output.

If Setup rejects an EXE, report its edition and the displayed message. Do not replace it with an unverified file.

**Check headset** only runs a diagnostic; a runtime window appearing and closing does not launch the game. Use **Save & play** or the ordinary play shortcut. Optional VD/SteamVR shortcuts should target the installed `BloodMoneyVR.exe`. The launcher does not change the global Windows OpenXR runtime setting.

## Steam Link shows a desktop, blank panel or no VR game

Update to **Alpha 4 (0.1.8.173)**. In **Connection & game**, choose **SteamVR**, connect Steam Link to this PC from the Quest and use **Save & play**. The launcher opens SteamVR if needed and checks the actual headset connection before starting the game. If it reports that SteamVR is not ready or no headset is connected, the game has not been started: complete the VR connection, put on the headset and choose **Retry**.

A remote desktop image is not proof of a working SteamVR VR session. First confirm that SteamVR sees the headset and controllers. Close other VR games. **Check headset** only inspects an existing connection; it does not open SteamVR or start Blood Money. You do not need to add Blood Money to SteamVR; an optional library shortcut should target the installed mod launcher, not the original game. See the [Steam Link launch steps](INSTALLATION.md#steam-link-on-quest).

Once the mod starts, the game menu is meant to appear on a panel in VR. Load a mission to check the stereo gameplay view. Close the dashboard/Desktop overlay and keep the game window active. If the launcher reports **pending** output, put on the headset and return to the game; if output is disabled or failed after the game started, focus its window and press F9 to retry. Loading the mod into that same running game again is unnecessary. A modules-loaded message alone no longer counts as a completed VR launch.

For connection failures, keep the PC and headset on the same trusted local network and check the firewall permissions for Steam and VR Server. If you use a VPN, check its local-network/split-tunneling rules on both devices; a VPN being installed does not establish that it caused the failure. The mod does not change network, firewall or VPN settings.

## Settings seem unchanged or the wrong copy starts

Use **Blood Money VR Settings** on the desktop or in Start, or `Settings-BloodMoney-VR.cmd` in the installed folder. Modifier checkboxes are under **Modifiers → Verified / Experimental**. Save, then restart the game.

Every release replaces all seven mod INIs on every install, update and same-version reinstall; old modifier choices, calibration and manual runtime/audio changes do not carry over. Fresh launcher settings use the game and language selected in Setup, Auto connection and Original renderer. Check your connection choice again after updating. Manually copied test folders are separate from the registered installation: check a shortcut's target rather than starting an old test copy.

The launch-error dialog now shows output from that launch. Full logs can contain older attempts. A loaded reload-support DLL does not mean physical reload is enabled; the normal profile reports **button reload**.

If a new launch says the game is already running after its window closed, allow a few seconds for shutdown. Check for `HitmanBloodMoney.exe` in Task Manager if it remains. Save progress before closing an active game, and report a persistent windowless process rather than repeatedly launching another copy.

## A launcher file is missing or blocked

DLL loading can be blocked by antivirus software. If `LaunchCamera.exe` disappears or Windows reports error 225/226, check the exact path in Windows Security Protection history or your antivirus log. Review the download source and release SHA256 before deciding what to do. A detection is not automatically a false positive. The launcher does not disable protection, add exclusions or restore quarantined files.

## Flat-screen launch / Meta runtime error 126

Use **Alpha 4 (0.1.8.173)** if a previous build cannot find the Meta runtime outside
the default installation folder. The mod now checks OculusBase, both installation
registry views and the OVRService path for x86 tracking and the x64 compositor.
The runtime remains installed by Meta; no Meta runtime DLL is bundled with the mod.

An absent `LibOVRRT32_1.dll` under the default Oculus folder does not establish
that Meta is incorrectly installed: it may be located elsewhere. If it still
fails after updating, the new camera log and hands status identify attempted
locations and load errors. An existing DLL can also fail with error 126 when a
dependency is missing. Review logs for personal installation paths before sharing.

Successful game-module injection does not by itself mean that headset output
has started. Startup now reports headset readiness separately; a sleeping or
unfocused headset can remain pending. Auto with `AllowBackendFallback=1` can
recover from persistent Meta startup errors through OpenXR once per launch.
The active PC OpenXR runtime must be installed and configured for the connection
you use. Explicit `Backend=OpenXR` remains available. For Steam Link or VDXR,
choose that connection in Settings so the mod uses its installed runtime.
Opening a desktop stream alone does not establish a VR session. This update
does not certify every headset/connection combination.

## Sound stays on the PC

A Quest 3 tester using USB confirmed that opening Control Panel Sound settings
and enabling **Oculus Virtual Audio Device** restored headset audio after manual
OpenXR selection. The taskbar volume control had not exposed that disabled
device. That workaround applies to the Meta connection; Steam Link uses
**Steam Streaming Speakers** instead.

Alpha 4 fixes automatic playback selection when Steam, Oculus and Virtual
Desktop audio devices are installed together. A runtime endpoint has priority;
otherwise the OpenXR host can identify its selected headset output. Steam
Streaming Microphone is excluded from automatic playback selection. Check the
headset volume and the game's output/mute state in Windows Volume mixer if
sessions are routed correctly but sound is still absent.

The mod tries to route the game's audio to an available headset endpoint. Check
`audioState`, `audioApplied` and `audioVerified` in `logs/camera-status.json`, or
the Audio messages in `logs/camera.log`. Applied is a Windows preference;
verified additionally means the observed active game audio sessions are on
that endpoint. `restart_required` means an existing stream did not move: restart
the game or select its output in Windows Volume mixer. `policy_unavailable`
means automatic routing is unsupported by this Windows interface; use Volume
mixer manually.

For Quest Link over USB, run `mmsys.cpl`, open Playback, right-click empty space
and show disabled/disconnected devices. Enable the headset output if present.
Also check Meta Horizon Link's **Hear Computer Audio in VR** option. If the
Oculus output is absent entirely, repair the Meta PC audio driver/installation;
switching the VR backend cannot create it. For several active headset outputs,
select the desired application output in Volume mixer, or specify an exact
endpoint ID as `[Audio] Output` in `vr.ini` and restart.

Use `[Audio] Output=Default` to restore the application's prior stored preference on
the next launch. The mod does not change Windows' global playback default and
does not install/enable drivers. Do not share the private `.audio-route.state`
file; the diagnostics collector omits it and raw endpoint IDs.

## Hands and controls

Release all buttons, wake both controllers, face forward and hold right stick click to recenter. Alpha 4 corrects the OpenXR pointing orientation that could make SteamVR/VDXR hands or weapons point about 90 degrees upward. If that persists, confirm that the installed Alpha 4 shortcut is running and report the headset, connection and item; bending your wrists or changing weapon grips should not be needed to compensate. Weapon-specific foregrip alignment remains a separate known limitation.

With default settings, A reloads the right-hand weapon on release, and an empty magazine reloads automatically when reserve ammunition is available. Disable **Automatic reload** in Modifiers for button-only reloads. Transfer a left-only gun to the right first. Use a short right-stick click for inventory. Physical magazine reloads and pouches remain disabled.

Physical crouching is off by default; use B. For seated play, sit and recenter with F7 or the held right-stick click. To crouch by lowering the headset, enable **Physical crouching** in Modifiers and restart.

### Items fall when closing inventory

Hold the chosen hand's grip **before closing inventory** and keep it held afterward. You can select an item independently for each hand. Releasing grip inside inventory stows the held item when possible; releasing it outside drops it. If an item drops while grip stays held, report the item and exact steps. Painkillers and adrenaline are applied directly when selected with a held grip and inventory is closed; they do not appear in the hand.

X/Y menus appear beside your hand: hold the button while selecting with right stick up/down, then release to confirm.

### Choppy headset view or unexpected movement direction

**Disable in-game V-Sync.** The mod renders the eyes on alternating game frames: at 60 game FPS, each eye receives only 30 new frames per second. Higher game frame rates help make the headset view smoother.

Movement direction can behave incorrectly on ledges, while passing through windows or climbing pipes; behavior may vary by headset/setup. These sections still need work.

## Crash or broken interaction

Record the mission, outfit, held items, selected menu label and last action. Include whether the problem occurs outside VR. Use separate saves when testing.

Run `Collect-Diagnostics.cmd` in the installed mod directory. It creates a local ZIP under `diagnostics/` and shows its location. Review it before attaching it to an issue. Nothing is uploaded automatically.

The report contains selected metrics and file-verification results. Raw logs, full INIs, personal paths, screenshots, saves and dumps are not automatically included. Runtime logs remain under `logs/`.

[Open a bug report](https://github.com/andreystashev/hitman-blood-money-vr-showcase/issues/new/choose).
