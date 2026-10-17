# Hitman: Blood Money VR

An unofficial VR mod for the original PC release of **Hitman: Blood Money**, with headset rendering, a first-person camera, tracked hands and controller-directed weapon aiming.

**Updated October 17, 2026.** The core gameplay loop is implemented; interaction refinement and mission testing continue. The integrated internal baseline is .94, with a periodic-stall fix added in .95. This is the public project information page; source code and downloadable builds are not currently distributed here.

[Русский](README.md) · [Detailed status](STATUS.md) · [Recent changes](CHANGELOG.md) · [Roadmap](ROADMAP.md) · [Demo checklist](DEMO-CHECKLIST.md)

## Implemented

- Headset rendering, head position and rotation, first-person view, recentering, controller locomotion and physical crouching.
- Tracked arms, independent dual-weapon aiming, GRIP pickup, release, throwing and hand-to-hand transfer.
- Controller access to the native inventory, with health, alert level, held item names and ammunition shown inside it. English button hints and pickup outlines are implemented.
- Automatic NPC inventory drops, physical body gripping and movement, outfit actions and body-hiding interactions.
- Eye-proximity scope activation, with fixes for left-hand aiming and scope exit on reload, empty magazines and release.
- Native button reload and a separate experimental physical reload system using magazines and weapon mechanisms.
- Adaptation of scripted scenes and Requiem, a camera/mirror-arm startup fix, and incremental scene-item discovery to avoid periodic stalls.

Implementation, gameplay confirmation and full release readiness are different milestones. See the [status tables](STATUS.md) for their boundaries.

## Validation so far

The user confirmed automatic NPC drops, left-hand scope fixes and rendered-position item release in tested scenarios. On October 17, the user confirmed that periodic stalls and arm flashes were resolved in the tested .95 scene. The .94 startup check reached ready VR components and successful headset frame submission. The .95 full automated suite passed **136 checks**. These results do not establish compatibility with every mission, weapon or gesture.

The previously recorded short demo shows only **6DoF weapons, picking up pistols in both hands and button-reloading the right pistol**. It does not demonstrate the later features. A video link has not yet been added.

## Still unfinished

- Consistent two-hand foregrips, grip alignment, elbow poses and mirror arms across weapon models.
- In-headset regression of the new inventory dashboard, action hints, outlines and right-hand retention across missions.
- A stereo pair from one game state and a transfer path without the current CPU copy.
- A completed universal live scope-lens view.
- Physical reload refinement across weapon families, intermediate-state persistence, complete feedback and haptics. Some native magazine models, mechanism animations and sounds already exist.
- Free two-hand fiber-wire interaction and a separate spatial inventory wheel.
- Full mission/load-cycle coverage and validation of other headsets.

Living-hostage grips, physical melee and selected scene-prop interactions remain experimental.

## Compatibility and availability

The primary test setup is **Meta Quest 3S via Quest Link / Air Link on Windows**, using a separately installed original PC game with a supported executable. Other headsets and game versions are not claimed as tested.

The internal `stable-0.1.8.94` tag identifies a reproducible development baseline, not a public release validated through the entire game. No public build release date has been announced.

Development: [andreystashev](https://github.com/andreystashev). Research includes [ReGlacier / ReHitman](https://github.com/ReGlacier/ReHitman).
