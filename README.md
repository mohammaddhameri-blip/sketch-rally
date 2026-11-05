# Sketch Rally v1.4

**by MrDhameri**

A browser racing game for smartboards and paired phones, with hand-drawn or scanned car designs and automatic Hill Climb, Downhill and Challenge races.

## What's new

- Main-menu creator credit under the Sketch Rally title.
- Empty starting roster; no pre-registered demo racers.
- Draw Your Car now supports freehand pen, eraser, and **filled square, circle and polygon** tools. Pick a palette colour first; polygons have 3–8 sides. Undo continues to work.
- Dedicated **Challenge Mode** with 10 increasingly difficult fixed hill-climb tracks adapted from the user's November 5 Hill Climb Race Level Blueprint.
- The same car design is used in all ten Challenge levels. Editing and wheel adjustments are locked once a run starts.
- An attempt ends if the vehicle gets stuck, overturns or exceeds the level time limit. A fresh design and a restart from Level 1 are required for another attempt.
- **Best Overall** keeps a snapshot of the car design, racer name, levels finished and cumulative time. Full 10-level finishers rank first by fastest total time; incomplete runs follow by levels finished, then lowest cumulative time.
- Normal Hill Climb and Downhill remain available, and Hill Climb course edits are preserved when you temporarily open Challenge Mode.
- Paired host-phone photo capture, image rotation, wheel corrections and the existing race physics remain supported.

## How to play

1. Select Hill Climb, Downhill or Challenge on the main menu.
2. Draw/scan car designs or pair the host phone. The roster initially starts empty.
3. For standard races, prepare the track and start racing.
4. For Challenge Mode, the ten courses are predefined. Start with your completed designs and let the cars compete through the levels automatically.
5. Open **Best Overall** to inspect the completion rankings and car designs.

## Challenge course progression

1. Gentle climb
2. First rolling hill
3. Rolling hills
4. Hill and first ramp
5. Step challenge
6. Rocks and ramp
7. Tyres and step
8. High hill and obstacles
9. Bridge and ramp
10. Ultimate hill climb

## Notes

- Best Overall is currently persisted in browser **localStorage on the smartboard/device**. It is not synchronized between devices and can be cleared from the leaderboard. Clearing browser data may remove it.
- The game is hosted as a static GitHub Pages site. Public cache propagation can lag after a commit.
- The Challenge track geometry uses normalized waypoints derived from the original line drawing; obstacle appearances/physics are adapted to the existing game engine.
- Full browser-based gameplay and physical phone-to-smartboard tests are still recommended after deployment; JavaScript syntax checks have passed.
