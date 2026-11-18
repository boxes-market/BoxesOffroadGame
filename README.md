# Boxes Offroad Game

An in-browser voxel off-road driving game. Drive a 4x4 across an endless, procedurally generated world, find landmarks and cities, chase parcel thieves, hide from hunter trucks, or race a thief to a waypoint.

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
| F / click | Grappling hook |
| E | Hop. In the air, A / D spins, and Space with W / S flips |
| T | Switch to the next waypoint |
| 1 / 2 | Turn parcel thieves / hunter trucks on or off |
| 3 | Start or leave race mode |
| J / M | Journal of places to find / map of everywhere you have been |
| C / R | Camera distance / recover the truck |
| H / V | Horn / mute |

## What is in it

- **An endless world:** the world has no edge. It is generated a region at a time from a seed as you drive: grassland, forest, desert, snowfields, mountains, seas, river canyons and cities. "New world" on the start screen generates a different one. Add `?seed=1234` to the address to pick one.
- **Places to find:** every region has a landmark, a city, or a road junction. There are thirteen kinds of place in all, and more of each the further you go. A waypoint arrow points to the nearest one you have not found, and the map fills in as you drive.
- **Cities:** a grid of streets with a ring road, buildings with lit windows, parks and street lamps. Buildings are solid, and the grappling hook bites into them.
- **Roads:** every place is linked by road, routed around steep ground and water. Roads are cut into hillsides, banked up across dips and carried over water on causeways, with berms, lamps and hedgerows along them. They are quicker to drive. Narrow side trails break off to dead ends with a lost parcel at each.
- **Physics:** springy suspension, jumps, flips and spins, and tyres that slip: loose ground lets the tail step out, snow more so, and a road holds better. Go fast enough and the truck flattens trees and cacti and rolls over rocks. Red mushrooms are trampolines.
- **Parcel thieves:** yellow buggies that run when you get close. Touch one to catch it.
- **Hunter trucks:** black trucks that patrol and hunt by sight. Their red light shows from a long way off, and at night so do their headlights (and the thieves'). Break line of sight behind a hill, or creep through forest, and they lose you. They match your top speed, then tire to 95% after a long chase.
- **Grappling hook:** hit a thief to reel it in, or a hunter to stun it so you can ram it. Miss, and the hook bites into whatever it lands on and drags the truck to it.
- **Race mode:** one waypoint opens the same distance from you and a thief. First there scores, first to 5 wins.

Progress saves in the browser's local storage. Add `?nosave` to the address to play without reading or writing the save.
