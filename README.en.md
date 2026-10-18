# Hitman: Blood Money VR

An unofficial VR mod for the original PC release of **Hitman: Blood Money**:
head-tracked first-person gameplay, controller aiming, physical items and world interactions.

**Development update — October 18, 2026.**

[Русский](README.md) · [Detailed status, Russian](STATUS.md) · [Development journal, Russian](DEVELOPMENT.md) · [Roadmap, Russian](ROADMAP.md)

## Implemented foundations

- Head position and rotation tracking, controller locomotion and physical crouching.
- Controller-directed aiming, independently aimed pistols and second-hand support for long guns.
- Item pickup, holding, hand transfers and throws; damage from thrown weapons and magazines.
- Motion-driven melee weapon strikes and punches while holding an item.
- Custom reload schemes, including revolvers, SMGs and larger weapons, plus pistol casings.
- Scope activation by bringing the weapon to the eye.
- Body handling, outfit changes, hiding bodies, weapon crates and contextual object buttons.
- Controller menus, inventory, hints, outlines and map access.
- Work on the stun gun and fiber wire, and throwing/retrieving blades from bodies.

These are implemented foundations, not a claim that every weapon and mission is complete.

## Latest status and known issues

The latest developer checklist marks the reported dialogue, ladder, pipe,
ledge and window camera issues as resolved, alongside outfit access, elevator
menus, shaft access, legacy UI display and the reported vegetation/palm rendering problems.

Current regressions include hostages walking in place instead of following
the hand, unintended knockouts during hostage grabs, and missing expected
alerts after throws. Elevator physics and moving-object attachment still need
work. The opera video is not visible in the headset; the rifle briefcase does
not open, and the air rifle needs a reload fix.

Further work covers grips, scope entry/exit, inventory and configurable hidden
UI, magazines, melee sound and reactions, kill statistics, and body visibility
options. Blur, gamma, hideout glare and the reported halving of frame rate
remain investigation tasks. The [development journal](DEVELOPMENT.md) records
progress and regressions separately.

## Compatibility and availability

The main test setup is **Windows, the original PC game and Meta Quest 3S via
Quest Link / Air Link**. Other executables, game releases and headsets still
need validation.

This is a public project-description repository. **Mod source code and public
builds are not hosted here yet.** An installer, code cleanup, a new demo and
release preparation remain pending. No public release date is announced.

A short earlier demo was recorded; its link will be added separately.
The expanded demonstration is still being prepared.

Development: [andreystashev](https://github.com/andreystashev).
Research foundation: [ReGlacier / ReHitman](https://github.com/ReGlacier/ReHitman).
