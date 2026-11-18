# Boxes Offroad Game

An in-browser voxel off-road driving game. Drive a 4x4 across a procedurally generated island, find the twelve landmarks, chase parcel thieves, outrun hunter trucks, or race a thief to a waypoint.

The whole game is one file, `index.html`, with no dependencies and no build step. It needs a browser with WebGL2.

## Play

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8090
```

Then go to `http://localhost:8090`.

## Controls

| Key | Action |
| --- | --- |
| W A S D / arrows | Drive and steer |
| Space | Handbrake (drift) |
| Shift | Boost |
| E | Hop. In the air, A / D spins, and Space with W / S flips |
| T | Switch to the next waypoint |
| 1 / 2 | Turn parcel thieves / hunter trucks on or off |
| 3 | Start or leave race mode |
| J / M | Journal of landmarks / full island map |
| C / R | Camera distance / recover the truck |
| H / V | Horn / mute |

## What is in it

- **Terrain:** a voxel island generated from a seed, with grassland, forest, desert, snowfields, mountains, lakes and river canyons. "New island" on the start screen generates a different one. Add `?seed=1234` to the address to pick one.
- **Landmarks:** twelve set points to reach. A waypoint arrow gives direction and distance, and the map fills in as you drive.
- **Physics:** springy suspension, jumps, drifting, flips and spins. Go fast enough and the truck flattens trees and cacti and rolls over rocks. Red mushrooms are trampolines.
- **Parcel thieves:** yellow buggies that run when you get close. Touch one to catch it.
- **Hunter trucks:** black trucks that chase and ram you. Outrun them, or hit them harder than they hit you.
- **Race mode:** one waypoint opens the same distance from you and a thief. First there scores, first to 5 wins.

Progress saves in the browser's local storage. Add `?nosave` to the address to play without reading or writing the save.
