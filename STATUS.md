# Status and known limitations

Alpha 2 is an early public test, not a promise of a bug-free campaign. The primary setup is Steam on Windows x64 with Meta Quest 3S/Touch over Quest Link or Air Link.

## Included by default

Headset output and positional tracking; tracked arms; controller locomotion/crouching; firearm aiming from either hand; grip pickup/drop/transfer/throw; second-hand support; supported optics; button reload; hand-adjacent menus; two-hand grip inventory; map/briefing access; adapted scripted cameras.

## Incomplete or experimental

- Weapon-specific fore-end grips and arm alignment can be imperfect.
- Movement direction can behave incorrectly on ledges, while passing through windows or climbing pipes; behavior may vary by headset/setup. These sections still need work.
- Scripted mission actions, outfit changes, traversal, hostages and body interactions need wider testing.
- Scope entry/exit, recoil and weapon upgrades can reveal camera/firing issues.
- Elevators can affect physics and UI placement.
- Dense missions can have frame-time drops. No guaranteed performance target is advertised.
- Mirrors, clothing/body visibility, vegetation and post-processing may show artifacts.
- OpenXR and non-Meta hardware need separate validation.
- Automatic Meta-to-OpenXR recovery and per-game audio routing are included in
  0.1.8.170. Routing is verified against active game audio sessions; unsupported
  Windows interfaces, streams that require restart, and missing audio devices
  still need manual action. The original reporter's system needs a separate retest.

Physical reloads, body pouches and damage from swings/punches/thrown items are disabled by default. Use A reload and two-hand grip inventory for initial reports. Debug weapon grants are disabled.

Recent work includes scoped trigger handling, a scoped skeleton-conversion guard and selected-item Place/Take actions. The admission-paper action in Flatline was retested successfully by the developer. These results do not establish correctness for every mission or weapon combination.

Use separate test saves and save before scripted interactions. [Report reproducible bugs](https://github.com/andreystashev/hitman-blood-money-vr-showcase/issues/new/choose) with the mission, equipment and exact version.

Alpha 2 specifically addresses persistent scope zoom after reload, inventory input locks, weapon-lifetime crashes after stowing, seated height calibration and outward-facing first-person wall-hug traversal. These fixes have local validation; weapon-specific foregrip alignment remains unfinished and is not advertised as fixed.
