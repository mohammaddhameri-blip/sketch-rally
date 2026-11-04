# Sketch Rally — v1.1

Sketch Rally is a browser racing game for hand-drawn cars, with automatic Hill Climb and Downhill Race modes, up to 30 racers, and a paired host-phone camera.

## What's new in v1.1

- **Double-tap a racer name** in the smartboard racer list to rename it inline. Enter saves, Escape cancels.
- **Design your car:** One `Draw your design here!` button opens the drawing studio, where players can switch between Side and Top view.
- **Scan drawings:** Separate `Take photo` and `Upload photo` controls open the scanner. Side view is selected by default, and a Side/Top switch is available before saving the photo.
- **Fine-tune car:** Flip Side and Flip Top moved beneath the main game screen with the tyre correction controls.
- **Host phone:** Pairing is accessed from `PAIR HOST PHONE` on the main menu, via a pairing dialog instead of a permanent Garage section. The mobile controller remains `phone.html`.
- **One race-start button:** A leaf-green `🏁 BEGIN RACE! 🏁` button is centered over the game canvas during setup, with animated flags and jumping letters. It launches the full-auto race directly and disappears during racing. Race navigation and reset/rematch remain separate.

## Existing capabilities

- Side/top car drawings and scanning, automatic transparent-paper cleanup and outline thickening; monochrome sketches remain monochrome.
- Host-controlled phone registration and remote race start.
- Up to 30 car registrations, configurable tracks up to 20 km and two automatic race modes.
- Optional 3-minute racer design turns, flip/tyre correction, synthesized engine volume and rematches.

## Hosting

Put `index.html` and `phone.html` at the root of the GitHub repository; enable GitHub Pages from `main` / `(root)`. Use HTTPS for phone camera permission. Host-phone pairing requires both devices to be online.

## Verification

JavaScript syntax and isolated browser checks passed for inline rename, timer settings, the drawing studio, scanner side/top photo import, transferred Flip controls and launching the auto race from the animated center button. Actual public Pages deployment timing and physical phone-smartboard pairing were not retested in this release.
