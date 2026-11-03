# Sketch Rally — Playable Prototype v0.4

A self-contained 2D car sketch and automated racing prototype with an in-game drawing studio and animated setup preview. Core racing needs no server or login. Phone pairing uses an internet-connected Supabase Realtime service; the two hosted pages load a client library from a CDN.

## Open the game

Open `index.html` in a current Chrome, Edge or other modern browser, or upload the contents of this folder to a static web host such as GitHub Pages. Phone users can use the image picker/camera capture to add their car drawings.


## New in v0.3: Phone as smartboard camera

On the **smartboard**, open the game, choose **2 · Cars**, select the racer you want to replace and click **Create pairing code**. Scan the QR code on your phone (or open `phone.html` and enter the 8-character code). The smartboard shows a low-resolution preview while the phone camera is on. Captured photos appear for host review; click **Use for selected racer** or **Discard**.

On the **phone**, open the camera page, connect, tap **Start camera**, allow permission, aim at a side-view car sketch and tap **Capture & send to smartboard**. A photo-upload fallback is available if camera permission is denied. The host may edit the car's wheel positions after importing.

**Automatic background transparency:** Scans use adaptive local contrast and colour differences to remove paper and soft shadows; a **Background removal** strength slider lets the host tune the result. Built-in canvas drawings remain transparent. Results are approximate; detailed shadows and faint pencil marks may require adjustment.

**Network and privacy:** This is a temporary Realtime Broadcast room, using your existing connected Supabase platform with a public publishable key. No database photo uploads or persistent online roster are involved. Both devices require internet access, and camera access needs HTTPS (GitHub Pages works). Room codes are not an authentication system, so keep codes private. The camera companion transmits only within the paired room, and snapshots require host approval. The race itself runs on the smartboard, not on the phone.

## New in v0.2: Draw cars inside the game

1. Open **Cars**, select a racer, and tap **Draw car in game**.
2. Draw a side-view car directly on the canvas with a mouse, stylus or finger. Include a body and two wheels.
3. Use pen colours, brush size, eraser, undo or clear to edit the sketch.
4. Tap **Use this car**. The game crops the drawing, estimates two wheel positions, and uses the sketch as the actual racer graphic.
5. Drag the wheel markers and adjust their sizes if the estimation needs correcting. You can reopen your saved in-game drawing and make changes.

**Alternative:** Capture a photo of a sketch on paper or upload an image as before.

## New in v0.2: Animated setup preview

While the host designs the course, the track editor shows animated demo cars using the current road. During car setup, the main game screen loops a cinematic side-view race on the host's track. Tap **Demo on / Demo off** to toggle these animations. The demo is **visual only** and is not the official physics race; the official race only starts when **Start race** is pressed.

## Play

1. **Track:** Choose a mode and preset, or select Draw and drag in any direction across the track preview to reshape the road. Select Rock and tap to add an obstacle; Erase removes the nearest obstacle.
2. **Cars:** The game starts with two sample cars. Select a racer, enter a name and use Capture or upload to import a side-view sketch on plain paper. The background is removed and two wheel positions are estimated.
3. **Correction:** Drag the two colored circles onto the wheels in the sketch. Select each wheel and set its size with the slider. Add up to four racers.
4. **Race:** Press Start race. All racers use standardized engine force, and the simulation handles acceleration, gravity, wheel traction, chassis contact and rocks. Rankings and finish times appear automatically.

## Current prototype scope

- **Multiplayer:** 1–4 racers on the smartboard. A paired phone can send sketches in real time, but the track and race still run on the host device (no online lobby).
- **Scanning:** Heuristic background removal and estimated round wheel detection, with manual adjustments. It is not an advanced machine-vision model and won't recognize every drawing correctly.
- **Track:** Hill Climb supports a continuous side-view terrain profile and rocks; Downhill supports a top-down winding road. Neither supports tunnels, overhangs or fully arbitrary 2D obstacle art.
- **Race physics:** Experimental lightweight browser simulation; results are not realistic engineering measurements. Very difficult tracks may leave every racer stuck.
- **Storage:** Phone photos and previews travel ephemerally through Supabase Broadcast; there is no saved photo archive. Drawings and tracks are not persisted between reloads.

## Suggested next development phase

Persistent garages, stronger wheel/background detection, more obstacle types, saved tracks and online shared racing sessions.