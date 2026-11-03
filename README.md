# Sketch Rally v0.8

Sketch Rally is a browser game for hand-drawn cars, automated Hill Climb and Downhill racing, and phone-to-smartboard camera registration.

## How to play

- **Smartboard:** Open `index.html`. Choose a mode, edit the track, register racers, then start.
- **Host phone:** Pair with the room code or QR in the smartboard garage. Open `phone.html` to scan, name and register cars and to send the race start command. Internet access is needed on both devices; camera permission requires HTTPS.

## New in v0.8

- **Settings:** Accessible from the main menu and top-right gear. Enable/exit full screen on supported browsers.
- **Time limit:** Toggle the 3-minute per-racer design deadline on or off. Off means unrestricted drawing and adjustments in the garage. The preference is saved locally.
- **Car sound volume:** 0–100% slider for a synthesised engine tone. Volume is saved locally. Browser sound may require one tap on the smartboard before a phone-initiated race can produce audio.
- **Flip sketches:** Horizontal flip for side and top drawings, including scanned photos.
- **Fine wheel adjustment:** Four arrow buttons for the selected wheel, with 1/3/6-pixel steps; the canvas also supports keyboard arrow nudges.
- **Auto-colour monochrome cars:** Fills plausible body spans with at least one solid racer colour, while retaining dark linework and transparent paper. It's approximate automatic colouring, not AI interpretation.
- **Timed rematch:** When the timer is enabled, completed races offer a Rematch button. Each existing racer gets another 3 minutes to refine their car before the next race.
- **Track length:** 1, 2, 5, 10 and **20 km**. Longer distances actually extend simulation and progress by repeating the host-drawn section, alternating its direction for continuous terrain. The km values are in-game distance units, not real-world scale. A slow starter can catch up over a longer race, but is not guaranteed to win.

## Existing features

Two fully automatic racing modes, side and top car art, digital drawing, paper scanning, transparent-background processing, doodle line thickening, track editor, up to 8 racers, animated setup, phone registration and remote start remain available.

## Verification

The JavaScript parses successfully. Desktop Chromium checks covered settings, timer on/off, wheel nudges, flipping, 20 km downhill racing, timed rematches, and single-colour fill for black-and-white sketches. Physical phone-to-smartboard pairing and public Pages deployment were not re-tested in this update.
