# Buildings

## Town Hall
- Cost: 20 Wood, 10 Stone (settings `Town Hall.WoodCost`, `Town Hall.StoneCost`). Needs a workbench nearby.
- Founds a colony. On first build it adopts nearby citizens without a colony, then tops up to the starting citizen
  count (4 by default). Later, any citizen without a colony who comes inside its area joins too.
- **E**: 24-slot colony chest; keep food here for newcomers (settlers eat from any colony chest). It keeps 10 food of
  any kind for them to start (its [Keep in stock](#keep-in-stock) list): settlers eat food beyond that first.
- **Shift+E**: the colony's window, in four tabs.
  - **Citizens**: the colony at a glance (beds taken, food in this chest, how many are hungry, what the next newcomer
    waits for), then every citizen (name, job, status, workplace), ten a page. Citizens nobody is near show their last
    known status; vanished citizens show as *Missing* and drop off after 3 in-game days. Click a citizen to choose
    him, then **Recall** brings him at once to a free spot by the Town Hall, wherever he is in the loaded world (stuck
    somewhere, or just far off); he carries on with his work from there. Only players who may manage the colony (its
    owner, or players on a ward covering it) can recall. A settler marked *Missing* (his body is lost) gets **Bring
    back** instead: the Town Hall keeps what it needs of every member (name, looks, job, home, skills) and brings him
    back as himself, empty-handed, if his body isn't anywhere in the world. The window tells how it went: back, back but gone indoors
    again (night or a raid), or why not (no free spot by the Town Hall, not your colony).
  - **Saga**: what happened in the colony, newest first, twelve lines a page: who came to live here, who died and
    how, which huts were built or went up a level, who started or left work where, and who was called back or got
    boxed in and was moved out. The last 60 lines are kept with the Town Hall.
  - **Work orders**: every building, upgrade and repair the colony has ordered and not finished, in the order
    builders take them, eight a page: the hut, what it becomes ("new", "level 2" or "repair"), pieces up of all, and how it stands (who is building it, what it
    needs, waiting for a builder, set aside). At the top, what all open orders still need that the colony's chests
    don't hold and the builders don't already carry ("Still to bring: 15 Wood, 12 Stone"), with **Hand over** beside it
    (0.23): what the chosen order (or the first) still needs beyond the colony's chests and its builder's load goes from
    your bag into the Town Hall's chest ("Handed over 12 Wood, 4 Stone"); when the Town Hall keeps one of those items in
    stock, its own amount is topped up first, so the builder can still take what's short (0.26). Click an order to see its full description, then:
    - **Do first**: builders take it before everything else, even their own hut; a builder busy elsewhere comes over
      within seconds. If it waits on you (materials, a tool, a higher Builder's Hut), he still sets it aside after a
      minute and works on something else; press Do first again once you've helped.
    - **Set aside**: no builder takes it until you press **Resume** (a builder on it leaves it at once). Handy for an
      order you can't supply yet.
    - **Cancel upgrade**: as in the hut's window, only before the builder has changed anything.
    - **Leave as it is** (in its place for a repair): the missing pieces aren't put back, and aren't asked for again.
  - **Keep in stock** (0.21): what its chest keeps, as on every hut (below). To start, Food (any) × 10, for newcomers.
- Its colony area is a 50 m circle (setting `Colony.ColonyRadius`). Job huts can only be built inside it.
- Colony buildings aren't destroyed by falling trees or rolling logs; monsters can still damage them.
- **Only players can damage the Town Hall chest**: monsters, raids, fire and stray rocks can't break it. You can still
  remove it with the hammer; the Ashlands' heat and lava, the Deep North's cold and a collapse (no support) can still
  destroy it, like any building.
- **If it's lost anyway**, the colony lives on for 3 in-game days (setting `Colony.TownHallGraceDays`, 0–10): its
  settlers keep their jobs and its huts keep working, and the huts say "The Town Hall is gone: build a new one here
  within N days to keep the colony". A new Town Hall built among them in that time takes the colony over — the same
  settlers, huts and orders, and no newcomers. After that, settlers lose their colony and job as before, and the next
  Town Hall founds a new colony. With `TownHallGraceDays = 0` a colony ends 30 seconds after its Town Hall is gone.

## Lumberjack's Hut
- Cost: 20 Wood (setting `Lumberjack Hut.WoodCost`). Needs a Town Hall nearby instead of a workbench: it only shows
  in the hammer while you stand well inside a Town Hall's colony area (within about 44 m), so the hut lands inside it. A hut outside every colony (its Town Hall was
  destroyed) says "Build near a Town Hall" and joins as soon as a Town Hall is in range.
- **E**: 18-slot storage where the lumberjack delivers wood and seeds and fetches seeds for replanting.
- Put a **Cultivator** in its storage to let the lumberjack replant (he doesn't use it up). The hut window shows
  "Fells 5 of 6 kinds, replants 3 · Replanting: on" ("needs a Cultivator in storage", "off (setting)").
- **Trees…** (0.22, in place of the replanting list; MineColonies' Saplings tab): a line per tree kind (Beech, Birch,
  Fir, Pine, Oak, Ancient tree…, and a mod's trees by name) with two ticks. **Fell**: he cuts that kind down (ticked
  for every kind his axe allows; untick one and he leaves those trees standing). **Replant**: where he fells a tree he
  plants the ticked kinds' saplings in turn (greyed for a kind with no sapling, that doesn't grow there, or whose
  grown tree needs a better axe: "replanting needs a level 3 hut"). Your
  replanting choices from before 0.22 are the Replant ticks.
- **Stop at** (0.22): "no limit", 200, 500 or 1000 Wood — with that much Wood in the colony's chests he rests
  ("Enough wood") and starts again below it.
- **Shift+E**: the worker (name and status), **Hire**, **Fire**, **Auto-hire** (on by default — a hut without a
  worker hires a jobless citizen by itself). Firing switches auto-hire off so the same citizen isn't re-hired at once.
- Destroying the hut makes its worker jobless (after about 30 seconds — a building has to be missing that long to
  count as gone, so one that is still loading isn't mistaken for a destroyed one).
- **Take down** (0.23, any finished hut's window; click twice, "Sure? Take it down"): a builder takes its building down
  from the top (with any leftovers of an older level), as he takes old pieces away in an upgrade, and the materials go
  to his hut; he clears nothing round it first. It is ordered only when all of the hut is loaded ("Come closer…"), so
  no piece stays standing out of reach (0.26). When the last piece is down, what still lies of its materials on the
  hut's own ground goes to the Town Hall's chest (a pile of yours beside it stays), and the hut's chest goes too: its contents into the Town Hall's chest (what doesn't fit drops by the hut), its worker is
  let go, and the saga says "the Forager's Hut was taken down". The window says "Being taken down (12 of 30 pieces
  left)"; Work orders shows it as "take down". Only for players who may manage the colony; never the Town Hall.
  **Cancel take down** (on its window or Work orders) stops it, and what came down is put back as a repair. While it
  is taken down it can't be upgraded.
- A new hut only hires once the builder has finished its building; huts from before 0.3.0 keep working and have a
  **Build** button.

## Builder's Hut
- Cost: 20 Wood (setting `Builder Hut.WoodCost`). Needs a Town Hall nearby, like the Lumberjack's Hut.
- Hires a builder straight away. He builds his own hut first, then every other hut's building in the order the huts
  were placed. **Shift+E**: the worker, what he's working on, and how many buildings wait.
- **E**: 18-slot storage — put building materials here (he also takes from the Town Hall and the other huts).
- **Hand over** (0.23, on its Hut tab; MineColonies' arrow): what his current order (or the colony's first) still
  needs beyond what the colony's chests hold for him and what he already carries (0.26) goes from your bag into this
  chest, as much as you carry ("Handed over 12 Wood, 4 Stone"). Equipped items stay with you.
- A site that waits on you (a tree or rock above his level, a tool, materials, something in the way) holds him for a
  minute at most when there is other work: he builds another hut (his own first) and comes back after five minutes,
  once he is free or that hut waits on you too.
  With nothing else to do he stays at the site and carries on as soon as you have helped.
- Every hut's window shows its building: "Under construction: 12 of 29 pieces" (or "Being repaired: 2 pieces to put
  back"), the builder's name, what he needs, and pieces he left out (underground at this spot, or they kept falling).
- **Repairs:** with nothing to build, the builder mends damaged colony buildings, and pieces a troll or a fire broke
  off a finished hut are put back as a repair order, while the hut keeps working. A piece you take away with your
  hammer stays away. See [Citizens and jobs](Citizens-and-Jobs.md#builder).

## Forager's Hut
- Cost: 20 Wood (setting `Forager Hut.WoodCost`). Needs a Town Hall nearby.
- Hires a forager once its building stands (see [Citizens and jobs](Citizens-and-Jobs.md#forager)). He picks what
  grows wild within 40 m (10 m more per level) and grows back, and fills the hut's chest: food the colony eats, and
  herbs such as dandelions and thistles for you.
- **E**: storage. **Shift+E**: the worker, his status, what the hut's level gives and how many kinds he picks.
  **What to pick…** opens the hut's list: a tick per kind, with where it grows and whether it's food. Everything is
  ticked to start except flint and branches (tick them if you want piles of them); untick what you don't want (each
  hut has its own list).

## Farm
- Cost: 20 Wood (setting `Farm.WoodCost`). Needs a Town Hall nearby.
- Hires a farmer once its building stands (see [Citizens and jobs](Citizens-and-Jobs.md#farmer)). He works **only the
  fields you mark** with **field markers** (below), as in MineColonies: a Farm has no ground of its own (since 0.20.1).
  Place a marker near the Farm, choose its crop and size, and the Farm takes it: **one field per level** (1 at level 1,
  5 at level 5). With no field his window says "No field yet" and he says "Needs a field". Crops that grew round a Farm
  before 0.20.1 are yours to harvest.
- Put a **Cultivator** and **seeds** in its chest (**E**): carrot, turnip or onion seeds, barley, flax — whatever the
  ticked crops need. The harvest comes back to the chest: food the colony eats.
- **Shift+E**: the worker, how many fields it works per level, and how many crops it grows. **What to grow…** opens
  its list: one tick per crop the game's Cultivator can plant, with its seed; crops that don't grow where the Farm
  stands are greyed. Everything that grows there is ticked to start. Like every hut's list it shows 12 lines a page;
  **< Prev** / **Next >** turn the pages. A carrot is also the seed of the carrot-seed crop:
  with both ticked the Farm keeps itself going.
- **With PlantEverything** (or another mod that lets the Cultivator place bushes): its berry bushes, mushrooms,
  thistle and dandelions are on the list too, unticked until you tick them, with their price ("seed: 5 Raspberries").
  Ticked, the farmer plants a bush on a free plot for that price from the Farm's chest, picks it whenever it's ripe and
  leaves it to regrow (a bush takes its plot for good; take it away with the hammer to plant crops there again).
- **Fields**: its window's **Fields** tab says "Fields: 2 of 3", then lists every field of the colony, nearest first,
  with **Assign** / **Leave**, and a tick: **New fields join this Farm by themselves** (on).

## Field markers
- A wooden sign in the hammer's **Misc** tab (setting `Field.WoodCost`, 4 Wood), placed inside a colony's area like
  the huts. It marks a **square field** round it, turned with it: plots 1.25 m apart, the sign's own spot left out.
  While you place one, and while you look at one with the hammer or the Cultivator, its square shows on the ground.
- The sign shows the field's crop ("Carrots", or "Mixed crops" for the Farm's list).
- **E** on it opens its window: the crop (**Crop…**: the Farm's list, or one crop; crops that don't grow there are
  greyed, a bush shows its price), the size (**−** / **+**: 3×3, 5×5, 7×7, 9×9 or 11×11 plots, 8 to 120; a new one is 5×5),
  the Farm that works it with **Assign to a Farm** / **Leave it**, and how its plots stand (growing, ripe, bare).
- A new marker joins the nearest Farm of its colony that takes new fields by itself and has room. With none, it says
  "No Farm" until one has room (upgrade a Farm, or build another; a Farm being upgraded takes fields too).
- A field you took from its Farm with **Leave it**, or gave a Farm with **Assign**, stays as you set it: new fields
  joining by themselves don't move it. If its Farm is taken down, it joins another with room by itself.
- Only players who may manage the colony place a marker in it or change one; anyone may look. Removing it ends the
  field; what grows there stays, for you.

## Longhouse
- Cost: 20 Wood (setting `Longhouse.WoodCost`). Needs a Town Hall nearby. No job: it's where settlers live.
- The builder puts up its building, a long hall with **beds**: 2 at level 1, 2 more each level (10 at level 5), bunk
  style along both long walls with the chest at the back and a clear aisle down the middle. Each
  bed is a settler's home; the colony shares them out by itself, nearest first. A bed that's knocked down frees its
  settler, who gets the next free one. While the Longhouse goes up a level its settlers wait for the new beds.
- **E**: storage, like every hut's. **Shift+E**: the beds and who sleeps in each.

## Hut windows
- **Shift+E** on a job hut opens its window. The Lumberjack's Hut's Hut tab has **Trees…**, **Stop at** and **Recall** in
  a row. A Farm's has three tabs: **Hut**, **Fields** and **Keep in stock**; the
  other huts' (and the Longhouse's) have two: **Hut** and **Keep in stock**.
- The Hut tab: its level and what it gives, its worker (and what he's good at) with **Hire**, **Fire**, **Auto-hire** and
  **Recall** (0.20: brings him back to just outside his hut's door, wherever he is in the loaded world; only for
  players who may manage the colony), its list (Trees, What to pick, What to grow), its building and upgrade. The
  worker line shows his skill ("Astrid (good at foraging, Farming 12)").

## Keep in stock
- (0.21, MineColonies' minimum stock.) Every hut, the Longhouse and the Town Hall have a **Keep in stock** tab: a list
  of items, each with an amount, that its chest keeps. "Keep in stock: 2 of 5", then a row per item with what the
  chest holds of what it keeps ("8 / 10", orange while short), **−** / **+** (by 5; with Shift by a whole stack) and
  **×** to take it off. **Add…** lists **Food (any)** (any food a settler eats) and every item the colony's chests
  hold; tick one to keep a whole stack of it.
- Room on the list: 5 items per level on a job hut, 10 per level on the Longhouse, 10 on the Town Hall. A full list
  greys Add… and says "The list is full (5 at level 1)".
- **Other settlers leave kept items alone**: breakfast, meals, feeding fires and builders take only what a chest holds
  beyond what it keeps. The building's own worker uses all of it (the farmer's and lumberjack's seeds, the builder's
  materials in his Builder's Hut); the Town Hall feeds newcomers from its food. A settler whose meal is due eats kept
  food only when there's no other food in the colony.
- **Settlers with free time bring what's missing**: one of them takes it from a colony chest that can spare it and
  carries it over, up to 20 at a time, one settler per building and item. Hover: "(carrying 10 Raspberries to the Town
  Hall)". Setting `Colony.CarryToStock` (on).
- Only players who may manage the colony change a list. A building that never had its list changed keeps nothing,
  except the Town Hall (10 food).
- **A Farm whose fields grow seed carrots, seed turnips or seed onions** plants a Carrot, a Turnip or an Onion for
  each, and those are food: settlers eat them from its chest like any other. Put a few on the Farm's Keep in stock list
  so the seed cycle never stalls.

## Placing a hut
- While you place a hut, its building shows as a see-through outline, with a line under the crosshair:
  - **Green** — ready: the builder can start building straight away.
  - **Yellow** — the builder clears or flattens the site first. The line says what ("2 trees, 1 rock, flatten the
    ground (about 12 stone)") and which tools he needs in the colony's chests (an axe, a pickaxe, a hoe) — or clear it
    yourself. A tree or rock that needs a better Builder's Hut than the colony has gets a second line: "1 tree needs a
    level 2 Builder's Hut — or clear it yourself". The ground in front of each door counts too: he levels it and
    clears what grows or lies there (bushes, small trees, stumps, rocks, logs), never items or anyone's building.
  - **Red** — the hut can't go here: another building or another hut's site is in the way, it's outside the colony
    area, it's someone else's colony (you need to be on its owner's ward there), inside someone else's ward, in a place where building isn't allowed, below the water line, too steep (the
    ground varies more than 4 m), or raised higher than the design's posts reach. Red huts can't be placed.
- **Page Up / Page Down** raise or lower the hut 25 cm at a time, up to 2 m (settings `Placing.RaiseKey` and
  `Placing.LowerKey`). A raised hut stands on its design's posts; a design without posts can't be raised.
- While you hold the hammer, unfinished buildings within 50 m show the pieces still to come as a light outline.

## Blueprints
- Each hut's building comes from a blueprint (PlanBuild's `.blueprint` text format). The mod ships plain placeholders
  (with a wooden door).
- To use your own design: in a test world with `devcommands` on, place the hut's chest, build the building around it,
  look at the chest and type `vc_blueprint save lumberjack_hut` (or `builder_hut`, `forager_hut`, `farm`, `longhouse`)
  in the console. It is saved to
  `BepInEx/config/VikingColonies/blueprints/` and used for new huts of that kind. The command also lists pieces that
  barely hold.

## Levels and upgrades
- Huts have levels 1–5, following the game's eras: 1 Meadows; 2 Black Forest and Swamp; 3 Mountains and Plains;
  4 Mistlands; 5 Ashlands. A hut's window (Shift+E) shows its level.
- Each level has its own design: `<hut>.blueprint` for level 1 and `<hut>_2.blueprint` … `<hut>_5.blueprint`. Save
  yours with `vc_blueprint save <hut> <level>`; a tip: in a test world, `vc_build upgrade` puts up the next level at
  once, so you can start a new level's design from the one before. The mod's placeholders are plain longhouses built
  from each era's materials; a level can only be built when you can supply what its design uses. A level opens with
  the first era of its band: level 2's placeholders are core wood, so a colony reaches level 2 in the Black Forest
  age and its workers use bronze axes on birch and oak (no iron needed). Saving a design that uses nothing from its
  level's first era gives a gentle warning.
- "Upgrade to level N" in the hut's window orders the upgrade. It says what the upgrade needs, or why it can't happen
  yet (the building isn't finished, the Builder's Hut is too low, the bigger building can't go there).
- The builder keeps the pieces that are the same in both designs, takes the old ones down from the top (their materials
  drop and he brings them back to his hut) and builds the new ones. The ground stays where the hut has it (he raises
  it a little when the new design's floors would otherwise not rest on it). He changes
  nothing before he has a new piece's materials: without them he waits ("Needs …") and the hut stays as it is. The hut
  keeps working at its old level until he is done. You can cancel until he has changed the first piece.
- A builder builds and upgrades huts up to his own Builder's Hut's level; his own hut can always go one level higher,
  so upgrade the Builder's Hut first.

### What a level gives
- **Lumberjack's Hut:** the lumberjack works 10 m further out per level (40 m at level 1, 80 m at level 5;
  `Lumberjack.RadiusPerLevel`), and may use better axes: up to flint (1), iron (2), black metal (3), Jotun Bane (4),
  Berserkir (5). He borrows a copy of the best allowed axe in the colony's chests (the axe stays in the chest). His
  Trees list fells the kinds that axe can fell.
- **Builder's Hut:** the builder may use axes and pickaxes up to the same ladder (pickaxes: antler, iron, black metal).
  A tree or rock that needs a better tool than his level allows: he says which Builder's Hut level it takes — or
  clear it yourself. A level-1 builder uses only a flint axe and an antler pickaxe, so keep one in a chest; birch and
  oak on his sites wait for a level-2 Builder's Hut (he works on other sites meanwhile).
- **Longhouse:** two more beds per level.
- **Forager's Hut:** the forager works 10 m further out per level (40 m at level 1, 80 m at level 5).
- **Farm:** one more field per level (1 at level 1, 5 at level 5).
- **Every hut's chest** has a row more per level (`Storage.RowsPerLevel`); it never shrinks.
- The hut's window shows what its level gives. A hut gets its new level's perks when the upgrade is finished.
