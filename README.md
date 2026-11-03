# Sketch Rally — v0.7

## Host phone → Smartboard

1. On the smartboard open the game and choose **PAIR HOST PHONE** from the main menu (or **Cars → Pair host phone**).
2. On your phone scan the QR link or open `phone.html`, enter the eight-character room code and connect.
3. Choose **+ New racer**, type the player's name, and select **Top + Side sheet**, **Side view**, or **Top view**.
4. Take a picture using the phone camera or select an existing photo, then tap **Capture & Register**. Wait for confirmation.
5. Repeat to register up to **8 cars**. To add another view to an existing racer, select their name in the dropdown before scanning.
6. Tap **START RACE** on the phone. The smartboard shows the selected fully automatic race mode and starts the animation.

The first remote registration replaces the two sample racers. The live roster updates on the smartboard. The game removes paper backgrounds, thickens sketch lines and estimates wheel positions. The host can preselect either Hill Climb (side view) or Downhill (top view) on the smartboard.

## Existing features

- Two game modes, hand-drawn tracks, in-game drawing of side and top views, automatic photo cleanup, wheel detection and adjustments.
- An individual **3-minute timer** for players drawing and adjusting manually on the smartboard. Cars registered on the host phone count as completed designs and can race immediately. Any active manual design turns must finish before a race.
- All driving remains fully automatic. The main smartboard runs the simulation; the phone sends controls and images.

## Technology and safety

This static GitHub Pages project uses the previously connected Supabase Realtime Broadcast service with a **publishable key**, and needs internet on both devices for pairing. Photo data is compressed and sent through a temporary room, not saved as a permanent online image gallery. Camera permission requires HTTPS; a photo-upload fallback is available. Pairing room codes aren't strong authentication: share them only with the intended host. Registration is blocked while racing. Session data resets on a reload.

## Verification

Both browser scripts passed JavaScript syntax checks. An isolated two-screen browser simulation passed: pairing, two named registrations, replacing sample racers, adding a top view to an existing racer, roster sync and remote starting of Hill Climb. Live physical-device / Supabase production connection has not been tested.