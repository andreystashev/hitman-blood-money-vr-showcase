# Changelog

## Alpha 2 - 0.1.8.171

- Two-hand inventory selection: select an item with either grip, keep holding it while browsing, then choose a different item for the other hand. Left/right indicators show the pending choices. Closing without making a choice preserves the held equipment.
- Clearer inventory captions and contextual equipment help. Turn the right palm toward your face for the Y reminder; hold Y to see the controls for both hands and health/alarm/ammunition information. Nearby interactions have hand-adjacent previews.
- Optional native draw/holster animations run one hand at a time. Transferring an already-held item skips the animation. Fixed inventory action locks after equipping and a crash when stowing/changing a weapon after shooting.
- Scoped weapons remain usable as optics when empty. Reloading restores the normal VR view and moving the weapon away prevents stale zoom from returning.
- Seated calibration shares the native eye anchor with the hands. Button crouching works without physically standing up. Standing play remains the default.
- More consistent pipe/ledge transitions, short first-person climbing clips and movement rearming after traversal. Continuous observer views choose clear side/raised viewpoints and keep rendering when a preferred viewpoint is blocked.
- First-person wall-hug ledges face outward, follow the character's current turn and map horizontal movement to the displayed view. Updated elevator-hatch discovery includes high/owner-only hatch actions.
- Manual-only empty-magazine reload option. The supplied new-install profile uses button reloads with automatic empty reload disabled.
- Duplicate weapon storage merges compatible ammunition without prematurely destroying weapon objects still referenced by NPC damage logic. Silverballer instances and distinct variants retain their special handling.

Validation: 206 Full checks passed. The installer payload fixtures and installed-launcher check passed. The reported traversal and inventory fixes were tested locally in a headset; all-mission/hardware coverage remains incomplete.

## Alpha 1 update — 0.1.8.170

- Attempt recovery once from persistent Meta initialization errors through the active
  OpenXR runtime, coordinating rendering, head tracking and controller ownership.
- Require fresh tracking, visible headset output and submitted frames before
  reporting headset readiness; show pending output separately from loaded modules.
- Select headset audio for the game process without changing the global playback
  default. Check active game sessions before reporting a verified route.
- Diagnose missing/disabled/ambiguous devices and unsupported routing; preserve
  previous application preferences with recovery state and respect later user edits.
- Add only missing new settings during updates; preserve explicit opt-outs.

This does not install missing audio drivers or certify all SteamVR/Virtual
Desktop configurations. The original reporter later confirmed that manual
OpenXR selection plus enabling the disabled Oculus Virtual Audio Device in
Control Panel restored VR/audio. The new automatic 0.1.8.170 path still needs a retest.

Validation: all 206 checks passed across the Full run and focused retries;
39 isolated installer lifecycle checks passed. Local x86/x64 silent DirectSound
tests verified new streams on the chosen endpoint and restored preferences.
Existing streams did not migrate on this machine; a full game restart was not
tested. Independent processes confirmed unchanged system playback defaults.

## Alpha 1 hotfix — 0.1.8.169

- Find the installed Meta runtime through OculusBase, both Windows installation
  registry views and OVRService, with the default location as a fallback.
- Share discovery between x86 head/controller tracking and the x64 Meta host.
- Report attempted paths and distinguish an absent DLL from an existing DLL
  that Windows cannot load, including dependency failures.
- Include the latest continuous gameplay recorder fixes.

Validated: 202 automated checks, real test-DLL loading from non-default Unicode
paths in x86/x64, installed Meta DLL loading without opening a VR session, and
28 isolated installer checks covering update, settings retention and uninstall.
The original tester's Quest 3 launch has not yet been retested. Windows error
126 can also indicate a missing dependency; this release does not guarantee
that every error 126 is resolved. OpenXR remains experimental.

## Alpha 1 — 0.1.8.168

First public installer release for the original PC game.

- Head tracking, tracked hands, controller movement and physical item handling.
- Firearm aiming from either hand, dual wielding and second-hand support.
- Hand-adjacent menus, inventory, map and briefing.
- Conservative defaults: button reload, standard inventory, no debug weapon grants; experimental physical reload/storage/damage systems disabled.
- Recent corrections for scoped trigger handling and skeleton conversion during scoped recoil.
- Preserved selected-item arguments for hand-context Place/Take, including the admission paper in Flatline.
- Separate mod installation, executable checks, preserved settings and local diagnostic export.

This is an alpha. See [STATUS.md](STATUS.md) and [INSTALLATION.md](INSTALLATION.md).

## Before the public alpha

Private development established the camera, controllers, weapons, reload prototypes, scripted views, native menus and installer workflow. Older snapshots were progress reports rather than public download releases; their historical commits remain available here.
