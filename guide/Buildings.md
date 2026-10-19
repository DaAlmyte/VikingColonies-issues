# Buildings

## Town Hall
- Cost: 20 Wood, 10 Stone (settings `Town Hall.WoodCost`, `Town Hall.StoneCost`). Needs a workbench nearby.
- Founds a colony. On first build it adopts nearby citizens without a colony, then tops up to the starting citizen
  count (4 by default). Later, any citizen without a colony who comes inside its area joins too.
- **E**: 24-slot colony chest; keep food here for newcomers (settlers eat from any colony chest). It keeps 10 food of
  any kind for them to start (its [Keep in stock](#keep-in-stock) list): settlers eat food beyond that first.
- **Shift+E**: the colony's window, in five tabs (the fifth, **Hall**, since 1.4: see Levels below), and **Sound the alarm** (1.3) beside Close: everyone of the colony
  shelters indoors as in a raid, and the guards gather round where you stood (each at their own spot) and fight any
  monster within 30 m of it (a call for help still brings them), for 5 minutes or until **All clear**. Players in the colony's area are told when it starts and ends.
  - **Citizens**: the colony at a glance (beds taken, food in this chest, how many are hungry, what the next newcomer
    waits for), then every citizen (name, job, status, workplace), ten a page. Citizens nobody is near show their last
    known status; vanished citizens show as *Missing* and drop off after 3 in-game days. Click a citizen to choose
    them, then **Recall** brings them at once to a free spot by the Town Hall, wherever they are in the loaded world (stuck
    somewhere, or just far off); they carry on with their work from there. Only players who may manage the colony (its
    owner, or players on a ward covering it) can recall. A settler marked *Missing* (their body is lost) gets **Bring
    back** instead: the Town Hall keeps what it needs of every member (name, looks, job, home, skills) and brings them
    back as themselves, empty-handed, if their body isn't anywhere in the world. The window tells how it went: back, back but gone indoors
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
      within seconds. If it waits on you (materials, a tool, a higher Builder's Hut), they still set it aside after a
      minute and works on something else; press Do first again once you've helped.
    - **Set aside**: no builder takes it until you press **Resume** (a builder on it leaves it at once). Handy for an
      order you can't supply yet.
    - **Cancel upgrade**: as in the hut's window, only before the builder has changed anything.
    - **Leave as it is** (in its place for a repair): the missing pieces aren't put back, and aren't asked for again.
  - **Keep in stock** (0.21): what its chest keeps, as on every hut (below). To start, Food (any) × 10, for newcomers.
- Its colony area is a 50 m circle at level 1 (setting `Colony.ColonyRadius`), 10 m more per level. Job huts can only
  be built inside it.
- **Levels (1.4, the Hall of Trophies):** the Town Hall goes from level 1 to 5. **Shift+E › Hall** shows its level,
  what it gives, and what the next level needs and gives:

  | Level | Show the hall | Materials (from its chest, used up) | Colony area | Settlers | Huts up to |
  |---|---|---|---|---|---|
  | 1 | — | — | 50 m | 10 | level 1 |
  | 2 | Eikthyr's trophy | 40 Wood, 20 Stone, 10 Deer Hide | 60 m | 15 | level 2 |
  | 3 | The Elder's and Bonemass's trophies | 40 Core Wood, 40 Stone, 20 Bronze, 20 Iron | 70 m | 20 | level 3 |
  | 4 | Moder's and Yagluth's trophies | 40 Fine Wood, 30 Silver, 20 Black Metal | 80 m | 25 | level 4 |
  | 5 | The Queen's trophy | 30 Yggdrasil Wood, 40 Black Marble, 10 Refined Eitr | 90 m | 30 | level 5 |

  - **Showing a trophy:** hang it on an item stand within 10 m of the Town Hall, or put it in its chest (levels 3 and
    4 need two trophies), then press **Raise to level N**. A Forsaken your world has already beaten counts without
    its trophy ("beaten in this world"), so trophies already on the sacrificial stones needn't be won again
    (`Town Hall.BeatenBossesCount`). It isn't used up: take it to the sacrificial stones afterwards if you like. The Hall tab
    also lists every Forsaken's trophy shown in the hall now.
  - **Settlers:** newcomers stop at the level's number (never past `Colony.MaxSettlers`); nobody leaves.
  - **Huts:** a hut can be upgraded to the Town Hall's level at most ("Upgrading to level 3 needs a level 3 Town
    Hall"), besides needing a Builder's Hut of that level: each hall level opens the next age of huts. Huts already
    higher keep their level.
  - The Town Hall's chest gets a row more per level (`Storage.RowsPerLevel`).
  - Only players who may manage the colony can raise it. The Saga records it, and everyone in the colony's area is
    told. Costs and numbers are settings (`Town Hall.Level2Cost` …, see [Settings](Settings.md)); `Town Hall.Levels =
    false` turns levels off (the colony as before 1.4).
  - A Town Hall from before 1.4 is level 1. A new Town Hall that takes over a colony keeps the level it had reached.
- Colony buildings aren't destroyed by falling trees or rolling logs; monsters can still damage them.
- **Only players can damage the Town Hall chest**: monsters, raids, fire and stray rocks can't break it. You can still
  remove it with the hammer; the Ashlands' heat and lava, the Deep North's cold and a collapse (no support) can still
  destroy it, like any building.
- **If it's lost anyway**, the colony lives on for 3 in-game days (setting `Colony.TownHallGraceDays`, 0–10): its
  settlers keep their jobs and its huts keep working, and the huts say "The Town Hall is gone: build a new one here
  within N days to keep the colony". A new Town Hall built among them in that time takes the colony over — the same
  settlers, huts and orders, and no newcomers. After that, settlers lose their colony and job as before, and the next
  Town Hall founds a new colony. With `TownHallGraceDays = 0` a colony ends 30 seconds after its Town Hall is gone.

## The Town Hall camp (1.4)
- The place the colony gathers. The builder puts it up round the Town Hall's chest (the chest stays where you put it,
  at the back of the camp under a lean-to, facing the fire), and it grows with the hall's level:

  | Hall level | What it adds |
  |---|---|
  | 1 | a fire pit 6 m in front of the chest, a thatched lean-to over the chest, two standing torches |
  | 2 | three sitting logs round the fire, a maypole beyond it, the first trophy rack (two item stands) |
  | 3 | the fire becomes a bonfire; a chieftain's stone seat across it; a second trophy rack |
  | 4 | shingles on the lean-to, dvergr lanterns beyond the side seats, a longer first rack |
  | 5 | grausten pillars under the lean-to, lava lanterns where the torches stood |

- **Trophies** hung on its racks are within 10 m of the hall's chest, so they count for raising the hall.
- **In the evening** the colony gathers at the camp's fire before any other burning one; settlers keep it fed with wood
  from the colony's chests.
- **A new Town Hall** orders the camp at once; a builder puts it up after the huts (you can move its order first in
  Work orders). **A Town Hall from before 1.4** gets no camp until you press **Build the camp** in its Hall tab.
- Raising the hall orders the camp's next level. It **waits** while pieces of yours stand where it goes (the builder
  never takes down your buildings), or for a Builder's Hut of that level; the Hall tab says what it waits for.

## Lumberjack's Hut
- Cost: 20 Wood (setting `Lumberjack Hut.WoodCost`). Needs a Town Hall nearby instead of a workbench: it only shows
  in the hammer while you stand well inside a Town Hall's colony area (within about 44 m), so the hut lands inside it. A hut outside every colony (its Town Hall was
  destroyed) says "Build near a Town Hall" and joins as soon as a Town Hall is in range.
- **E**: 18-slot storage where the lumberjack delivers wood and seeds and fetches seeds for replanting.
- Put a **Cultivator** in its storage, or any of the colony's chests, to let the lumberjack replant (it isn't used
  up). The hut window shows "Fells 5 of 6 kinds, replants 3 · Replanting: on" ("needs a Cultivator in the colony's
  chests", "off (setting)").
- **Trees…** (0.22, in place of the replanting list; MineColonies' Saplings tab): a line per tree kind (Beech, Birch,
  Fir, Pine, Oak, Ancient tree…, and a mod's trees by name) with two ticks. **Fell**: the lumberjack cuts that kind down (ticked
  for every kind their axe allows; untick one and they leave those trees standing). **Replant**: where they fell a tree they
  plant the ticked kinds' saplings in turn (greyed for a kind with no sapling, that doesn't grow there, or whose
  grown tree needs a better axe: "replanting needs a level 3 hut"). Your
  replanting choices from before 0.22 are the Replant ticks.
- **Stop at** (0.22): "no limit", 200, 500 or 1000 Wood — with that much Wood in the colony's chests they rest
  ("Enough wood") and start again below it.
- **Shift+E**: the worker (name and status), **Hire**, **Fire**, **Auto-hire** (on by default — a hut without a
  worker hires a jobless citizen by itself). Firing switches auto-hire off so the same citizen isn't re-hired at once.
- Destroying the hut makes its worker jobless (after about 30 seconds — a building has to be missing that long to
  count as gone, so one that is still loading isn't mistaken for a destroyed one).
- **Take down** (0.23, any finished hut's window; click twice, "Sure? Take it down"): a builder takes its building down
  from the top (with any leftovers of an older level), as they take old pieces away in an upgrade, and the materials go
  to their hut; they clear nothing round it first. It is ordered only when all of the hut is loaded ("Come closer…"), so
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
- Hires a builder straight away. They build their own hut first, then every other hut's building in the order the huts
  were placed. **Shift+E**: the worker, what they're working on, and how many buildings wait.
- **E**: 18-slot storage — put building materials here (they also take from the Town Hall and the other huts).
- **Hand over** (0.23, on its Hut tab; MineColonies' arrow): what their current order (or the colony's first) still
  needs beyond what the colony's chests hold for them and what they already carry (0.26) goes from your bag into this
  chest, as much as you carry ("Handed over 12 Wood, 4 Stone"). Equipped items stay with you.
- A site that waits on you (a tree or rock above their level, a tool, materials, something in the way) holds them for a
  minute at most when there is other work: they build another hut (their own first) and come back after five minutes,
  once they are free or that hut waits on you too.
  With nothing else to do they stay at the site and carry on as soon as you have helped.
- Every hut's window shows its building: "Under construction: 12 of 29 pieces" (or "Being repaired: 2 pieces to put
  back"), the builder's name, what they need, and pieces they left out (underground at this spot, or they kept falling).
- **Repairs:** with nothing to build, the builder mends damaged colony buildings, and pieces a troll or a fire broke
  off a finished hut are put back as a repair order, while the hut keeps working. A piece you take away with your
  hammer stays away. See [Citizens and jobs](Citizens-and-Jobs.md#builder).

## Forager's Hut
- Cost: 20 Wood (setting `Forager Hut.WoodCost`). Needs a Town Hall nearby.
- Hires a forager once its building stands (see [Citizens and jobs](Citizens-and-Jobs.md#forager)). They pick what
  grows wild within 40 m (10 m more per level) and grows back, and fill the hut's chest: food the colony eats, and
  herbs such as dandelions and thistles for you.
- **E**: storage. **Shift+E**: the worker, their status, what the hut's level gives and how many kinds they pick.
  **What to pick…** opens the hut's list: a tick per kind, with where it grows and whether it's food. Everything is
  ticked to start except flint and branches (tick them if you want piles of them); untick what you don't want (each
  hut has its own list).

## Farm
- Cost: 20 Wood (setting `Farm.WoodCost`). Needs a Town Hall nearby.
- Hires a farmer once its building stands (see [Citizens and jobs](Citizens-and-Jobs.md#farmer)). They work **only the
  fields you mark** with **field markers** (below), as in MineColonies: a Farm has no ground of its own (since 0.20.1).
  Place a marker near the Farm, choose its crop and size, and the Farm takes it: **one field per level** (1 at level 1,
  5 at level 5). With no field the Farm's window says "No field yet" and the farmer says "Needs a field". Crops that grew round a Farm
  before 0.20.1 are yours to harvest.
- Put **seeds** in its chest (**E**) and a **Cultivator** in it or any of the colony's chests: carrot, turnip or onion seeds, barley, flax — whatever the
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

## Watchtower
- (1.1) Cost: 20 Wood (setting `Watchtower.WoodCost`). Needs the colony nearby, as every hut: within the colony's
  area (see [The colony's area](#the-colonys-area)).
- Hires a guard once its building stands (see [Citizens and jobs](Citizens-and-Jobs.md#guard)) — **two at level 3–4,
  three at level 5** (1.2), each at their own place by the door. They keep watch and fight monsters that come near the
  colony with the best gear in its chest — copies, the items stay in the chest:
  - **Role** (its window's button, 1.2): **Warrior** (to start) takes the best melee weapon (a club, an axe, a sword, a
    spear, an atgeir, a mace…) and a shield with a one-handed one; **Archer** takes the best bow or crossbow that has
    its ammunition in the chests (arrows, bolts), and that ammunition (never used up). Tools, torches and things thrown
    are left alone.
  - **Armour** (1.2): the best helmet, chest, legs and cape in the chest, worn in place of their trade's clothes; it
    protects them as a player's armour does.
  - With nothing in its chest they take the best in the colony's other chests; with nothing anywhere they say "Needs a
    weapon in the Watchtower's chest" (an archer: "a bow and arrows") and shelter like anyone.
- **It pushes the colony's border out**, as MineColonies' guard towers do: once its building stands, the ground 25 m
  round it (5 m more per level, 45 m at level 5) is part of the colony's area, so you can build huts by it. A
  Watchtower in the area can stand at its edge, and the next one at the edge of that: the colony grows tower by tower,
  up to `Colony.MaxReach` (150 m) from the Town Hall: of a tower near that edge only the part of its circle within
  reach counts (none when less than 10 m is left; its guard still keeps watch). Upgrading or repairing a tower never
  takes its ground away.
- **Orders** (1.3, its window): **Patrol** (to start: rounds of the colony's buildings) or **Hold post** (no rounds: a
  gatehouse). **Post here** puts its guards' post where you stand (within the tower's patrol circle); **Post by the
  tower** puts it back.
- **No monsters spring up** within a finished tower's circle (1.3), as by a workbench or a fire (setting
  `Watchtower.StopsSpawns`).
- **E**: storage (the guards' armoury). **Shift+E**: its guards ("2 of 2: Ulf (Fighting 12, 7 kills) — On watch; …"),
  Hire, Fire (one at a time), Auto-hire, Recall, **Role**, **Orders**, **Post here**, what the tower's level gives
  ("keeps watch and holds the border 25 m around the tower"), and Keep in stock.

## The colony's area
- The Town Hall's circle (`Colony.ColonyRadius`, 50 m) and a circle round each finished Watchtower of the colony
  (1.1). Huts and field markers can stand anywhere in it, and a hut joins the colony whose area holds it: the Town
  Hall's circle first, then the nearest tower's. While you place a hut, rings on the ground show every circle near you.
- Where settlers live — their free time, the evening, doors, newcomers walking in, death messages — is still the Town
  Hall's circle.

## Longhouse
- Cost: 20 Wood (setting `Longhouse.WoodCost`). Needs a Town Hall nearby. No job: it's where settlers live.
- The builder puts up its building, a hall round its hearth with **beds**: 2 at level 1, 2 more each level (10 at
  level 5), along its walls with a clear way to each. Each
  bed is a settler's home; the colony shares them out by itself, nearest first. A bed that's knocked down frees its
  settler, who gets the next free one. While the Longhouse goes up a level its settlers wait for the new beds.
- **E**: storage, like every hut's. **Shift+E**: the beds and who sleeps in each.

## Hut windows
- **Shift+E** on a job hut opens its window. The Lumberjack's Hut's Hut tab has **Trees…**, **Stop at** and **Recall** in
  a row. A Farm's has three tabs: **Hut**, **Fields** and **Keep in stock**; the
  other huts' (and the Longhouse's) have two: **Hut** and **Keep in stock**.
- The Hut tab: its level and what it gives, its worker (and what they're good at) with **Hire**, **Fire**, **Auto-hire** and
  **Recall** (0.20: brings them back to just outside their hut's door, wherever they are in the loaded world; only for
  players who may manage the colony), its list (Trees, What to pick, What to grow), its building and upgrade. The
  worker line shows their skill ("Astrid (good at foraging, Farming 12)").

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
  materials in their Builder's Hut); the Town Hall feeds newcomers from its food. A settler whose meal is due eats kept
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
    ground (about 12 stone)") and which tools they need in the colony's chests (an axe, a pickaxe, a hoe) — or clear it
    yourself. A tree or rock that needs a better Builder's Hut than the colony has gets a second line: "1 tree needs a
    level 2 Builder's Hut — or clear it yourself". The ground in front of each door counts too: they level it and
    clear what grows or lies there (bushes, small trees, stumps, rocks, logs), never items or anyone's building.
  - **Red** — the hut can't go here: another building or another hut's site is in the way, a rock nothing can break
    (a cliff, or a boulder no pickaxe breaks) stands where it goes, it's outside the colony
    area (the Town Hall's circle and its Watchtowers'), it's someone else's colony (you need to be on its owner's ward there), inside someone else's ward, in a place where building isn't allowed, below the water line, too steep (the
    ground varies more than 4 m), or raised higher than the design's posts reach. Red huts can't be placed.
- **Page Up / Page Down** raise or lower the hut 25 cm at a time, up to 2 m (settings `Placing.RaiseKey` and
  `Placing.LowerKey`). A raised hut stands on its design's posts; a design without posts can't be raised.
- While you hold the hammer, unfinished buildings within 50 m show the pieces still to come as a light outline.

## Blueprints
- Each hut's building comes from a blueprint (PlanBuild's `.blueprint` text format). Since 1.4 the mod ships a Viking
  building for each hut and level (and the Town Hall's camp), made with our design tool; before 1.4 they were plain
  placeholders.
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
  once, so you can start a new level's design from the one before. Since 1.4 the mod's own designs are Viking
  buildings made for each trade, looking their age (thatch and logs, a stone plinth, darkwood shingles, grausten), built
  from what that age gives and never from a trader's wares; a level can only be built when you can supply what its
  design uses. A level opens with
  the first era of its band: level 2 is built from core wood, fine wood and a little bronze, so a colony reaches level 2 in the Black Forest
  age and its workers use bronze axes on birch and oak (no iron needed). Saving a design that uses nothing from its
  level's first era gives a gentle warning.
- "Upgrade to level N" in the hut's window orders the upgrade. It says what the upgrade needs, or why it can't happen
  yet (the building isn't finished, the Builder's Hut is too low, the bigger building can't go there).
- The builder keeps the pieces that are the same in both designs, takes the old ones down from the top (their materials
  drop and they bring them back to their hut) and builds the new ones. The ground stays where the hut has it (they raise
  it a little when the new design's floors would otherwise not rest on it). They change
  nothing before they have a new piece's materials: without them they wait ("Needs …") and the hut stays as it is. The hut
  keeps working at its old level until they are done. You can cancel until they have changed the first piece.
- **Old huts and the new designs (1.4):** a hut built before 1.4 is rebuilt at its next upgrade: the builder takes its
  old building down piece by piece (the materials go back to their hut) and puts up the new design, clearing the
  doorways first so nobody is walled in. A bed you set as your spawn is left standing. On sloping ground a bigger new
  building may need the ground evened out round it; if a site can't be reached, the hut's window says so.
- A builder builds and upgrades huts up to their own Builder's Hut's level; their own hut can always go one level higher
  (up to the Town Hall's level, like every hut), so upgrade the Builder's Hut first.

### What a level gives
- **Lumberjack's Hut:** the lumberjack works 10 m further out per level (40 m at level 1, 80 m at level 5;
  `Lumberjack.RadiusPerLevel`), and may use better axes: up to flint (1), iron (2), black metal (3), Jotun Bane (4),
  Berserkir (5). They borrow a copy of the best allowed axe in the colony's chests (the axe stays in the chest). Their
  Trees list fells the kinds that axe can fell.
- **Builder's Hut:** the builder may use axes and pickaxes up to the same ladder (pickaxes: antler, iron, black metal).
  A tree or rock that needs a better tool than their level allows: they say which Builder's Hut level it takes — or
  clear it yourself. A level-1 builder uses only a flint axe and an antler pickaxe, so keep one in a chest; birch and
  oak on their sites wait for a level-2 Builder's Hut (they work on other sites meanwhile).
- **Longhouse:** two more beds per level.
- **Forager's Hut:** the forager works 10 m further out per level (40 m at level 1, 80 m at level 5).
- **Farm:** one more field per level (1 at level 1, 5 at level 5).
- **Watchtower:** one guard at levels 1–2, two at 3–4, three at 5 (1.2); they keep watch, and its circle of the colony's area reaches, 5 m further per level (25 m at
  level 1, 45 m at level 5).
- **Every hut's chest** has a row more per level (`Storage.RowsPerLevel`); it never shrinks.
- The hut's window shows what its level gives. A hut gets its new level's perks when the upgrade is finished.
