# Troubleshooting

## Game/headset output

Confirm normal game launch and the selected executable. Use the mod shortcut; Steam starts the Steam edition. Connect Link/Air Link, wake physical controllers, close the VR dashboard/Desktop and focus the game window. F9 toggles headset output.

If Setup rejects an EXE, report its edition and the displayed message. Do not replace it with an unverified file.

## Flat-screen launch / Meta runtime error 126

Update to **0.1.8.170** if a previous build cannot find the Meta runtime outside
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
you use. Explicit `Backend=OpenXR` remains available. Simply opening SteamVR or
Virtual Desktop does not configure that runtime for you. This update does not
certify every headset/connection combination.

## Sound stays on the PC

A Quest 3 tester using USB confirmed that opening Control Panel Sound settings
and enabling **Oculus Virtual Audio Device** restored headset audio after manual
OpenXR selection. The taskbar volume control had not exposed that disabled
device. This confirms that workaround for that setup; the new 0.1.8.170 automatic
recovery path still needs a separate retest.

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

Release all buttons, wake both controllers, face forward and hold right stick click to recenter. Report persistent drift with the triggering action; arm posing is still under development.

With default settings, A reloads the right-hand weapon on release. Transfer a left-only gun to the right first. Use a short right-stick click for inventory. Physical reloads and pouches are disabled by default.

### Items fall when closing inventory

Hold the right grip **before closing inventory** and keep it held afterward. Closing without grip held drops the selected item. If it still drops while grip stays held, report the item and exact steps.

X/Y menus appear beside your hand: hold the button while selecting with right stick up/down, then release to confirm.

### Choppy headset view or unexpected movement direction

**Disable in-game V-Sync.** The mod renders the eyes on alternating game frames: at 60 game FPS, each eye receives only 30 new frames per second. Higher game frame rates help make the headset view smoother.

Movement direction can behave incorrectly on ledges, while passing through windows or climbing pipes; behavior may vary by headset/setup. These sections still need work.

## Crash or broken interaction

Record the mission, outfit, held items, selected menu label and last action. Include whether the problem occurs outside VR. Use separate saves when testing.

Run `Collect-Diagnostics.cmd` in the installed mod directory. It creates a local ZIP under `diagnostics/` and shows its location. Review it before attaching it to an issue. Nothing is uploaded automatically.

The report contains selected metrics and file-verification results. Raw logs, full INIs, personal paths, screenshots, saves and dumps are not automatically included. Runtime logs remain under `logs/`.

[Open a bug report](https://github.com/andreystashev/hitman-blood-money-vr-showcase/issues/new/choose).
