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
| 3 | Race: next to a pack of street racers, race them; at a racetrack, line up on the grid; anywhere else, race mode against a thief |
| J / M | Journal of places to find / map of everywhere you have been |
| C / R | Camera distance / recover the truck |
| H / V | Horn / mute |

## What is in it

- **An endless world:** the world has no edge. It is generated a region at a time from a seed as you drive: grassland, forest, desert, snowfields, mountains, canyon country, alpine valleys, seas and cities. "New world" on the start screen generates a different one. Add `?seed=1234` to the address to pick one.
- **Places to find:** every region has a landmark, a city, or a road junction. There are fifteen kinds of place in all, and more of each the further you go. A waypoint arrow points to the nearest one you have not found, and the map fills in as you drive.
- **Canyon country:** red tablelands cut by deep, winding gorges with a river along the bottom, narrower slots off to the sides, rock spires on the floor and natural bridges overhead. The walls are cliffs: a truck gets in where a gorge opens out or a road comes down. On the wings, the gorges are for flying through. There is always canyon country west of the start.
- **Alpine country:** the green version of the canyons. Wide valleys with a river or a deep lake along the floor, flower meadows, timber chalets, a belt of pines on the slopes, then rock and snow. Cows and goats graze the meadows, and the bigger lakes have boats. There is always alpine country south-east of the start.
- **Big mountains:** peaks well over 100 m, ringed with cliff bands. A cliff is a wall however fast it is hit, and on steep ground the tyres spin instead of climbing, more so on snow and sand than on rock. Each mountain has three gullies that wind from foot to summit with no cliffs in them: a worn track marked with orange flags. Ordinary hills have cliff bands too, in patches. There is always a big mountain north of the start.
- **Cities:** a grid of streets with a ring road, buildings with lit windows, parks and street lamps. Buildings are solid, and the grappling hook bites into them.
- **Roads:** every place is linked by road, routed around steep ground and water. Roads are cut into hillsides, banked up across dips and carried over water on causeways, with berms, lamps and hedgerows along them. They are 15 blocks wide and quicker to drive. Narrow side trails break off to dead ends with a lost parcel at each.
- **Physics:** springy suspension, jumps, flips and spins, and tyres that slip: loose ground lets the tail step out, snow more so, and a road holds better. Go fast enough and the truck flattens trees and cacti and rolls over rocks; plough through them slowly, or one after another, and each costs a lot of speed and throws the truck about. Red mushrooms are trampolines.
- **Wings:** press B and the truck unfolds wings and flies as a glider, trading height for speed and back. Hands off, it settles into a long shallow glide; Shift is a push for climbing. Touching down folds the wings, and flying into a building or landmark folds them the hard way.
- **The sky:** floating islands you can land on and drive around, each with a crystal to collect; curving trails of rings that shove you forward; balloons to pop; thermals that lift you; blimps on slow circuits; and now and then a drone circling high up that fires a rocket at the ground, or at you.
- **Glitter bombs:** in flight, G drops one (three at a time, one back every five seconds). Where it lands is yassified for good: pink sparkling ground, flowers, blossom trees, pink buildings with every window lit. A thief caught in it twirls, sparkles and is out of the game. Hunter trucks go down to a single bomb anywhere within 20 blocks: wrecked on the spot and thrown into the air, pink.
- **Grow ops:** some regions hold a fenced compound of plastic tunnels and plant rows around a yard of water tanks, a trailer and a generator. The fence and the plants give way to a truck; the tunnels do not.
- **Animals:** herds of sheep and deer on the grass, deer in the forest, camels in the desert, goats in the highlands and canyons, cows in the alpine meadows, penguins on the snow. They graze, wander, and bolt from anything on wheels. Hit one and it is bowled over, gets up and runs.
- **On the water:** fishing boats, sailing boats and speedboats on the lakes and seas; out on deep water, pirate ships, submarines that surface and dive again, whales that come up to blow, and shark fins circling. Fly near a pirate ship and it fires broadsides at you. Nothing out there stops for a low-flying truck.
- **Lighthouses:** striped towers on rocks off the headlands, with a beam that sweeps round after dark.
- **Street racers:** packs of racing cars out on the roads all the time, each a different crowd: The Street Kings are quick, The Sunday Club and The Learner Drivers are not, and The Pub Crawl weave about, hiccup and spin out. They follow the road network from place to place and pick a new road at every junction. Pull up alongside a pack and press 3 to race them to a green finish beam about 900 m down the road.
- **Racetracks:** a circuit with kerbs, a gantry with start lights and a packed grandstand, and six drivers lapping it: an ace, a good driver, an average one, a poor one who runs wide, and two drunks. Press 3 there to line up on the grid for five laps. There is always a racetrack north-west of the start.
- **Parcel thieves:** yellow buggies that run when you get close. Touch one to catch it.
- **Hunter trucks:** black trucks that patrol and hunt by sight. Their red light shows from a long way off, and at night so do their headlights (and the thieves'). Break line of sight behind a hill, or creep through forest, and they lose you. They match your top speed, then tire to 95% after a long chase.
- **View distance:** a button on the start screen switches between Near (208 m), Far (320 m, the default) and Very far (416 m). The choice is remembered.
- **Grappling hook:** one throw every 15 seconds. Hit a thief to reel it in, or a hunter to stun it so you can ram it. Miss, and the hook bites into whatever it lands on and drags the truck to it.
- **Race mode:** one waypoint opens the same distance from you and a thief. First there scores, first to 5 wins.
- **Two players:** press "Play with a friend" on the start screen, then "Copy invite link" and send it. Only one of you makes the room; the other just opens the link. You then share one game: the same world (set by the room code), the same waypoint, one set of thieves and hunters that go for whichever of you is nearer, and finds and parcels that count for both. Herds, boats and lighthouses are in the same places for both of you, though each of you sees the animals move in your own way. Street racers, racetrack drivers and pirate cannon fire are each player's own. You see each other's trucks (theirs is blue), can bump and hook each other, and key 3 races your friend instead of the thief. A room keeps its own save.

## How two players connect

There is no game server. The two browsers find each other through the public PeerJS broker (`0.peerjs.com`) and then talk directly over WebRTC, using Google's public STUN server to get through home routers. That means each player's IP address is visible to the other player and to those two services, as with any peer-to-peer game. It works on most home networks; some strict office or mobile networks block it.

Progress saves in the browser's local storage. Add `?nosave` to the address to play without reading or writing the save.
