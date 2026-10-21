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

## Before playing

**Disable in-game V-Sync.** The mod renders the eyes on alternating game frames: at 60 game FPS, each eye receives only 30 new frames per second. Higher game frame rates help make the headset view smoother.

Hold the right grip before closing inventory and keep it held to retain the selected item. Hold X/Y to select actions in the menus beside your hand, then release to confirm. See [Controls](CONTROLS.md).

Movement direction can behave incorrectly on ledges, while passing through windows or climbing pipes; behavior may vary by headset/setup. These sections still need work.

## Other runtimes

`vr.ini`, section `[VR]`, accepts `Backend=Auto`, `Meta` or `OpenXR`. The new default is Auto. With `AllowBackendFallback=1`, persistent Meta startup errors can trigger one attempt with the active PC OpenXR runtime after the old session stops. The mod changes rendering and controller tracking together; it does not change Windows' active runtime. Set `AllowBackendFallback=0` to keep your selected backend. OpenXR and controller compatibility still need individual testing.

Audio defaults to `[Audio] Output=Auto` in the same file. The mod tries to select an available headset playback endpoint for the game and checks its active audio sessions. The global Windows default is unchanged. Set `Output=Default` and restart the game to restore the application's previous stored playback preference. Existing streams may still require a restart or manual output selection. This cannot create a missing Oculus audio device or repair its driver.

## Update and uninstall

Close the game and VR helpers, then run the newer Setup and select the same mod folder. Uninstalling first is not required. Setup replaces its supplied binaries and other matching package files; it does not wipe the entire folder. Existing INI settings, logs and unrecognized user files are retained, except that Setup disables the old debug weapon-grant setting and adds missing new recovery/audio keys. Existing explicit choices, including `AllowBackendFallback=0` and `Output=Default`, are preserved. Items already in saves are not removed. Updating an in-use mod folder is refused rather than forcibly closing the game.

Windows per-application audio preferences can remain after the game exits. The mod keeps a private recovery journal and can restore its own prior preference on the next launch with `Output=Default` or while VR is inactive. Later user changes take priority. To remove the mod permanently, select the desired output in Windows Volume mixer if needed.

If a folder contains manually mixed builds or third-party modifications, use a new empty mod folder for a clean comparison. Setup does not repair or reinstall Meta Horizon Link, and it does not replace game files.

Rerun Setup to change the selected game. Uninstall through Windows Installed Apps. Settings, logs and unrecognized user files remain; game files stay in place.

## Verify the download

A SHA256 file is provided beside Setup. Compare it with PowerShell's `Get-FileHash -Algorithm SHA256`. The alpha is unsigned; use files from this repository's release page.
