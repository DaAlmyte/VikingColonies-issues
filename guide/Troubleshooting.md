# Troubleshooting

## Huts and placing them

- **Can't find the buildings in the hammer**: look in the **Misc** tab. The camp needs a workbench nearby, and the
  huts show only while you stand within about 44 m of a Chieftain's Camp.
- **Hut says "Build near a Chieftain's Camp"**: the hut is more than 50 m from every Chieftain's Camp.
- **The outline is red**: the line under the crosshair says why. Move or turn the hut, lower it, or remove what's in
  the way.
- **The raise and lower keys clash with another mod**: change `Placing.RaiseKey` and `Placing.LowerKey`.
- **The camp or a hut went up into the side of a big rock**: the builder breaks up rocks standing on the building's
  lot, but not yet a big boulder whose middle lies beside it with only its side reaching in (1.4.0). Leave a few
  metres between the camp or a hut and big boulders, or break the rock back yourself with a pickaxe.
- **A hut is being taken down**: someone pressed Take down on its window (twice). The building comes down piece by
  piece, and the contents of its chest end up in the camp's chest; whatever doesn't fit there drops by the hut. To
  stop it, use Cancel take down on its window or in Work orders.
- **A hut shows as "repair" in the camp's Work orders**: pieces of it were broken, and the builder puts them back when
  they have the materials. Press **Leave as it is** if you want them gone. A piece you remove with your hammer is
  never put back.
- **A new hut doesn't hire**: its building isn't finished. Build a Builder's Hut and give the builder wood, stone, a
  flint axe, an antler pickaxe and a hoe (see [Getting started](Getting-Started.md)), or use `vc_build finish` in a
  test world.
- **The upgrade button says it needs a higher Builder's Hut**: upgrade the Builder's Hut first. Its builder may raise
  their own hut one level above itself.
- **An upgrade waits with "Needs: …"**: the new design's materials aren't in the colony's chests yet (iron for level
  2, for example). Put them in any colony chest.
- **A hut says "The Chieftain's Camp is gone: raise a new one here within N days"**: its camp was removed or broken.
  Raise a new camp among the colony's huts before the days run out, and it takes the colony over.

## Settlers and newcomers

- **Nobody gets hired**: either every citizen already has a job or auto-hire is off (Shift+E on the hut). More
  settlers come by themselves if you build a Longhouse (free beds) and keep 5 food in the camp's chest. A newcomer
  then arrives each day.
- **No newcomers though there's a bed and food**: the colony may be unhappy, and the camp's Overview says so. Choose a
  settler there to see their reasons. A home, meals of several kinds and an evening fire help.
- **New settlers appear far off and walk in**: that's how newcomers come (0.16). When there's no way in, they appear by
  the Chieftain's Camp. With `Colony.NewcomersWalkIn` off they always appear there.
- **"Settlers can't come: the settler body didn't load"**: the mod couldn't make its settler body at start-up, often
  after a game update. Look at the start of the log (BepInEx/LogOutput.log) for the error and tell the mod's author.
  The colony and its buildings keep working.
- **A settler works slower**: they're hungry or unhappy, and their hover says which.
- **A settler wears rags, or leather**: clothes go with their trade and are for looks only (no armour).
- **Settlers say odd things above their heads**: that's small talk in their free time. Turn it off with
  `Messages.SmallTalk` (your own setting). Needs ("Needs 12 Wood", "Hungry") always come first.
- **A settler says "Dazed (something went wrong; starting over)"**: their job hit an error, so they pause and start
  over by themselves. If it keeps happening, the BepInEx log has a line "… had an error in their work" once a minute.
  Please report it with that line.
- **A worker stays inside their hut**: this was fixed in 0.20 for huts turned off the compass. One still wedged inside
  is moved to just inside the door after half a minute, and Recall on the hut's window brings them out at once.
- **A settler shows as *Missing* in the camp**: nobody saw them where they were last, though that area is loaded, so
  their body is lost (another mod removed it, or a bug). Choose them on the People tab and press **Bring back**, and
  they come back to the camp as themselves (same name, looks, job, home and skills), empty-handed. If their body is
  still somewhere in the world, the window says so instead. Go near them and use Recall.
- **A cairn on the map that you can't find**: it floats if they died in water, and it's gone once someone emptied it.
  Remove the pin by hand then.

## Free time, food and sleep

- **Settlers never sit down**: there's no seat or burning fire within 15 m of their hut (for the jobless, the camp), so
  build a bench or a campfire there. They leave alone a seat you stand or sit on, and in rain they only use seats and
  fires with a roof over them. With `Colony.FreeTime` off they always wait standing.
- **A settler stands on a bench**: they just got up from it the way a player does, and they walk off it.
- **Settlers stop work before dark**: that's the evening (0.70 of the day). They gather at the colony's fire, then go
  to bed. `Colony.EveningGathering` turns it off.
- **Settlers gather at the camp in the evening**: no fire is burning in the colony. The camp's fire (1.4) burns once
  it's built and there's wood in a colony chest, and settlers keep it fed. Without a camp yet, light a campfire or
  hearth near the camp.
- **The wood in the camp goes down**: settlers feed the colony's fires with it, never taking the last 10, and a fire
  they keep burning says so when you look at it. `Colony.TendFires` turns it off. You can also keep the wood in your
  own chest or put Wood on the camp's Keep in stock list.
- **Settlers don't eat breakfast from the camp**: the camp's food is kept for newcomers (Food (any) × 10 to start; the
  camp's window says how much it keeps), so breakfast takes only food beyond that. Their daily meal still comes from
  it when there's no other food.
- **A settler sleeps beside their bed, not in it**: either a player lies in it, or `Colony.SleepInBeds` is off.
- **A Longhouse has fewer beds for settlers than it shows**: a player claimed one as a spawn point, and it's theirs now.
  Take it down with the hammer and the builder puts up a new one for the settlers.
- **A settler says "Sleeping", "Resting" or "Sheltering"**: it's night, a monster hunted them, or a raid is on at the colony. They
  come out at dawn, 15 seconds after the last monster, or when the raid ends.
- **Settlers stand outside at night**: either their hut isn't finished or has no door (they use the nearest finished
  hut with a door; with none, they stay out as before), or `Colony.SettlersGoIndoorsAtNight` is off.
- **Settlers stand at the camp saying "Fleeing"**: a monster that is alerted or hunting is within 20 m (or was in the
  last 15 seconds), and no colony hut with a finished building and a door is there to shelter in.

## Chests and stock

- **A settler takes nothing from a chest that holds it**: that building keeps it (its Keep in stock tab, 0.21), so
  other settlers leave kept items there. A builder who needs it says where it's kept ("more Wood is kept in the
  Lumberjack's Hut"). Lower the amount or take it off the list.
- **Things move between chests by themselves**: settlers with free time carry what a building keeps and lacks from
  chests that can spare it (0.21). The camp keeps 10 food for newcomers to start. Turn it off with
  `Colony.CarryToStock`, or change the lists.
- **A settler takes a long way round to a hut's chest**: they go in by that hut's own door (0.18). If other buildings
  shut it in, give it a clear way to its door.

## Getting stuck

- **A settler hops or steps aside now and then**: something the game's paths don't know about stopped their walk (a
  log, a step, another settler), and the hop gets them going again. If they keep hopping at the same place, something
  blocks their way for good. Clear it, or build a door or a ramp.
- **Settlers wait beside a door** (or a few steps back from a gate): another settler is going through, one at a time.
- **A settler stands at a door and doesn't go through**: the door is outside the colony's area, needs a key, or is
  under a ward of someone other than the colony's owner (add the owner to the ward). Settlers only open doors the
  colony's owner may open.

## Lumberjack

- **Lumberjack stands at the hut saying "No trees nearby"**: no tree within the hut's work area (40 m at level 1, 10 m
  more per level) is one their level's axe can fell. Birch and oak need a level-2 hut. Trees that would fall on
  buildings are left alone.
- **The lumberjack doesn't replant**: put a Cultivator in the Lumberjack's Hut's storage (Shift+E on the hut shows
  whether replanting is on), and check the kind's Replant tick on its Trees list.
- **The lumberjack leaves a tree standing**: one of four things is going on. The kind is unticked from Fell on the
  hut's Trees list, the trunk stands within 3 m of something you built (`Lumberjack.LeaveTreesNearBuildings`), their
  axe can't fell it yet, or every way it could fall would hit a building.
- **The lumberjack says "Enough wood"**: the colony's chests already hold the hut's "Stop at" amount of Wood. Set it to
  "no limit" on the hut's window, or use some wood.
- **The lumberjack says "Can't reach the hut"**: they can't walk to within 8 m of it (a closed door, stairs they can't
  use, a platform). Make a way in or move the hut.

## Farmer and forager

- **The farmer says "Needs a field"**: a Farm works only the fields you mark (0.20.1), so put a field marker (hammer,
  Misc tab) near it. If the marker says "No Farm", see "A field nobody works" below.
- **The farmer waits by the Farm saying "Needs seeds" or "Needs Cultivator"**: put a Cultivator and seeds for a ticked
  crop that grows there (carrot, turnip or onion seeds, barley, flax) in the Farm's chest. "Crops growing" means every
  plot is planted, and the farmer waits for the harvest. A seed crop (carrot seeds) is only sown while fewer than 6 of
  its seeds are stored.
- **A field nobody works**: its window says "No Farm". Every Farm works all the fields it has room for (one per
  level), so upgrade a Farm or build another, or take a field from a Farm in its Fields tab. A field outside every
  colony's area joins none; move its marker inside.
- **A field's crop isn't planted**: its seed isn't in the Farm's chest, or it doesn't grow there (its window greys it
  in the crop list). "Needs seeds" above the farmer's head says so when they have nothing else to do.
- **The farmer leaves a plot empty**: something stopped a plant growing there (cold, no room, a roof, the wrong
  biome). They rest that plot for a while and plant elsewhere.
- **The farmer doesn't plant berry bushes or mushrooms (PlantEverything)**: they're unticked to start. Tick them on the
  Farm's What to grow list, and put their price in the Farm's chest (the list says it: "seed: 5 Raspberries"). A bush
  the farmer planted stays on its plot for good; take it away with the hammer to grow crops there again.
- **The forager doesn't pick flint or branches**: they're unticked to start, so tick them in the hut's What to pick
  list.

## Builder

- **Hand over says "Nothing to hand over"**: your bag holds none of what the order still needs, the colony's chests
  already hold it (the builder takes from them), or the builder already carries it. "The chest is busy" is a different
  message: someone has the chest open, so try again.
- **The builder walks around mending things**: they have nothing to build, so they mend damaged colony pieces for free.
- **The builder says "Something's in the way: …"**: a piece of their plan would go into another building, yours or
  another hut's. Move that, or let the hut count as built with `vc_build done` (test worlds). `vc_build clear` removes
  the pieces they already put up for it.
- **The builder says "Something's in the way: a tree"** (or a rock …): they couldn't reach it, or couldn't fell it
  without hitting a building. Remove it yourself. They look again within a minute, or when they come back if they've
  gone to another site meanwhile. `vc_build ready` (test worlds) skips the rest of the clearing and flattening.
- **The builder says "Needs …"**: put that in their hut's storage or any colony storage. They look again every few
  seconds.
- **The builder says "Needs an axe" (or a pickaxe, a hoe, stone)**: put one in their hut's or any colony storage. The
  tool stays there and they work with a copy.
- **The builder says "Needs Builder's Hut level 2 for a tree" (with "or clear it yourself" after it)**: their level's tools can't
  fell it. Birch and oak need a bronze axe, and a level-1 builder may use only a flint axe. Fell it yourself, or
  upgrade the Builder's Hut and put a bronze or iron axe in a chest. Meanwhile they work on other huts.
- **The builder says "Can't place: no support for …"**: the blueprint has a piece nothing holds up. Add a beam or a
  post to your design (`vc_blueprint save` lists pieces that barely hold).
- **The builder left a hut half-done and works on another**: that hut waits on you, and its window says what it needs
  or what is in the way. They come back after five minutes, once they are free or their other site waits on you too.
- **`vc_blueprint save` says it's not allowed**: it's a design tool for test worlds (a world whose name starts with
  `VCTest`). Turn on `devcommands` first.

## Game and console

- **Console doesn't open**: add `-console` to the game's launch options (r2modman: Settings → Set launch parameters).
- **The log starts with "Game check: … is missing"**: a Valheim update renamed something the mod reads. The line says
  what stops working until the mod is updated. Everything else keeps working.

## Other mods
- Tested together with PlantEverything, PlantEasily, Seasonality, PlanBuild, EpicLoot and Monstrum (with Warfare)
  (2026-10-15). The whole self-test passes with them installed, with no errors and no clashing patches.
- Tested again for 1.4.3 (2026-10-21) with those, MyLittleUI 1.2.31, CraftFromContainers 4.0.70, Quick Stack - Store -
  Sort - Trash - Restock 1.4.16, MultiUserChest 0.6.2, ExtraSlots 1.2.21 and Gizmo 1.16.0, all at once. No errors, no
  clashing patches. ValheimPlus 10.3.0 on its own, with its settings as it ships them, gave the same result.
- Tested again for 1.5.1 (2026-10-28) with all of those and WackysDatabase 2.6.10, 16 mods at once. No errors, no
  clashing patches. ValheimPlus 10.4.0 on its own, with its settings as it ships them, gave the same result.
- **MyLittleUI** (checked with 1.2.31, 1.4.2): Shift+E on the camp and the huts opens their window, and their hover
  says "Manage", not MyLittleUI's "Rename". Before 1.4.2 the chest's rename took over Shift+E (report #1). Before 1.4.3
  a fallen settler's cairn showed only "Cairn" on hover with it; now it says "Here lies …" first.
- Trees and bushes another mod makes plantable (PlantEverything) are cleared from a building site like wild plants. The
  ones you planted yourself are left alone, and a hut's outline turns red over them.
- Crops a mod adds to the Cultivator show up on a Farm's What to grow list, and plants another mod adds for picking
  show up on a Forager's Hut's list. Long lists turn pages.
- **StarLevelSystem** and other mods that give creatures stars: settlers may get stars too, and the health that comes
  with them, but since 1.5.1 they keep their own size so they fit through doors. Before 1.5.1 a starred settler grew
  10% a star and could get stuck outside a hut; replacing the door with a bigger one was the way round it.

## Can't join a server
- See [Multiplayer](Multiplayer.md), Joining. A join code only works while the server has crossplay on; without it,
  join by the server's address (Join IP).
- "Incompatible version" means a mod is missing or a version differs. Start the game from your mod manager, with the
  server's version of VikingColonies.

## Removing the mod
- Without VikingColonies the game can't show what only the mod has. The camp's and the huts' chests (with what's in
  them), the settlers and their cairns disappear from the world while it's gone, and they come back when you install
  it again. The pieces the builder put up are the game's own and stay as ordinary buildings.
- On a server, everyone needs the mod, with the same first two numbers of its version, so don't remove it while
  players use a colony.

## Telling us what you think
Press **Feedback** in the camp's window (beside Report a problem). It opens a small window with two buttons. **Tell us
on Discord** opens our Discord server (post in #feedback), and **Write it on GitHub** opens the feedback form with the
versions filled in. Nothing is sent from the game: you write it and press send yourself. What you like, what felt like
a chore and what broke all help. The same window comes by itself once, at a good moment; `Messages.AskForFeedback`
turns that off.

## Reporting a bug
The quickest way is to press **Report a problem** in the camp's window (beside Close). A small window opens and writes
the report below, and it says where the file is saved: `VikingColonies-bugreport.txt`, with `LogOutput.log` beside it.
The start of the folder, your Windows account's own folder, shows as `%USERPROFILE%`, which also works typed into File
Explorer's address bar. **Show the file** under it opens the folder with the file picked out, ready to drag into
your post or the form. Then pick a way to send it (since 1.6):
- **Bug form on GitHub** copies the report and opens the bug form with the versions and the report's first lines
  filled in. Click the form's last box, paste (Ctrl+V), say what happened, and press Submit.
- **Ask on Discord** copies the report and opens our Discord. Start a post in #bug-reports, say what happened, and
  paste (Ctrl+V; Discord turns a long paste into a file), or drag the file in. You don't need a GitHub account.
What the button did shows under them in the window, which stays open.

Nothing is sent from the game. You see everything first and post it yourself (folder names that could hold your
Windows account's name are shortened in the report). The report covers the colony around the Chieftain's Camp; for
trouble elsewhere, use the console as below and type `vc_bugreport form` (straight to the bug form).

Stand near the settler or building with the trouble and open the console (F5; it needs the `-console` launch option,
see "Console doesn't open" above). Type `vc_bugreport` (no cheats needed) and it writes
`BepInEx/VikingColonies-bugreport.txt`. That file has the mod's and the game's versions, your other mods, the colonies
around you (only what your game has loaded: their buildings and orders, each settler's state, what they did lately and
anything that went wrong for them), and the mod's last warnings and errors. On a server, the player near the settler
(or the host) is the one to type it. Send that file with `BepInEx/LogOutput.log` from your mod manager profile and
describe what you did. The game writes your Steam ID into that log, so you can delete it before sending. The log stays
small by default (start-up, deaths, the colony's saga, warnings and errors). For a bug report, turn on
`Developer.VerboseLog` (see [Settings](Settings.md)) and play until it happens again, so every settler's step is in it.
