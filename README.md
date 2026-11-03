# Sketch Rally — v0.6

Draw side-view and top-view cars, scan two-view paper sketches using a paired phone, and race automatically on hill-climb or downhill courses.

## What's new — timed car design

- Every racer gets **one 3-minute turn**, including side/top drawing, scanning, naming and wheel adjustments.
- In **Cars → Garage**, choose a racer and tap **Start 3:00** to begin their turn. The countdown is visible in the Garage, drawing studio and smartboard header.
- Only the active racer can edit. Each player has their own timer. The next racer is selected after a turn ends; their clock does **not** begin until the host presses Start.
- Tap **Finish early** to submit a design before time runs out, or let the timer reach zero. **At zero, current drafts auto-save and editing locks.** An unfinished racer uses the last available artwork or a starter car.
- The timer keeps counting if you close the drawing studio or change screens. A browser page reload resets the unsaved local session, including timers.
- The race is available once all racers have finished or timed out. There is no steering during races.
- You can choose the number of racers before starting the first design turn (1–4 racers). The roster locks once the first turn begins.

## Run

Open `index.html` from the GitHub Pages site. `phone.html` is the optional camera companion. Both are plain HTML. The phone and smartboard need internet for Supabase Realtime camera pairing; the actual race and drawing run locally.

## Other features

- Main menu with **Hill Climb** (side view) and **Downhill Race** (top view)
- Host-drawn hills or winding downhill roads; demo cars animate during setup
- In-game side and top sketch canvases, transparent background, thickened doodle outlines
- A two-panel paper drawing can supply both views, with manual wheel correction
- Four-racer local automatic racing

## Prototype limitations

No persistent player data: refreshing the page resets racers, sketches, timing and tracks. The timer uses the host device's wall clock, so it continues while another tab is open, but a full page reload begins a fresh session. Phone scanning is hosted via a short-lived Realtime Broadcast room and requires the host's approval.