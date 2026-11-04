# Sketch Rally v1.0

Draw, scan, register and race up to 30 custom cars in fully automatic Hill Climb and Downhill modes.

## What's new

- **Original sketch colours:** Black-and-white drawings stay black and white. Automatic paper-background transparency and doodle line thickening remain in place; no automatic colour fill is added.
- **Fine-tune area:** Wheel markers, wheel-size slider, arrow-pad adjustment, re-detection and background-removal controls are located in a panel **below the race display**. The panel automatically selects the latest car registered by the host's phone. A racer picker lets the host select another car.
- **Immersive race view:** Pressing Start Race makes the canvas fill the available smartboard browser viewport, with Pause and Exit view controls. Starting locally also attempts browser-native fullscreen. Web browsers do not ordinarily allow remote phone messages to trigger native fullscreen; a phone-triggered race uses the in-page immersive mode instead. The host may additionally set the browser/device to fullscreen.
- **Phone registration controls:** Select an existing racer, retake or choose a photo, draw a rectangular crop directly on the preview, apply Original / Contrast / B&W / Vivid photo filters, then register the edited image. Choosing an existing racer replaces the selected side/top view(s), while **+ New racer** adds another. The phone also supports **Remove racer**, with confirmation and smartboard roster synchronization.

## Use

1. Smartboard: open `index.html`, choose a mode, then select **Pair host phone**.
2. Phone: scan the QR code or open `phone.html` and enter the room code.
3. Choose + New racer, or select an existing name, capture/choose a car photo, crop/filter, and tap **Register this photo**.
4. Tune wheels below the race screen if necessary.
5. From the phone, tap **Start Race**. The smartboard runs the automated race in immersive view. Tap **Exit view** to return to the controls.

## Existing features retained

30-racer maximum; 3-minute manual drawing timer (optional); optional timed redesign rematch; race length up to 20 in-game km; adjustable engine sound; side and top sketch views; drawn tracks; horizontal sketch flipping; wheel nudges; automatic racing in both modes.

## Notes and limitations

Both devices need internet access for real-time pairing. Camera permissions require a secure (HTTPS) origin, such as GitHub Pages. Race data and images are kept in the current browser session; pairing uses temporary Supabase Realtime Broadcast messages (not a persistent image gallery). Room codes are not a substitute for verified authentication. Browser tests simulated the real-time message channel; a live two-device Supabase connection has not been verified as part of this release.
