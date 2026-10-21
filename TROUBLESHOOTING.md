# Troubleshooting

## Game/headset output

Confirm normal game launch and the selected executable. Use the mod shortcut; Steam starts the Steam edition. Connect Link/Air Link, wake physical controllers, close the VR dashboard/Desktop and focus the game window. F9 toggles headset output.

If Setup rejects an EXE, report its edition and the displayed message. Do not replace it with an unverified file.

## Flat-screen launch / Meta runtime error 126

Update to **0.1.8.169** if a previous build cannot find the Meta runtime outside
the default installation folder. The mod now checks OculusBase, both installation
registry views and the OVRService path for x86 tracking and the x64 compositor.
The runtime remains installed by Meta; no Meta runtime DLL is bundled with the mod.

An absent `LibOVRRT32_1.dll` under the default Oculus folder does not establish
that Meta is incorrectly installed: it may be located elsewhere. If it still
fails after updating, the new camera log and hands status identify attempted
locations and load errors. An existing DLL can also fail with error 126 when a
dependency is missing. Review logs for personal installation paths before sharing.

Successful game-module injection does not by itself mean that headset output
has started. OpenXR is an experimental alternative selected with `Backend=OpenXR`
under `[VR]` in `vr.ini`; simply opening SteamVR/Virtual Desktop does not switch
a profile configured for the Meta backend. The active PC OpenXR runtime must
also be configured for the connection you are using. Quest 3/Virtual Desktop
compatibility is not newly certified by this hotfix.

## Hands and controls

Release all buttons, wake both controllers, face forward and hold right stick click to recenter. Report persistent drift with the triggering action; arm posing is still under development.

With default settings, A reloads the right-hand weapon on release. Transfer a left-only gun to the right first. Use a short right-stick click for inventory. Physical reloads and pouches are disabled by default.

## Crash or broken interaction

Record the mission, outfit, held items, selected menu label and last action. Include whether the problem occurs outside VR. Use separate saves when testing.

Run `Collect-Diagnostics.cmd` in the installed mod directory. It creates a local ZIP under `diagnostics/` and shows its location. Review it before attaching it to an issue. Nothing is uploaded automatically.

The report contains selected metrics and file-verification results. Raw logs, full INIs, personal paths, screenshots, saves and dumps are not automatically included. Runtime logs remain under `logs/`.

[Open a bug report](https://github.com/andreystashev/hitman-blood-money-vr-showcase/issues/new/choose).
