# Known issues

Problems in VikingColonies we know about, the worst first: what's being done, and a way round them where there is one.

_Last updated 20 October 2026._

VikingColonies 1.4.1 · Works with the current Valheim (checked 19 October 2026).

Is your problem not here? [Report it](https://github.com/DaAlmyte/VikingColonies-issues/issues/new/choose), or press
**Report a problem** in the Town Hall's window. Look at [Troubleshooting](Troubleshooting.md) first: it explains the
things that work that way on purpose.

- **A young colony can lose settlers to Necks and Greylings.** Settlers don't fight back yet: the one a monster is
  after runs from it, and in a colony with no walls or guards, a Neck that keeps hunting can catch them. **Way round:**
  build a Watchtower early (its guards deal with monsters in the colony), put up walls, or clear the Necks near the
  colony yourself. Settlers that stand up to weak animals are planned for 1.5.
- **Food put in after settlers went hungry is only eaten the next day.** A settler who finds nothing to eat at their
  meal goes hungry for the rest of the day, however much food arrives later (big stacks from stack-size mods are
  fine). **Way round:** keep food in a colony chest before the morning meal. Fixed for 1.4.2: a hungry settler looks
  for food again during the day.
- **Debug mode's K key, and the console's killall and killenemies, kill settlers too:** they treat settlers like
  monsters. **Way round:** don't use them near a colony. Fixed for 1.4.2: settlers are spared, as tamed animals are.
- **A settler may climb onto a hut's roof when its door is blocked** (rare): they try the blocked door from beside it
  and step up onto the low edge of the roof. **Way round:** keep huts' doors clear. Fixed for 1.4.2.

## Fixed in 1.4.1

- Settlers no longer hide from Necks again and again: only the settler one is after runs, and the rest work on.
- Settlers no longer bump into each other or into you: they pass through.
- Settlers' speech no longer shows at odd places on the screen when they are just out of view.
- A big boulder reaching into a hut's or the Town Hall camp's lot from beside it is now broken up, like one standing
  on it.
