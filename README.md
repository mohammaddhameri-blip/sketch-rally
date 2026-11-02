# Sketch Rally — Playable Prototype v0.1

A self-contained 2D car sketch and automated racing prototype. No server, login, packages or external libraries are needed.

## Open the game

Open `index.html` in a current Chrome, Edge or other modern browser, or upload the contents of this folder to a static web host such as GitHub Pages. Phone users can use the image picker/camera capture to add their car drawings.

## Play

1. **Track:** Choose a preset or select Draw and drag left-to-right across the track area to draw a road. Select Rock and tap to add an obstacle; Erase removes the nearest obstacle.
2. **Cars:** The game starts with two sample cars. Select a racer, enter a name and use Capture or upload to import a side-view sketch on plain paper. The background is removed and two wheel positions are estimated.
3. **Correction:** Drag the two colored circles onto the wheels in the sketch. Select each wheel and set its size with the slider. Add up to four racers.
4. **Race:** Press Start race. All racers use standardized engine force, and the simulation handles acceleration, gravity, wheel traction, chassis contact and rocks. Rankings and finish times appear automatically.

## Current prototype scope

- **Multiplayer:** Local, shared-device multiplayer with 1–4 car designs. Players take turns importing their drawings onto the same game device. No real-time phone-to-host sync or online lobby yet.
- **Scanning:** Heuristic background removal and estimated round wheel detection, with manual adjustments. It is not an advanced machine-vision model and won't recognize every drawing correctly.
- **Track:** Continuous 2D road profile and rocks. It does not yet support tunnels, overhangs, loop-the-loops or arbitrary 2D obstacle art.
- **Race physics:** Experimental lightweight browser simulation; results are not realistic engineering measurements. Very difficult tracks may leave every racer stuck.
- **Storage:** Runs locally without uploading images; drawings and tracks are not saved between reloads.

## Suggested next development phase

Phone-to-host code/QR joining, persistent car garages, improved wheel/background detection, more obstacle types, saved tracks and online shared racing sessions.