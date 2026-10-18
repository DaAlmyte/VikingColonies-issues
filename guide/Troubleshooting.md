# Troubleshooting

- **Can't find the buildings in the hammer** — look in the **Misc** tab. The Town Hall needs a workbench nearby;
  the huts show while you stand within about 44 m of a Town Hall.
- **Hut says "Build near a Town Hall"** — it's more than 50 m from every Town Hall.
- **Nobody gets hired** — all citizens already have jobs, or auto-hire is off (Shift+E on the hut). More settlers
  come by themselves: build a Longhouse (free beds) and keep 5 food in the Town Hall's chest, and a newcomer arrives
  each day.
- **Lumberjack stands at the hut saying "No trees nearby"** — no tree within the hut's work area (40 m at level 1,
  10 m more per level) that his level's axe can fell: birch and oak need a level-2 hut. Trees that would fall on
  buildings are left alone.
- **The lumberjack doesn't replant** — put a Cultivator in the Lumberjack's Hut's storage (Shift+E on the hut shows
  whether replanting is on), and check the kind's Replant tick on its Trees list.
- **The lumberjack leaves a tree standing** — its kind is unticked from Fell on the hut's Trees list, its trunk stands
  within 3 m of something you built (`Lumberjack.LeaveTreesNearBuildings`), his axe can't fell it yet, or every way it
  could fall would hit a building.
- **Hand over says "Nothing to hand over"** — your bag holds none of what the order still needs, or the colony's
  chests already hold it (the builder takes from them), or the builder already carries it; "The chest is busy" — someone has it open, try again.
- **A hut is being taken down** — someone pressed Take down on its window (twice). Its building comes down piece by
  piece; its chest's contents end up in the Town Hall's chest (what doesn't fit there drops by the hut). Cancel take
  down on its window or in Work orders stops it.
- **The lumberjack says "Enough wood"** — the colony's chests hold the hut's "Stop at" amount of Wood; set it to "no
  limit" on the hut's window, or use some wood.
- **Settlers never sit down** — there's no seat or burning fire within 15 m of their hut (the Town Hall for the
  jobless): build a bench or a campfire there. A seat you stand or sit on is left to you, and in rain they only use
  seats and fires with a roof over them. With `Colony.FreeTime` off they always wait standing.
- **A settler stands on a bench** — he just got up from it the way a player does, and walks off it.
- **New settlers appear far off and walk in** — that's how newcomers come (0.16). With no way in they appear by the
  Town Hall. `Colony.NewcomersWalkIn` off makes them appear there always.
- **A settler wears rags, or leather** — clothes go with his trade; they're for looks only (no armour).
- **"Settlers can't come: the settler body didn't load"** — the mod couldn't make its settler body at start-up (often
  after a game update). Look at the start of the log (BepInEx/LogOutput.log) for the error and tell the mod's author;
  the colony and its buildings keep working.
- **No newcomers though there's a bed and food** — the colony may be unhappy: the Town Hall's Citizens tab says so.
  Choose a settler there to see his reasons (a home, meals of several kinds, an evening fire help).
- **A settler works slower** — hungry, or unhappy (his hover says which).
- **A settler takes a long way round to a hut's chest** — he goes in by that hut's own door (0.18); if it is shut in
  by other buildings, give it a clear way to its door.
- **Settlers stop work before dark** — that's the evening (0.70 of the day): they gather at the colony's fire, then go
  to bed. `Colony.EveningGathering` turns it off.
- **Settlers gather at the Town Hall in the evening** — no fire is burning in the colony: light a campfire or hearth
  near the Town Hall (and keep wood in a colony chest; settlers keep it fed).
- **The wood in the Town Hall goes down** — settlers feed the colony's fires with it (never the last 10).
  `Colony.TendFires` turns it off; or keep the wood in your own chest, or put Wood on the Town Hall's Keep in stock list.
- **A settler takes nothing from a chest that holds it** — that building keeps it (its Keep in stock tab, 0.21): other
  settlers leave kept items there. Lower the amount or take it off the list.
- **Things move between chests by themselves** — settlers with free time carry what a building keeps and lacks from
  chests that can spare it (0.21). The Town Hall keeps 10 food for newcomers to start. Turn it off with
  `Colony.CarryToStock`, or change the lists.
- **Settlers don't eat breakfast from the Town Hall** — its food is kept for newcomers (Food (any) × 10 to start):
  breakfast takes only food beyond that. Their daily meal still comes from it when there's no other food.
- **A settler sleeps beside his bed, not in it** — a player lies in it or has claimed it as a spawn point, or
  `Colony.SleepInBeds` is off.
- **Settlers say odd things above their heads** — that's small talk in their free time; turn it off with
  `Messages.SmallTalk` (your own setting). Needs ("Needs 12 Wood", "Hungry") always come first.
- **Settlers stand at the Town Hall saying "Fleeing"** — a monster that is alerted or hunting is (or was in the last
  15 seconds) within 20 m, and no colony hut with a finished building and a door is there to shelter in.
- **A settler says "Sleeping" or "Sheltering"** — it's night, a monster hunted him, or a raid is on at the colony; he
  comes out at dawn, 15 seconds after the last monster, or when the raid ends.
- **Settlers stand outside at night** — their hut isn't finished or has no door (they use the nearest finished hut
  with a door; with none, they stay out as before), or `Colony.SettlersGoIndoorsAtNight` is off.
- **A hut says "The Town Hall is gone: build a new one here within N days"** — its Town Hall was removed or broken.
  Build a new Town Hall among the colony's huts before the days run out and it takes the colony over.
- **A cairn on the map that you can't find** — it floats if he died in water, and it's gone once someone emptied it
  (remove the pin by hand then).
- **A settler hops or steps aside now and then** — something the game's paths don't know about stopped his walk (a
  log, a step, another settler); that's how he gets going again. If he keeps hopping at the same place, something
  blocks his way for good: clear it, or build a door or a ramp.
- **Settlers wait beside a door** (or a few steps back from a gate) — another settler is going through it; one at a
  time.
- **The farmer says "Needs a field"** — a Farm works only the fields you mark (0.20.1): put a field marker (hammer,
  Misc tab) near it. If the marker says "No Farm", see "A field nobody works" below.
- **The farmer waits by the Farm saying "Needs seeds" or "Needs Cultivator"** — put a Cultivator and seeds for a
  ticked crop that grows there (carrot, turnip or onion seeds, barley, flax) in the Farm's chest. "Crops growing" means
  every plot is planted: he waits for the harvest. A seed crop (carrot seeds) is only sown while fewer than 6 of its
  seeds are stored.
- **A field nobody works** — its window says "No Farm": every Farm works all the fields it has room for (one per
  level). Upgrade a Farm or build another, or take a field from a Farm in its Fields tab. A field outside every
  colony's area joins none: move its marker inside.
- **A field's crop isn't planted** — its seed isn't in the Farm's chest, or it doesn't grow there (its window greys it
  in the crop list). "Needs seeds" above the farmer's head says so when he has nothing else to do.
- **A worker stays inside his hut** — fixed in 0.20 for huts turned off the compass; one still wedged inside is moved to
  just inside the door after half a minute. Recall on the hut's window brings him out at once.
- **The farmer leaves a plot empty** — something stopped a plant growing there (cold, no room, a roof, the wrong
  biome); he rests that plot for a while and plants elsewhere.
- **The forager doesn't pick flint or branches** — they're unticked to start: tick them in the hut's What to pick list.
- **The farmer doesn't plant berry bushes or mushrooms (PlantEverything)** — they're unticked to start: tick them on
  the Farm's What to grow list, and put their price in the Farm's chest (the list says it: "seed: 5 Raspberries").
  A bush he planted stays on its plot for good; take it away with the hammer to grow crops there again.
- **A hut shows as "repair" in the Town Hall's Work orders** — pieces of it were broken; the builder puts them back
  when he has the materials. Press **Leave as it is** if you want them gone. A piece you remove with your hammer is
  never put back.
- **The builder walks around mending things** — he has nothing to build and mends damaged colony pieces for free.
- **The lumberjack says "Can't reach the hut"** — he can't walk to within 8 m of it (a closed door, stairs he can't
  use, a platform). Make a way in or move the hut.
- **A settler says "Dazed (something went wrong; starting over)"** — his job hit an error; he pauses and starts over
  by himself. If it keeps happening, the BepInEx log has a line "… had an error in his work" once a minute: please
  report it with that line.
- **Console doesn't open** — add `-console` to the game's launch options (r2modman: Settings → Set launch parameters).
- **A new hut doesn't hire** — its building isn't finished. Build a Builder's Hut and give the builder wood, stone, a
  flint axe, an antler pickaxe and a hoe (see [Getting started](Getting-Started.md)), or use `vc_build finish` in a
  test world.
- **`vc_blueprint save` says it's not allowed** — it's a design tool for test worlds: turn on `devcommands` first.
- **The builder says "Something's in the way: …"** — a piece of his plan would go into another building (yours or
  another hut's). Move that, or let the hut count as built with `vc_build done` (test worlds); `vc_build clear` removes
  the pieces he already put up for it.
- **The builder says "Needs …"** — put that in his hut's (or any colony) storage; he looks again every few seconds.
- **The builder says "Can't place: no support for …"** — the blueprint has a piece nothing holds up; add a beam or
  a post to your design (`vc_blueprint save` lists pieces that barely hold).

- **The outline is red** — the line under the crosshair says why. Move or turn the hut, lower it, or remove what's in
  the way.
- **The builder says "Needs an axe" (or a pickaxe, a hoe, stone)** — put one in his hut's or any colony storage. The
  tool stays there; he works with a copy.
- **The builder says "Something's in the way: a tree"** (or a rock …) — he couldn't reach it, or couldn't fell it
  without hitting a building. Remove it yourself; he looks again within a minute (or, if he has gone to another site
  meanwhile, when he comes back). `vc_build ready` (test worlds)
  skips the rest of the clearing and flattening.
- **The builder says "Needs Builder's Hut level 2 for a tree — or clear it yourself"** — his level's tools can't fell
  it (birch and oak need a bronze axe; a level-1 builder may use only a flint axe). Fell it yourself, or upgrade the
  Builder's Hut and put a bronze or iron axe in a chest. Meanwhile he works on other huts.
- **The builder left a hut half-done and works on another** — that hut waits on you (its window says what it needs or
  what is in the way). He comes back after five minutes, once he is free or his other site waits on you too.
- **The raise and lower keys clash with another mod** — change `Placing.RaiseKey` and `Placing.LowerKey`.
- **A settler stands at a door and doesn't go through** — the door is outside the colony's area, needs a key, or is under
  a ward of someone other than the colony's owner (add the owner to the ward). Settlers only open doors the colony's
  owner may open.
- **The upgrade button says it needs a higher Builder's Hut** — upgrade the Builder's Hut first; its builder may raise
  his own hut one level above itself.
- **An upgrade waits with "Needs: …"** — the new design's materials aren't in the colony's chests yet (for example
  iron for level 2). Put them in any colony chest.
- **A settler shows as *Missing* in the Town Hall** — nobody saw him where he was last, though that area is loaded:
  his body is lost (another mod removed it, or a bug). Choose him on the Citizens tab and press **Bring back**: he
  comes back to the Town Hall as himself (same name, looks, job, home and skills), empty-handed. If his body is still
  somewhere in the world it says so instead; go near him and use Recall.
- **The log starts with "Game check: … is missing"** — a Valheim update renamed something the mod reads; the line says
  what stops working until the mod is updated. Everything else keeps working.

## Other mods
- Tested together with PlantEverything, PlantEasily, Seasonality, PlanBuild, EpicLoot and Monstrum (with Warfare)
  (2026-10-15): the whole self-test passes with them installed, no errors, no clashing patches.
- Trees and bushes another mod makes plantable (PlantEverything) are cleared from a building site like wild plants;
  the ones you planted yourself are left alone, and a hut's outline turns red over them.
- Crops a mod adds to the Cultivator show up on a Farm's What to grow list; plants another mod adds for picking show
  up on a Forager's Hut's list. Long lists turn pages.

## Removing the mod
- Without VikingColonies the game can't show what only the mod has: the Town Hall's and the huts' chests (with what's
  in them), the settlers and their cairns disappear from the world while it's gone, and come back when you install
  it again. The pieces the builder put up are the game's own and stay as ordinary buildings.
- On a server, everyone needs the same version: don't remove it while players use a colony.

## Reporting a bug
Stand near the settler or building with the trouble, open the console (F5; it needs the `-console` launch option,
see above) and type `vc_bugreport` (no cheats needed): it writes `BepInEx/VikingColonies-bugreport.txt` — the mod's
and the game's versions, your other mods, the colonies around you (only what your game has loaded: their buildings and
orders, each settler's state, what he did lately and anything that went wrong for him), and the mod's last warnings
and errors. On a server, the player near the settler (or the host) is the one to type it. Send that file with
`BepInEx/LogOutput.log` from your mod manager profile and describe what you did. The log stays small by default
(start-up, deaths, the colony's saga, warnings and errors); for a bug report turn on `Developer.VerboseLog` (see
[Settings](Settings.md)) and play until it happens again, so every settler's step is in it.
