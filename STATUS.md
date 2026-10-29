# Status and known limitations

Alpha 5 (0.1.8.174) is an early public test, not a promise of a bug-free campaign. The primary setup is Steam on Windows x64 with Meta Quest 3S/Touch. Quest Link/Air Link, Virtual Desktop/VDXR and Steam Link through SteamVR have been checked locally; other hardware/runtime combinations need individual testing.

## Included by default

Headset output and positional tracking; tracked arms; controller locomotion/crouching; firearm aiming from either hand; grip pickup/drop/transfer/throw; second-hand support; supported optics; button reload; hand-adjacent menus; two-hand grip inventory; map/briefing access; adapted scripted cameras.

The settings launcher offers connection/game checks and **Verified** / **Experimental** modifier lists. In SteamVR mode it opens SteamVR if needed and waits for a connected, tracked headset before starting the game; a desktop stream or loaded game modules alone are not reported as a complete VR launch. Physical crouching and Snap turn are disabled by default. Original is the default renderer; DXVK is optional. Performance recording is off by default. Automatic empty-magazine reload is enabled; physical magazine reloads, body pouches and debug weapon grants remain disabled. Experimental combat options can be disabled separately.

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

The current profile is designed to keep punches, gun-butt strikes and non-blade object hits nonlethal: head hits can knock out, while body hits react, deal small nonlethal damage and accumulate a knockout. Blade swings retain lethal damage. Coins are excluded from the mod's added hit logic and keep native distraction behavior.

Recent work includes scoped trigger handling, a scoped skeleton-conversion guard and selected-item Place/Take actions. The admission-paper action in Flatline was retested successfully by the developer. These results do not establish correctness for every mission or weapon combination.

Use separate test saves and save before scripted interactions. [Report reproducible bugs](https://github.com/andreystashev/hitman-blood-money-vr-showcase/issues/new/choose) with the mission, equipment and exact version.

Alpha 5 fixes high-resolution VR capture and transport, adds optional snap turning including during reloads, and keeps Settings from taking focus after a successful Save & play launch. It retains the earlier connection, controller pointing, stereo-pair, audio, gameplay and scope/traversal changes. Weapon-specific foregrip alignment remains unfinished and is not advertised as fixed.

Capture and transport preserve source frames up to 4096×4096 per eye. Runtime scaling and the headset video stream can still affect final resolution and sharpness; the transport dimensions alone do not establish the decoded headset image quality.

Automated regression checks cover high-resolution capture/transport, snap-turn transitions, launch focus, connection/readiness decisions, OpenXR controller poses, stereo frame pairing and audio selection. Local checks used Meta, Virtual Desktop/VDXR and SteamVR with Original and DXVK. These checks do not replace testing every mission, NPC report path or headset setup. See the [Alpha 5 notes](https://github.com/andreystashev/hitman-blood-money-vr-showcase/releases/tag/v0.1.8.174-alpha.5).
