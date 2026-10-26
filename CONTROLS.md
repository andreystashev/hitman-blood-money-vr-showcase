# Controls and first steps

These controls describe the default Alpha 4 profile (0.1.8.173) with Meta Touch controllers. All 14 visible modifiers are enabled except Physical crouching, including the Experimental combat modifiers. Physical magazine reloads and body pouches remain disabled.

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
| Physically crouch | Crouch only when the Physical crouching modifier is enabled; off by default |
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

**Painkillers and adrenaline:** highlight the item, hold the chosen hand's grip and close inventory. The game applies a dose directly; it does not become a held item, and your weapon is retained. Release grip before closing to cancel the selection.

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
- **Automatic reload is on by default:** an empty magazine reloads when reserve ammunition is available. Disable **Automatic reload** in Settings → Modifiers to wait for A instead. Ordinary A reload remains available; physical magazine handling is disabled.

## Physical combat — Experimental modifiers

- **Punch knockouts:** hold grip with an empty hand for intentional physical strikes. Head hits can knock out; body hits react, deal small nonlethal damage and accumulate a knockout.
- **Gun butt strikes:** physical firearm strikes use the same nonlethal head/body principle.
- **Physical melee weapons:** blade swings retain lethal damage. Native trigger attacks remain available through their separate modifier.
- **Thrown object hits:** non-blade guns, mines, magazines and props use nonlethal head/body handling. Native blade throws retain their normal behavior.
- **Coins** keep the game's distraction behavior and are excluded from the mod's added hit/damage/knockout logic.

These mechanics need wider mission testing; disable their checkboxes in **Experimental** if unwanted. The latest delayed recognition of an attacker by a civilian still needs a dedicated manual report-to-guard test. Do not assume every witness/report path is correct.

A fiber wire held in the right hand accepts that hand's trigger without a second grip. While crouching at an ordinary unlocked door, the action menu offers **Open Door** as well as the keyhole action.

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
| Movement direction feels wrong during climbing or traversal | Recenter before entry; if it persists on Alpha 4, report the exact location and headset/setup. |
| Item falls even with grip held | Report the item and exact steps вЂ” this may be a bug. |

See [Installation](INSTALLATION.md) for setup and [Troubleshooting](TROUBLESHOOTING.md) for logs and diagnostics.

## Change modifiers and play seated

1. Open **Blood Money VR Settings** on the desktop or in Start, or run `Settings-BloodMoney-VR.cmd` in the installed mod folder.
2. Open **Modifiers**, then choose **Verified** or **Experimental**. Read the description beside each checkbox and change the options you want.
3. **Save & play** saves both pages and launches. **Save** saves only the current page. Restart an already-running game to apply changes.

For example, turn **Automatic reload** off for button-only reloads; turn **Physical crouching** on to crouch by lowering the headset. Physical magazine reloads are a separate unfinished feature and remain off.

For seated play, sit comfortably and recenter with F7 or the held right-stick click. With Physical crouching off, B controls crouching while your head remains tracked. No separate seated-mode INI edit is needed. Recenter again after switching between sitting and standing.

**Installing, updating or reinstalling resets all seven mod INIs to the release defaults**, including these modifier choices and calibration. Only the launcher's game path, connection and language are retained. See [Installation](INSTALLATION.md) before updating. Weapon-specific support grips can still be imperfect.

Turn the right palm toward your face for the Y reminder. Hold Y to see contextual controls for both hands. During supported third-person actions, a short inventory-stick click cycles camera presets.
