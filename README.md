# Sketch Rally v1.3

Sketch Rally is a browser racing game with hand-drawn cars, automatic Hill Climb and Downhill races, and optional phone-to-smartboard camera pairing.

## Updates in v1.3

- Version number **v1.3** now appears immediately beside the Sketch Rally name in the smartboard header and phone header. The separate badge has been removed.
- Cleaner Garage preview: redundant Garage labels, help overlay, demo caption and footer controls are hidden on the Cars screen, while Track and Race retain their necessary information.
- Duplicate fine-tuning status text has been hidden.
- **Photo rotation on host phone:** After capture or upload, use Rotate 90° left/right or the fine rotation slider (−180° to +180°) before cropping, filtering and assigning to a racer. Saved images use the corrected orientation.
- **Photo rotation on smartboard:** The Side/Top scanning dialog offers the same 90° rotate controls and a fine rotation slider before registering a car.

## Game flow

1. On the smartboard open the game and select Hill Climb or Downhill, then choose Design Cars.
2. Draw car views directly or take/upload paper sketches. On the host phone, pair using the room QR or code.
3. Rotate/crop/filter a phone photo, register under a player's name, and repeat for multiple racers.
4. Prepare the track and start the fully automated race.

## Notes

- Phone pairing needs internet on both devices; camera access requires HTTPS and device permission.
- Background removal, line thickening, horizontal flipping, wheel fine-tuning and up to 30 racers remain available.
- Rotating a photo resets any existing crop selection so the entire image remains available for the next crop.
- This is a temporary client-side session. Refreshing may reset racers and race progress.

## Verification

JavaScript syntax checks passed. Headless browser tests verified the cleaner smartboard Garage, the corrected scanner rotation preview and save flow, and the phone photo editor's 90° buttons and free-angle slider. Physical phone-to-smartboard pairing and public GitHub Pages cache propagation have not been independently tested.
