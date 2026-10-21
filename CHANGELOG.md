# Changelog

## Alpha 1 hotfix — 0.1.8.169

- Find the installed Meta runtime through OculusBase, both Windows installation
  registry views and OVRService, with the default location as a fallback.
- Share discovery between x86 head/controller tracking and the x64 Meta host.
- Report attempted paths and distinguish an absent DLL from an existing DLL
  that Windows cannot load, including dependency failures.
- Include the latest continuous gameplay recorder fixes.

Validated: 202 automated checks, real test-DLL loading from non-default Unicode
paths in x86/x64, installed Meta DLL loading without opening a VR session, and
28 isolated installer checks covering update, settings retention and uninstall.
The original tester's Quest 3 launch has not yet been retested. Windows error
126 can also indicate a missing dependency; this release does not guarantee
that every error 126 is resolved. OpenXR remains experimental.

## Alpha 1 — 0.1.8.168

First public installer release for the original PC game.

- Head tracking, tracked hands, controller movement and physical item handling.
- Firearm aiming from either hand, dual wielding and second-hand support.
- Hand-adjacent menus, inventory, map and briefing.
- Conservative defaults: button reload, standard inventory, no debug weapon grants; experimental physical reload/storage/damage systems disabled.
- Recent corrections for scoped trigger handling and skeleton conversion during scoped recoil.
- Preserved selected-item arguments for hand-context Place/Take, including the admission paper in Flatline.
- Separate mod installation, executable checks, preserved settings and local diagnostic export.

This is an alpha. See [STATUS.md](STATUS.md) and [INSTALLATION.md](INSTALLATION.md).

## Before the public alpha

Private development established the camera, controllers, weapons, reload prototypes, scripted views, native menus and installer workflow. Older snapshots were progress reports rather than public download releases; their historical commits remain available here.
