# Hitman: Blood Money VR

An unofficial VR mod for the original PC release of **Hitman: Blood Money**, with a headset view, first-person camera, tracked hands and controller-directed weapon aiming.

**In development. A short demo has been recorded showing 6DoF weapons, picking up pistols in both hands, and button-based reloading for the right-hand pistol.** This repository is the project's information page. Source code and downloadable builds are not currently published here.

[Русский](README.md) · [Detailed status](STATUS.md) · [Roadmap](ROADMAP.md) · [Demo checklist](DEMO-CHECKLIST.md)

## Shown in the demo

- 6DoF weapon tracking: position and rotation follow the VR controllers.
- Picking up pistols in both hands.
- Button-based reloading for the right-hand pistol only.

This is a short demonstration of the current work-in-progress version. It does not establish that other mechanics are ready or that all missions are stable. Left-hand reloading and physical reloading are not demonstrated in this clip.

## Next milestones

- Validate core gameplay across multiple missions and repeated loads.
- Improve grip alignment, item pickup and arm poses.
- Refine two-hand support, scopes and contextual interactions.
- Improve stereo consistency and rendering performance.
- Refine physical magazine, cartridge, cylinder, pump and bolt interactions.
- Develop a VR inventory interface, fiber-wire interaction, sounds and haptics.

See the [roadmap](ROADMAP.md) for priorities and acceptance criteria.

## Current limitations

Stereo eyes use sequential game frames; fast motion may produce temporal differences between the views. Arm alignment and item grabbing still have reported issues. Scopes currently use the game's fullscreen zoom, without a separate live scope-lens view. Physical reloads are experimental and need further animation, feedback and persistence work. Compatibility targets a particular executable build, and full mission and weapon coverage has not been validated.

## Availability

The primary test setup is **Meta Quest 3S with Quest Link / Air Link on Windows**, using a separately installed copy of the original PC game. Other headset configurations still need testing.

A short demo has been recorded; the video link will be added separately. No public test-build release date has been announced. Requirements, installation instructions and known issues will accompany a future downloadable build.

## Author and research

Developed by [andreystashev](https://github.com/andreystashev). Reverse-engineering research draws in part on [ReGlacier / ReHitman](https://github.com/ReGlacier/ReHitman).

Updated **October 13, 2026**. Priorities may change with playtest findings.
