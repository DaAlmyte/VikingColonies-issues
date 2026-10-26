# Known issues

Problems in VikingColonies we know about, the worst first: what's being done, and a way round them where there is one.

_Last updated 26 October 2026._

VikingColonies 1.5.0 · Works with Valheim 1.0.20 (checked 25 October 2026).

Is your problem not here? [Report it](https://github.com/DaAlmyte/VikingColonies-issues/issues/new/choose), or press **Report a problem** in the Town Hall's window. Look at [Troubleshooting](Troubleshooting.md) first: it explains the things that work that way on purpose.

- **The Town Hall and the huts are in the hammer's Furniture tab, not Misc.** Valheim 1.0's build menu files them
  with the chests, so they don't show where this guide says. Fixed in 1.5.1: they're in the Misc tab. **Way round
  until then:** look in the **Furniture** tab (with a workbench near for the Town Hall; inside a colony's area for the
  huts).
- **With StarLevelSystem, settlers with stars can get too big for doors.** That mod makes some settlers bigger along
  with their stars, and they get stuck outside their hut. Fixed in 1.5.1: settlers keep their own size whatever
  another mod sets (their stars and the health that comes with them stay). **Way round until then:** give the hut a
  bigger door.
- **The builder sometimes walks round the outside of a hut to reach its chest.** When the chest stands against the
  back wall, the builder can head for the outside of that wall first, then go round to the door, and the same can
  happen at the Town Hall camp's chest. The work still gets done, only slower. Fixed in 1.5.1: the builder walks
  straight to the chest's open side.

## Recently fixed

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
