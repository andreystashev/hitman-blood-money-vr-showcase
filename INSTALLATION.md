# Installation

Use the original PC game, not Reprisal. Launch it normally once. Steam is the primary tested edition. Setup recognizes several other exact executable builds; recognition does not establish gameplay compatibility for every edition. Modified/unrecognized EXEs may be refused.

## Install and launch

1. Connect Quest Link/Air Link and wake both physical Touch controllers. Install Meta's PC software separately.
2. Download Setup from [Releases](https://github.com/andreystashev/hitman-blood-money-vr-showcase/releases).
3. Run Setup and select the detected game or browse to `HitmanBloodMoney.exe`.
4. Choose a writable mod folder separate from the game directory. Game files are not replaced.
5. Close the ordinary game and use the Blood Money VR shortcut. The Steam edition starts through Steam.
6. Wear the headset, close dashboard/Desktop overlays and keep the game window active. F9 toggles headset output if needed.
7. Load a mission and recenter by holding the right stick button for about 0.65 seconds.

Read [Controls](CONTROLS.md) before playing. Keep the supplied button-reload/inventory defaults for initial reports.

## Other runtimes

`vr.ini`, section `[VR]`, accepts `Backend=Auto`, `Meta` or `OpenXR`. OpenXR uses the active PC runtime and is experimental. Controller mappings and headset compatibility need individual testing. SteamVR is not required for the tested Meta path.

## Update and uninstall

Close the game and VR helpers, then run the newer Setup and select the same mod folder. Uninstalling first is not required. Setup replaces its supplied binaries and other matching package files; it does not wipe the entire folder. Existing INI settings, logs and unrecognized user files are retained, except that Setup disables the old debug weapon-grant setting. Items already in saves are not removed. Updating an in-use mod folder is refused rather than forcibly closing the game.

If a folder contains manually mixed builds or third-party modifications, use a new empty mod folder for a clean comparison. Setup does not repair or reinstall Meta Horizon Link, and it does not replace game files.

Rerun Setup to change the selected game. Uninstall through Windows Installed Apps. Settings, logs and unrecognized user files remain; game files stay in place.

## Verify the download

A SHA256 file is provided beside Setup. Compare it with PowerShell's `Get-FileHash -Algorithm SHA256`. The alpha is unsigned; use files from this repository's release page.
