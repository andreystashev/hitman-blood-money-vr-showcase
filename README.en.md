# Hitman: Blood Money VR

An unofficial VR mod for the original PC release of **Hitman: Blood Money**, with a headset view, first-person camera, tracked hands and controller-directed weapon aiming.

**In development. Core gameplay testing and an initial demonstration of the simplified version are being prepared.** This repository is the project's information page. Source code and downloadable builds are not currently published here.

[Русский](README.md) · [Detailed status](STATUS.md) · [Roadmap](ROADMAP.md) · [Demo checklist](DEMO-CHECKLIST.md)

## Implemented features

- Headset rendering and head-controlled camera movement.
- First-person view and recentering.
- Tracked controllers and in-game arms.
- Weapon-directed aiming and firing, including independent dual-pistol aiming.
- Separate button reloads for the left and right hands.
- Item grabbing, releasing, dropping and hand-to-hand transfer.
- Support for holding long weapons with both hands.
- Controller access to menus, the native inventory and VR settings.
- Experimental scope handling and physical reload mechanisms for multiple weapon families.

Implementation and gameplay validation are separate milestones. Headset rendering, stereo and aiming direction were confirmed in earlier play sessions. The current simplified candidate needs its own validation before the demo; item interactions, scopes and hand poses still need work.

## Initial demo scope

The current test candidate uses **button reloads**: A for the right hand and X for the left. Reloading keeps the weapon in its hand and fills it immediately, without a physical magazine gesture or reload animation.

Experimental physical reloads, automatic body crouching and full-body rendering are disabled by default. The first demo focuses on the camera, hands, firing, ordinary movement, reloading and mission loading.

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

A demonstration video will be added after core validation. No public test-build release date has been announced. Requirements, installation instructions and known issues will accompany a future downloadable build.

## Author and research

Developed by [andreystashev](https://github.com/andreystashev). Reverse-engineering research draws in part on [ReGlacier / ReHitman](https://github.com/ReGlacier/ReHitman).

Updated **October 13, 2026**. Priorities may change with playtest findings.
