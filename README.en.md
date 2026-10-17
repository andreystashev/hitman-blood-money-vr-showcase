# Hitman: Blood Money VR

An unofficial VR mod for the original PC release of **Hitman: Blood Money**. Look around and lean in a headset, aim weapons with your hands, pick up items and interact with the world using VR controllers.

**Development update — October 17, 2026.**

[Русский](README.md) · [Features and limitations](STATUS.md) · [Update history](CHANGELOG.md) · [Roadmap](ROADMAP.md)

## What is implemented

- First-person gameplay with head position and rotation tracking.
- Controller-directed weapon aiming, including independently aimed dual pistols.
- Picking up, holding, throwing and transferring items between hands.
- Supporting long weapons with a second hand.
- Controller locomotion and physical crouching.
- Controller access to menus and the inventory.
- Gripping and moving bodies, changing outfits and using the game's body-hiding actions.
- Scope activation by bringing a weapon to your eye.

Physical reloads, melee weapon strikes and living-hostage grips are implemented and still being refined. See the [feature status](STATUS.md) for details.

## Recent improvements

**Interface.** Health, alert level, item names and ammunition now appear inside the inventory. Nearby objects have button hints, and available pickups are highlighted with an outline.

**Interactions.** NPC inventory drops are automatic. Fixes address the right-hand weapon disappearing after inventory use, gripping sleeping bodies and item position on release.

**Weapons and arms.** Left-hand scope aiming and scope exit during reloads, empty magazines and weapon release have received fixes. Elbow poses, grips and mirror arms are still being refined.

**Startup and smoothness.** A conflict that prevented VR startup after mirror-arm changes has been fixed. Scene-item discovery has been improved to address periodic stalls on large levels.

## Work in progress

The next priorities are consistent two-hand grips across weapon models, physical reload refinement and broader mission testing. Items can still bounce or fall through some surfaces. A separate live scope-lens view, improved stereo rendering, haptics and free two-hand fiber-wire interaction remain planned.

## Compatibility and availability

Development targets **Windows and the original PC game**. The primary test headset is **Meta Quest 3S via Quest Link / Air Link**. Other headsets have not yet been validated.

The project is in development. No public test-build date has been announced, and downloadable builds and source code are not currently available on this page.

A short demo has been recorded showing 6DoF weapons, pistols held in both hands and button-reloading the right pistol. A video link will be added separately.

Development: [andreystashev](https://github.com/andreystashev). Research foundation: [ReGlacier / ReHitman](https://github.com/ReGlacier/ReHitman).
