# Controls and first steps

These controls describe the default Alpha 2 profile (0.1.8.171) with Meta Touch controllers. Physical reloads, body pouches and motion-driven damage are experimental and disabled by default.

## Before playing

1. **Disable V-Sync in the game.** The mod renders the left and right eyes on alternating game frames. At 60 game FPS, each eye receives only 30 new frames per second, so a higher game frame rate helps the headset view feel smoother.
2. Connect your headset, wake both controllers, and launch using the **Blood Money VR** shortcut.
3. Close the VR desktop/dashboard overlay and keep the game window focused.
4. After loading a mission, face forward and **hold the right stick button for about 0.65 seconds** to recenter.

## Movement and looking

| Input | Action |
| --- | --- |
| Left stick | Walk and strafe relative to your viewing direction |
| Click left stick | Toggle running; disabled while moving a body |
| Right stick left/right | Smooth turn |
| B | Toggle crouching |
| Physically crouch | Crouch in the game |
| Hold right stick button for about 0.65 seconds | Recenter while facing forward |

**Traversal:** the first-person wall-hug camera faces outward, and horizontal input follows the displayed left/right direction. Observer cameras choose clear viewpoints where possible. Mission-specific climbing/window transitions still need wider testing; save before these sections.

## Picking up, holding and throwing items

**Grip is a hold button: keep it squeezed for as long as you want to hold an item.**

- Move your hand near an item and squeeze **grip** to pick it up.
- Keep that hand's **grip held** to retain it.
- Release grip to drop it.
- Move your hand and release grip to throw it.
- To support a long gun with your other hand, bring that hand near the fore-end and hold its grip.

## Choose equipment independently for both hands

1. Short-click the right stick to open inventory. Browse with right stick left/right.
2. Squeeze and **hold** the grip of the hand that should receive the highlighted item.
3. Keep that grip held while browsing. Select another item with the other grip if desired. Left/right markers show the pending hand choices.
4. Short-click the right stick again to close; keep the chosen grips held.

To stow an item, open inventory while holding it, release that hand's grip **inside inventory**, then close. Releasing grip outside inventory drops it instead. Non-concealable weapons are dropped rather than stowed. Opening and closing without changing a hand preserves its item.

A single item instance cannot be held twice. Choosing an already-held item transfers it between hands. Optional native draw/holster animations run sequentially, one hand at a time; normal tracked control resumes after they finish.

## X/Y menus вЂ” hold, select, release

These menus appear **beside your hand**, rather than as a large panel in front of your face.

| Input | Menu |
| --- | --- |
| Hold X | Nearby contextual actions, such as doors and lifts |
| Hold Y | Item/personal menu, including map, briefing and health/alarm/ammunition information |

To use either menu:

1. **Press and keep holding X or Y** to open the menu.
2. While still holding the button, move the **right stick up/down** to highlight an option.
3. **Release X or Y to confirm** the highlighted option.
4. For another menu or a nested selection, fully release the button, then press and hold it again.

Choose **CANCEL** or move the left stick to cancel.

**Do not release X/Y while browsing:** releasing the button confirms the current selection.

## Weapons and reloading

| Input | Action |
| --- | --- |
| Trigger on the hand holding a weapon | Fire; original button attack for melee tools |
| A, on release | Reload the right-hand weapon |
| Bring a supported optic to your eye | Enter scope/binocular view |

- Keep **grip held while aiming and firing**, or you will drop the weapon.
- If your only firearm is in your left hand, **transfer it to the right hand before reloading**.
- The default profile uses **button reloads**. Physical magazine handling is experimental and disabled by default.

## Pause, ordinary menus and settings

| Input | Action |
| --- | --- |
| Left controller Menu button | Pause/back |
| Left stick in ordinary menus | Navigate |
| A in ordinary menus | Confirm |
| B in ordinary menus | Back |
| X on result screens | Continue |
| A/X during movies | Skip when the game allows it |

To open **VR settings**, pause the game, then hold **both stick buttons for about 0.65 seconds**.

### Keyboard shortcuts

| Key | Action |
| --- | --- |
| F6 | Open VR options while paused/in a menu |
| F7 | Recenter |
| F9 | Toggle headset output |
| F11 | Toggle tracked hands and VR controls |

## If something behaves unexpectedly

| Problem | What to try |
| --- | --- |
| Item falls after inventory | Squeeze and hold the grip of the desired hand on its highlighted item, then keep it held while closing inventory. |
| X/Y menu closes too soon | Keep the button held while browsing; release only to confirm. |
| View or hands feel offset | Face forward and hold the right stick button for about 0.65 seconds to recenter. |
| Headset view feels choppy | Check that V-Sync is disabled and the game window stays focused. |
| Movement direction feels wrong during climbing or traversal | Recenter before entry; if it persists on Alpha 2, report the exact location and headset/setup. |
| Item falls even with grip held | Report the item and exact steps вЂ” this may be a bug. |

See [Installation](INSTALLATION.md) for setup and [Troubleshooting](TROUBLESHOOTING.md) for logs and diagnostics.

## Alpha 2 settings and seated play

Existing INI choices survive an upgrade. Set both inventory options below if an old installation still uses Alpha 1 selection.

Restart after changing the following INI options:

| File / section | Setting | Meaning |
| --- | --- | --- |
| mod.ini / Features | LegacyInventory=0 | New independent two-hand selection; 1 restores the old right-hand workflow |
| hands.ini / Input | InventoryGripConfirm=1 | Enable grip selection in inventory |
| mod.ini / Features | InventoryEquipAnimations=1 | Play native draw/holster animations; 0 skips them |
| mod.ini / Features | AutoReload=0 | Require button reload when empty; 1 permits automatic reload |
| mod.ini / Camera | SeatedMode=1 | Calibrate seated eye height; default is 0 for standing |
| mod.ini / Camera | LedgeFirstPerson=1 | First-person ledge view; 0 uses an observer view |
| mod.ini / UI | WristControlHints=1 | Enable contextual hand help |

For seated play, sit comfortably and recenter with F7 or the held right-stick click. Button crouching then uses the character's crouch height without requiring you to stand. Recenter again after switching between sitting and standing.

Physical reloads, body pouches and motion-driven damage remain experimental and disabled by default. Weapon-specific support grips can still be imperfect.

Turn the right palm toward your face for the Y reminder. Hold Y to see contextual controls for both hands. During supported third-person actions, a short inventory-stick click cycles camera presets.
