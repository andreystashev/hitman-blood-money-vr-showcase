# Status and known limitations

Alpha 3 (0.1.8.172) is an early public test, not a promise of a bug-free campaign. The primary setup is Steam on Windows x64 with Meta Quest 3S/Touch over Quest Link or Air Link. Virtual Desktop/VDXR head and hand tracking were also checked locally; other hardware/runtime combinations need individual testing.

## Included by default

Headset output and positional tracking; tracked arms; controller locomotion/crouching; firearm aiming from either hand; grip pickup/drop/transfer/throw; second-hand support; supported optics; button reload; hand-adjacent menus; two-hand grip inventory; map/briefing access; adapted scripted cameras.

The settings launcher offers connection/game checks and **Verified** / **Experimental** modifier lists. All visible modifiers start enabled except Physical crouching. Automatic empty-magazine reload is enabled; physical magazine reloads, body pouches and debug weapon grants remain disabled. Experimental combat options can be disabled separately.

## Incomplete or experimental

- Weapon-specific fore-end grips and arm alignment can be imperfect.
- Physical punches, gun-butt strikes, blade swings and thrown-object hits are experimental despite being enabled in this profile. Head/body handling, reactions and weapon-specific interactions need wider mission testing.
- The latest delayed civilian attack recognition/report-to-guard behavior still needs a dedicated manual test; a victim turning toward the player does not establish that every report path works.
- Ledge, window and pipe handling has changed in Alpha 2 and passed local checks. Mission-specific entry/exit transitions and other headset setups still need wider testing.
- Scripted mission actions, outfit changes, traversal, hostages and body interactions need wider testing.
- Scope entry/exit, recoil and weapon upgrades can reveal camera/firing issues.
- Elevators can affect physics and UI placement.
- Dense missions can have frame-time drops. No guaranteed performance target is advertised.
- Mirrors, clothing/body visibility, vegetation and post-processing may show artifacts.
- OpenXR and non-Meta hardware need separate validation.
- Automatic Meta-to-OpenXR recovery and per-game audio routing are included in
  0.1.8.170. Routing is verified against active game audio sessions; unsupported
  Windows interfaces, streams that require restart, and missing audio devices
  still need manual action.

Alpha 3 is designed to keep punches, gun-butt strikes and non-blade object hits nonlethal: head hits can knock out, while body hits react, deal small nonlethal damage and accumulate a knockout. Blade swings retain lethal damage. Coins are excluded from the mod's added hit logic and keep native distraction behavior.

Recent work includes scoped trigger handling, a scoped skeleton-conversion guard and selected-item Place/Take actions. The admission-paper action in Flatline was retested successfully by the developer. These results do not establish correctness for every mission or weapon combination.

Use separate test saves and save before scripted interactions. [Report reproducible bugs](https://github.com/andreystashev/hitman-blood-money-vr-showcase/issues/new/choose) with the mission, equipment and exact version.

Alpha 3 adds fresh settings on every install, accessible settings entry points, mode-aware reload/error messages, revised physical combat, inventory consumables and crouched door opening. It retains the Alpha 2 scope/inventory/traversal fixes. Weapon-specific foregrip alignment remains unfinished and is not advertised as fixed.

Validation for this release: 208 automated Full checks and 69 isolated installer checks passed. The developer checked the prepared release before publication. This does not replace testing every mission, NPC report path or headset setup.
