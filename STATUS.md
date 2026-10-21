# Status and known limitations

Alpha 1 is an early public test, not a promise of a bug-free campaign. The primary setup is Steam on Windows x64 with Meta Quest 3S/Touch over Quest Link or Air Link.

## Included by default

Headset output and positional tracking; tracked arms; controller locomotion/crouching; firearm aiming from either hand; grip pickup/drop/transfer/throw; second-hand support; supported optics; button reload; hand-adjacent menus; standard inventory; map/briefing access; adapted scripted cameras.

## Incomplete or experimental

- Weapon-specific fore-end grips and arm alignment can be imperfect.
- Scripted mission actions, outfit changes, traversal, hostages and body interactions need wider testing.
- Scope entry/exit, recoil and weapon upgrades can reveal camera/firing issues.
- Elevators can affect physics and UI placement.
- Dense missions can have frame-time drops. No guaranteed performance target is advertised.
- Mirrors, clothing/body visibility, vegetation and post-processing may show artifacts.
- OpenXR and non-Meta hardware need separate validation.

Physical reloads, body pouches and damage from swings/punches/thrown items are disabled by default. Use A reload and standard inventory for initial reports. Debug weapon grants are disabled.

Recent work includes scoped trigger handling, a scoped skeleton-conversion guard and selected-item Place/Take actions. The admission-paper action in Flatline was retested successfully by the developer. These results do not establish correctness for every mission or weapon combination.

Use separate test saves and save before scripted interactions. [Report reproducible bugs](https://github.com/andreystashev/hitman-blood-money-vr-showcase/issues/new/choose) with the mission, equipment and exact version.
