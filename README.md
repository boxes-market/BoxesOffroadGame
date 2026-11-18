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
| B | Wings: glide and fly. S pulls up, W dives, A / D bank, Shift pushes, Space airbrakes |
| G / right click | In flight: drop a glitter bomb |
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
- **Places to find:** every region has a landmark, a city, or a road junction. There are fourteen kinds of place in all, and more of each the further you go. A waypoint arrow points to the nearest one you have not found, and the map fills in as you drive.
- **Cities:** a grid of streets with a ring road, buildings with lit windows, parks and street lamps. Buildings are solid, and the grappling hook bites into them.
- **Roads:** every place is linked by road, routed around steep ground and water. Roads are cut into hillsides, banked up across dips and carried over water on causeways, with berms, lamps and hedgerows along them. They are quicker to drive. Narrow side trails break off to dead ends with a lost parcel at each.
- **Physics:** springy suspension, jumps, flips and spins, and tyres that slip: loose ground lets the tail step out, snow more so, and a road holds better. Go fast enough and the truck flattens trees and cacti and rolls over rocks; plough through them slowly, or one after another, and each costs a lot of speed and throws the truck about. Red mushrooms are trampolines.
- **Wings:** press B and the truck unfolds wings and flies as a glider, trading height for speed and back. Hands off, it settles into a long shallow glide; Shift is a push for climbing. Touching down folds the wings, and flying into a building or landmark folds them the hard way.
- **The sky:** floating islands you can land on and drive around, each with a crystal to collect; curving trails of rings that shove you forward; balloons to pop; thermals that lift you; blimps on slow circuits; and now and then a drone circling high up that fires a rocket at the ground, or at you.
- **Glitter bombs:** in flight, G drops one (three at a time, one back every five seconds). Where it lands is yassified for good: pink sparkling ground, flowers, blossom trees, pink buildings with every window lit. A thief or hunter caught in it twirls, sparkles and is out of the game.
- **Grow ops:** some regions hold a fenced compound of plastic tunnels and plant rows around a yard of water tanks, a trailer and a generator. The fence and the plants give way to a truck; the tunnels do not.
- **Parcel thieves:** yellow buggies that run when you get close. Touch one to catch it.
- **Hunter trucks:** black trucks that patrol and hunt by sight. Their red light shows from a long way off, and at night so do their headlights (and the thieves'). Break line of sight behind a hill, or creep through forest, and they lose you. They match your top speed, then tire to 95% after a long chase.
- **Grappling hook:** one throw every 15 seconds. Hit a thief to reel it in, or a hunter to stun it so you can ram it. Miss, and the hook bites into whatever it lands on and drags the truck to it.
- **Race mode:** one waypoint opens the same distance from you and a thief. First there scores, first to 5 wins.
- **Two players:** press "Play with a friend" on the start screen, then "Copy invite link" and send it. Only one of you makes the room; the other just opens the link. You then share one game: the same world (set by the room code), the same waypoint, one set of thieves and hunters that go for whichever of you is nearer, and finds and parcels that count for both. You see each other's trucks (theirs is blue), can bump and hook each other, and key 3 races your friend instead of the thief. A room keeps its own save.

## How two players connect

There is no game server. The two browsers find each other through the public PeerJS broker (`0.peerjs.com`) and then talk directly over WebRTC, using Google's public STUN server to get through home routers. That means each player's IP address is visible to the other player and to those two services, as with any peer-to-peer game. It works on most home networks; some strict office or mobile networks block it.

Progress saves in the browser's local storage. Add `?nosave` to the address to play without reading or writing the save.
