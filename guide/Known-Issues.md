# Known issues

Problems in VikingColonies we know about, the worst first: what's being done, and a way round them where there is one.

_Last updated 4 November 2026._

VikingColonies 1.6.1 · Works with Valheim 1.0.21 (checked 30 October 2026).

Is your problem not here? [Report it](https://github.com/DaAlmyte/VikingColonies-issues/issues/new/choose), or press **Report a problem** in the Chieftain's Camp's window. Look at [Troubleshooting](Troubleshooting.md) first: it explains the things that work that way on purpose.

- **A Troll can catch a settler.** Now and then a settler running from a Troll to their hut is caught at its door.
  Being worked on. (Since 1.5.1 the brave run from a Troll at 12 m like everyone, and a settler sheltering stays in
  until hurt to half.)
- **Settlers left behind when you move your Chieftain's Camp stay where they were.** Once the old one is gone, its
  colony lives on for 3 in-game days; then its settlers have no colony, and only a camp whose area they stand in takes
  them in, so one built far away never does. They stay, hungry, and there's no way yet to send a settler away. Fixed in
  1.7.0 (due Sunday 8 November): settlers left behind will walk to your new camp, and you'll be able to send one away. **Way round until
  then:** none that moves them; setting `Messages.WordsAboveHeads` off quiets what they say above their heads.
- **A settler can take a long way round a hut just after its door was used.** For a few seconds after a door
  opens or shuts, the game works out the paths round that hut again, and a settler setting off just then can
  loop several metres out before coming back to where they were going. They still get there. Being worked on:
  planned for 1.7.1.
- **Hugin the raven can stand in a settler's way by a door.** When you stand near a hut's door while Hugin brings a
  tip, he lands by you, and a settler walking in or out can stop against him for a while. Being worked on: Hugin will
  keep out of settlers' way. **Way round until then:** step away from the door, or turn `Messages.HuginTips` off once
  you know the colony.
- **The Farm's own beehive at levels 4 and 5 makes no honey.** It stands too far under the roof for the bees ("bees
  need more space"). The Forager's Hut's beehive and the Farm's at level 3 work. Fixed in 1.7.0 (due Sunday 8 November): the
  hive moves out from under the roof, and a Farm you already have moves its own hive when the world loads. **Way round
  until then:** a beehive of your own placed in the open works as usual.
- **Now and then a worker can't find the way to their hut's door and stays outside at night.** At some spots the
  ground just outside a hut's door isn't on the game's walking map, so a worker (often the lumberjack) can't get in
  and spends the night outside. Being worked on.

## Recently fixed

- **If every settler dies before the first Longhouse stands, no new ones come**: fixed in 1.6.1: update the mod. The
  morning after, new settlers walk in to start again.
- **A ring of campfires can build up round the Chieftain's Camp**: fixed in 1.6.1: update the mod. The extra fires
  are taken down by themselves.
- **With a terrain mod like Tunnelheim, levelled ground can say "A rock nothing can break"**: fixed in 1.6.1: update
  the mod. Such ground counts as ground, and the builder pays stone only for ground that rises.
- **Guards kill an animal you're taming inside the colony**: fixed in 1.6.1: update the mod. An animal you're taming
  is left alone until it bites someone.
- **A hut built from your own design can leave a few pieces out**: fixed in 1.6.1: update the mod. The builder puts
  a piece up only after what holds it.
- **Settlers running from monsters can all head for the same hut**: fixed in 1.6.1: update the mod. They spread over
  the colony's huts.
- **On a colony's first day, every settler talks about the same newcomer**: fixed in 1.6.1: update the mod.
- **At breakfast, settlers crowd together at the chest**: fixed in 1.6.1: update the mod. Each takes a place of their
  own by the chest.
- **A hut you've just placed can be broken by an animal before its builder starts**: fixed in 1.6.1: update the mod.
- **The Town Hall and the huts were in the hammer's Furniture tab, not Misc**: fixed in 1.5.1: update the mod. The
  colony's buildings, now with the Chieftain's Camp (the Town Hall's new name), are in the Misc tab.
- **A settler sitting on a bench or lying in a bed that the builder takes down could sink under the ground**: fixed
  in 1.5.1: update the mod. A settler who sank before the update walks again once you leave the area and come back.
- **A builder can take another hut's materials from its chest**: fixed in 1.5.1: update the mod. What a hut's own
  build still needs stays in its chest for that build's builder.
- **With StarLevelSystem, settlers with stars can get too big for doors**: fixed in 1.5.1: update the mod. Settlers
  keep their own size whatever another mod sets (their stars and the health that comes with them stay).
- **The builder sometimes walks round the outside of a hut to reach its chest**: fixed in 1.5.1: update the mod. The
  builder walks straight to the chest's open side.
- **A young colony could lose settlers to Necks and Greylings**: fixed in 1.5.0: update the mod. Settlers now stand up
  to weak animals: a Neck, a Greyling or a Boar that goes for a settler is fought off with what's in their hands.
- **MyLittleUI: the Town Hall's hover says Rename, and Shift+E doesn't open its window**: fixed in 1.4.2: update the mod. ([#1](https://github.com/DaAlmyte/VikingColonies-issues/issues/1))
- **Guards may not gather when you sound the alarm from inside the Town Hall**: fixed in 1.4.3: update the
  mod. Each guard now takes the nearest open spot round the alarm that they can walk to.
- **Food put in after settlers went hungry was only eaten the next day**: fixed in 1.4.2: update the mod. A hungry
  settler now looks for food again every half minute.
- **Debug mode's K key, and the console's killall, killenemies and killtame, killed settlers too**: fixed in 1.4.2:
  update the mod.
- **A settler could climb onto a hut's roof when its door was blocked**: fixed in 1.4.2: update the mod.

## Fixed in 1.4.1

- Settlers no longer hide from Necks again and again: only the settler one is after runs, and the rest work on.
- Settlers no longer bump into each other or into you: they pass through.
- Settlers' speech no longer shows at odd places on the screen when they are just out of view.
- A big boulder reaching into a hut's or the Town Hall camp's lot from beside it is now broken up, like one standing
  on it.
