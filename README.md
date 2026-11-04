# Sketch Rally v1.2

## Setup flow

**Smartboard:** The host now follows **1 · Cars → 2 · Track → 3 · Race**. From the main menu select **Design Cars**, draw or scan each sketch in the Garage, then choose **Next: Prepare Track**. Set road shape, hills/corners, obstacles and distance (up to 20 km), then choose **Next: Race**. The Race tab, up-to-30 car support, automatic racing, time limit and rematch remain.

**Host phone:** Connect with a room code or QR, then **take or upload a picture before naming anyone**. Crop/filter the photo and choose **Continue → Assign racer**. The registration dialog asks for a new racer's name or lets you select an existing racer, and allows Side / Top / Both view selection. Press **Register car** to send the sketch to the smartboard. A name is never required to enable the camera or open the editor.

To update or remove an existing racer, expand **Manage existing racers** on the phone. The phone can also start the smartboard race remotely.

## Testing

Chromium browser tests confirmed first-screen Cars, Next Track transition, distance setup, preserved timer race gate, photo upload without prior name, photo editor, post-photo name modal, required-name validation and registration with a simulated pairing channel. Real physical-device pairing has not been retested. Camera access needs HTTPS and internet access for pairing.