# Sketch Rally — v0.5

Draw, scan and race custom cars. Browser game for smartboards with an optional paired phone camera.

## Play
1. Open `index.html`. On the main menu, select **Hill Climb** (side view) or **Downhill** (top view), then **Start Game**.
2. **Track** — choose a preset or draw your own hills / road bends.
3. **Garage** — add racers and give each car a side view and/or a top view.
4. **Race** — watch the fully automatic race. No steering controls.

Use the home icon to return to the main menu. Up to four cars race on one host device.

## Draw or scan two views
- **In-app drawing:** Open **Side view** or **Top view** in the garage. Both tabs share one racer. Switch between them and press **Save views** to register drawings.
- **Two-view paper scan:** Choose **2 views** before taking or uploading a photo. On portrait paper draw **TOP at the top and SIDE at the bottom**. On landscape paper draw **TOP on the left and SIDE on the right**. Keep margins between the sketches.
- **Separate photos:** Choose **Side only** or **Top only**.
- **Cleanup:** The app removes the paper background, trims the image and automatically thickens dark doodle lines. This is heuristic processing, so faint pencils or shadows may need adjustments in **Fine-tune car**.
- The **side view** is used in Hill Climb and the **top view** in Downhill. If no top sketch has been provided, Downhill shows a simplified fallback car.

## Phone camera
On the smartboard, select **Garage → Pair phone**, then scan the QR code using your phone or open `phone.html`. Enter the room code, select a scan type, take a photo and send it. The host reviews before importing.

The camera pairing needs an internet connection and HTTPS. It uses Supabase Realtime Broadcast via a publishable client key; photos and preview frames are sent through a temporary room, and are not intentionally saved to a database. Codes are not authentication secrets; share only with trusted players.

## Prototype notes
The game runs as static HTML / CSS / JavaScript, without a build step. Main racing is local on the host; it does not provide an online lobby or cross-device racing controls. There is no permanent saved garage or track history; work can be lost on reload.
