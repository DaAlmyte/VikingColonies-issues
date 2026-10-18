# Citizens and jobs

- Citizens are vikings with random looks and Norse names. Hover one to see its name, job and status. A settler near
  you who needs something says so above his head ("Needs 12 Wood", "Storage full", "Can't reach the hut", "Hungry";
  setting `Messages.WordsAboveHeads`); plain work shows nothing. In their free time they greet you and make small talk
  (see "Free time").
- **Jobless** citizens spend their free time near the Town Hall. **No colony** means their Town Hall was destroyed (it must be missing
  for about 30 seconds); any Town Hall within 50 m adopts them, including a new one you build.
- Players can't hurt citizens; monsters can. A citizen who dies is gone (see "When a settler dies" below).
- When a monster comes within 12 m (or a monster nearby is alerted or hunting), or hits them, citizens run to their
  Town Hall or hut (status "Fleeing", with a red "!" over their head), or straight away from the monster if it is by both. They go back to what they
  were doing once no monster has been near for 15 seconds. Deer, birds and sleeping or penned animals don't scare them.
- Citizens jog like a player normally does and only sprint when fleeing.
- **Doors:** settlers open closed doors on their way — doors inside their colony's area that the colony's owner may open
  (no key, no one else's ward) — walk through, and close them behind them once they are 2 m past. A door they didn't open
  is left as it is, and a door is never closed on someone standing in the doorway. A chest behind a wall or a window
  isn't reached through it: they walk round and in. A settler whose way is cut off by a wall looks for a door near him
  straight away, rather than first walking to where the way ends.
- **One at a time:** settlers going through the same door take turns; the others wait beside it, out of the way (or
  a few steps straight back from it, at a gate with walls on both sides), and two coming from opposite sides let one
  through first. Anyone standing in the doorway (a player, or a settler run by
  another computer in multiplayer) is waited for, up to 12 seconds. A door with a stair or a bump right in front of
  it is used from further out, at the stair's foot.
- **Getting unstuck:** a settler whose walk doesn't move him (a log, a step, someone in the way) hops after three
  seconds and steps aside after five — twice, then he leaves it to his job to find something else to do. One who keeps
  trying to walk for two minutes without getting out of a few metres of ground (boxed in by walls) is moved to a free
  spot by the Town Hall, out of sight, when no player is within 30 m (after five minutes, whoever is near); never at
  night or in a raid, and at most twice in ten minutes. Waiting somewhere on purpose doesn't count. A monster in a
  doorway is never waited for.
- **Wedged inside a hut** (0.20): one who tries to walk for half a minute inside a hut without getting anywhere is moved
  to just inside its door, behind its walls, at any time (at most twice in ten minutes, with the rescue above).
- **Turned huts** (0.20): inside a hut, which side of its door a settler is on comes from the hut's shape. Before 0.20
  the game's walking map decided, and inside a hut turned off the compass it could be wrong, trapping its worker inside
  after he fetched from the chest. When the walking map gives him no way to the door from inside, or one that brings
  him no closer, he walks to it straight, hopping over a lip and stepping round the chest.

## Who they are
- **A trade he's good at (calling):** each settler is good at one trade (woodcutting, building, foraging or farming),
  or is a jack of all trades (1 in 5). In that trade he works 20% faster (`Colony.CallingBonus`). A hut hires a
  jobless settler good at its trade first; newcomers often bring the trade an empty hut needs.
- **A trait:**
  - hardworking (10% faster) or lazy (10% slower, he'd rather sit, and tends the fires half as often);
  - cheerful or grumpy;
  - chatty (talks and chats twice as often) or quiet (never starts a chat, sits by the fire instead);
  - brave (runs only when a monster is within 6 m) or timid (runs from 20 m).
- **Where he came from:** "from the coast", "from a farm in the Meadows", "from over the mountains"… The Saga says so:
  "Day 12: Astrid came from the coast: a forager, cheerful."
- **Hover** over him: a third line with his trait and trade ("Cheerful · good at foraging").
- **Out of sight:** in the Citizens tab a settler not loaded on your computer shows his last status and "(far
  away)", or "(seen day 12)" when the colony last saw him on an earlier day. One not where he should be is Missing.
- **Town Hall:** choose him in the Citizens tab and the line under the header says who he is, how long he's been
  here and where he sleeps ("Home: Longhouse bed 2."), and how he feels.
- **The hut's window** says when its worker is good at its trade: "Astrid (good at foraging) — Picking".
- **Clothes:** settlers dress by trade, in the game's own clothes:
  - the jobless in rags;
  - lumberjacks in leather;
  - builders in leather with a cap;
  - farmers in rags and leather trousers;
  - foragers in rags and troll-hide trousers.
  The clothes give no armour, and they never go in his cairn.
- Settlers from before 0.16 get a trade, trait and origin from who they are (always the same), and their days count
  from the day you first play 0.16.

## Free time
- A settler with nothing to do spends free time within 15 m of his hut (the Town Hall for the jobless). That means a
  jobless settler, or a worker whose job has nothing to do just now: "No trees nearby", "Crops growing", "Nothing to
  pick", or the builder's "No work". Every 30–90 seconds he picks one of these:
  - **A seat:** any free piece you can sit on (bench, chair, stool, throne, a mod's seat), one near a burning fire
    first. He sits there 40–90 seconds and now and then laughs or raises a toast.
  - **The fire:** a burning campfire, hearth or bonfire (not a torch). He sits on the ground 2–3 m from it, facing it.
  - **A chat** with another settler in free time within 20 m. They meet halfway, face each other and take turns talking
    with their hands.
  - **A stroll** to somewhere near, or **sitting down** on the ground for a while.
- In rain or snow nobody sits on the open ground; seats and fires with a roof over them are still used.
- A seat you sit or stand on is yours: settlers leave it, and get up if you sit down there.
- He gets up and goes the moment his job has work again, a monster comes, night falls or you recall him.
- Hover over him to see what he's doing: "Crops growing (taking a seat)", "Jobless (talking with Bjorn)".
- **Greetings:** the first time each day you come within 6 m of a settler, he says "Hail, <your name>!" (and waves, if
  he's in free time).
- **Small talk:** settlers in free time within 10 m say things above their heads. A chatting pair takes turns; others
  say a line every few minutes.
  - What they talk about follows the colony: a settler who died in the last two days, the weather, a newcomer or a new
    building today, or their job's wait.
  - A need ("Needs 12 Wood") always comes first. "Hungry" shows for a few seconds every half minute, with his talk in
    between; his hover always says it.
  - Setting `Messages.SmallTalk` (your own).
- Setting `Colony.FreeTime` turns free time off: they wait standing, as before 0.14.
- Give them somewhere to go: a few benches and a fire near the Town Hall and each hut. Hugin says so the first time a
  settler has free time with nothing to use.

## Lumberjack
- Works within 40 m of its hut (setting `Lumberjack.WorkRadius`; 10 m more per hut level, `Lumberjack.RadiusPerLevel`):
  chops trees it can cut with the best axe its hut's level allows (a flint axe of his own, or a copy of a better one in
  the colony's chests), then the
  logs and stump, picks up wood and seeds, and delivers to the hut when carrying 50 items (`Lumberjack.CarryCapacity`)
  or at night.
- Replants a sapling where the tree stood, using a dropped seed or one from the hut's storage, while a **Cultivator** is
  in the hut's storage (`Lumberjack.Replant`, `Lumberjack.ReplantNeedsCultivator`). Without one, seeds are delivered.
- **Trees list** ("Trees…" in the hut's window, 0.22): a line per tree kind with **Fell** and **Replant** ticks. He fells
  only the kinds ticked Fell, and plants the kinds ticked Replant in turn, each only where it grows and when he has its
  seed, so the forest becomes mixed. A kind is greyed when his level's axe can't fell it ("needs a level 2 hut"), it
  has no sapling, or it doesn't grow where the hut stands. Every kind the hut allows starts ticked; the hut remembers
  what you untick.
- **Trees by your buildings stay** (0.22): he doesn't fell a tree whose trunk stands within 3 m of a piece a player
  built (`Lumberjack.LeaveTreesNearBuildings`; 0 = off), measured from any part of it (0.26: a long wall's ends too). Plants, crops and saplings don't count. The builder still
  clears trees from a building site.
- **Stop at** (0.22): with the hut's amount of Wood in the colony's chests he plants what he holds, finishes the tree
  he felled last (its wood, logs and stump; 0.26), delivers his load and rests ("Enough wood"), and starts again below
  it.
- Stands at the trunk or beside a log on the uphill side, never under it, and only swings when his axe reaches.
- Has a **Woodcutting skill** like the player's: he starts as strong as a new character and improves with practice,
  at a quarter of a player's pace per hit since he chops all day (`Colony.LearningRate`; Shift+E on the hut shows
  his level). See [Skills](#skills) for the other workers'.
- Several lumberjacks share the work: each claims his tree, the logs and stump where it fell, and the wood he fetches.
- Fells trees away from your buildings, the colony's huts and unfinished building sites, and leaves trees standing
  when every direction would hit something. He finishes the logs and stump of a tree he felled before the next one,
  even when they landed or rolled outside his work area.
- After the blow that fells a tree he steps back to the side, out of the trunk's line, and waits until the logs lie
  still before he walks up to them; he never starts on a log that is still rolling. Settlers working within 25 m of a
  tree another settler fells wait for it too, and step out of the way of a log that rolls at them. Logs floating in
  water don't keep them waiting.
- Statuses: Working, Delivering, Delivering (his chest is full), Planting, Resting (night), No trees nearby, Enough wood,
  Storage full.

## Farmer
- Works from a Farm, on the **fields** assigned to it (see [Buildings](Buildings.md#field-markers)); a Farm has no
  ground of its own (0.20.1, as in MineColonies), and with no field he says "Needs a field". As a player farms: he
  cultivates a plot (with a copy of the Cultivator in the Farm's chest), plants a seed there (the field's crop, or the
  Farm's list's ticked crops in turn), picks what's ripe on his plots and carries the harvest home (up to 20 items).
- **Seeds** (0.20): he takes seeds for every plot waiting for that crop at once, up to 20, and holds them apart from
  his harvest; what's left goes back in the chest when he delivers. A field set to one crop is sown whenever its seed
  is in the chest (the seed-crop limit below is the Farm's list's).
- What comes first: night and danger as for everyone; a full load home; what he just picked; a ripe crop; planting an
  empty cultivated plot; cultivating a new one. With nothing to do he waits by the Farm: "Crops growing", "Needs
  seeds" or "Needs Cultivator" (also above his head when you're near).
- A crop is his when it stands on one of his plots. He never touches crops elsewhere, so your own garden stays yours.
  Crops grow by the game's own rules (sun, room, the right biome): barley and flax only in the Plains. He plants each
  plot only with a crop that grows on that very spot (a Farm by a biome's edge has plots in two).
- A seed crop (the carrot-seed crop: a carrot sown to grow carrot seeds) is sown only while fewer than 6 of the seed
  it gives are in the chest and his hands, so the harvest isn't all sown again. Food crops are always sown.
- A plant on his plots that can't grow there (too cold, no room, under a roof) is cleared after a minute and a half,
  and he leaves that plot for half an hour. A plot he can't cultivate, plant or get to he leaves for ten minutes.
- **Bushes (with PlantEverything):** a berry bush, mushroom, thistle or dandelion that mod makes plantable is on the
  Farm's list, unticked until you tick it. Ticked, he takes its price from the Farm's chest (5 raspberries for a
  raspberry bush), plants it on a free plot, picks it each time it's ripe and leaves it there to grow back; it isn't
  planted again (see [Buildings](Buildings.md#farm)).

## Forager
- Works from a Forager's Hut. He walks to the nearest wild plant on his hut's list that's ready within his area (40 m
  around the hut, 10 m more per level), picks it as a player does, gathers what drops and carries it home: up to 20
  items, then he delivers to the hut's chest. With nothing ready he waits by the hut ("Nothing to pick") and looks
  again every 10 seconds; bushes grow back on their own, as in the game. Hungry, he picks at half speed.
- He picks only what grows wild and grows back, and only the kinds ticked on the hut's **What to pick** list
  (everything but flint and branches to start): raspberries, blueberries, cloudberries, mushrooms, dandelions, thistles … The list comes
  from the game itself, so a kind a mod adds that grows back shows up too. Your planted crops (carrots, turnips,
  barley …) don't grow back once picked, so he never touches them, nor anything a player placed or that grows on
  cultivated ground; nor what never grows back (stones, wild seeds, the Mistlands mushrooms), or he would strip the
  land for good. Flint and branches grow back too: they're on the list but unticked until you tick them, and his
  wood and flint can feed the builder. Food someone dropped by a bush stays too: he
  gathers only what fell from the plant he picked.
- Food goes to the colony; what isn't food (dandelions, thistles) waits in his chest for you. When his chest is full he
  takes his load to the Town Hall's chest, or the nearest colony chest with room (0.21, see
  [Full chests](#full-chests)).
- What he brings home feeds the colony: settlers eat from every colony chest. Newcomers need food in the Town Hall's
  chest, so move some there.
- At dusk he delivers what he carries, then goes indoors. A full chest sends his load to another chest with room (0.21).

## Builder
- Works from the Builder's Hut. Takes one building at a time: the one you marked **Do first** in the Town Hall's Work
  orders tab, then his own hut, then the oldest waiting one; never one you **set aside** there. When you mark another
  order first he leaves his site for it within seconds. A site that waits on you for a minute is set aside by him for
  five minutes while he works elsewhere.
- Before building he prepares the site: picks up items, removes plants (picking berries and the like first), fells
  trees away from the site, chops logs and stumps, breaks rocks and takes down leftovers of old colony buildings, then
  flattens the ground — to 30 cm under the floor for a design with posts (the natural ground for a raised hut), or to
  the floors' underside for a design without posts. What he gathers goes to his hut.
- Tools stay in the colony's chests: he works with a copy of the best axe, pickaxe and hoe there, and fetches stone
  for raising low ground. The hoe levels the ground; a pickaxe is only needed for rocks and for ground more than half a
  metre too high. If one is missing he says so ("Needs a pickaxe (Antler pickaxe or better)") and waits.
- While building, he clears whatever grows or falls into the site; what he can't clear is named in the hut window but
  doesn't stop the building. He never reshapes the ground right next to another building.
- Fells a tree from behind it, opposite the way it will fall, steps clear after the blow and waits for the logs to
  settle, like the lumberjack.
- Dropped items on a new site are picked up only if they're plain (wood, stone, berries…); a player's own gear stays.
- Fetches materials (his hut, the Town Hall, then the other huts' storage), then works from spots just outside the
  building: he reaches 15 m (setting `Builder.Reach`) and never goes inside, so he can't shut himself in.
- Checks every piece with the game's support rule before placing it; lowest pieces first. A piece that falls is tried
  again later; after three falls it is skipped. Materials from fallen pieces are picked up again.
- **Mending.** With nothing to build he mends the colony's damaged buildings: any piece a builder put up (and the
  huts' own chests) below three quarters of its health, the nearest first. One swing of his hammer mends it, as yours does, and costs
  nothing. A new order takes him away once the piece in hand is mended.
- **Putting back what's broken.** Every minute a finished colony building is checked against its design. When pieces
  of it are broken (a troll, a fire, a falling tree), its order reopens as a **repair**: those pieces only, at the
  same level. A builder takes it like any order, fetches the materials and puts them back; the hut keeps working
  meanwhile. Not during a raid there or with monsters by the hut: it waits until they're gone.
- A piece you take away with your hammer is left out, never put back, so you can knock a doorway into a hut. So are
  pieces already missing when you first play 0.13, and a piece that falls again soon after it was put back three
  times. To stop a repair under way, press **Leave as it is** on it in the Town Hall's Work orders tab. The setting
  `Builder.RebuildMissingPieces` turns putting back off.
- **Takes huts down** (0.23) when you ask on a hut's window: every piece from the top, the materials to his hut; the
  hut's chest goes last (its contents to the Town Hall). A take-down needs no site preparation. Status "Taking down
  <hut> (12 pieces left)".
- Statuses: Building <hut> (12/29), Repairing <hut> (30/32), Taking down <hut>, Mending the <hut>, Fetching materials, Needs 6 Fine
  wood, Waiting for space, Can't reach the building site, Can't place: no support for <piece>, No work, Clearing the
  building site, Flattening the ground, Needs a pickaxe (Antler pickaxe or better).

## Skills
- (0.22, MineColonies: skills make them faster) Every worker learns at his work, as a player does: the lumberjack
  **Woodcutting** (he chops harder), the farmer and the forager **Farming**, the builder **Crafting**. Farming and
  Crafting make him faster: a skill of 100 works twice as fast as 0. Practice comes with every action that happened (a plot
  cultivated, planted or harvested, a pick, a piece built, mended or taken down; 0.26: not a failed try) at `Colony.LearningRate` (0.25 of a player's pace per action; it was
  `Lumberjack.LearningRate` before 0.22, and your value moves over).
- Shift+E on his hut shows his skill ("Farming 12"); the Town Hall's Citizens tab shows every skill he has when you
  choose him. A settler brought back keeps his skills.

## When a settler dies
- Players in the colony's area (the Town Hall's `ColonyRadius`) or within 50 m of the spot see
  "Ingrid the Lumberjack has died (hit by a falling tree)" in the middle of the screen and as a line in the chat.
  With `Messages.DeathMessage = ChatOnly` it shows only in the chat (each player's own setting).
- Causes: killed by *a monster's name*, attacked (the attacker is gone), hit by a falling tree, crushed, fell from a
  height, drowned, burned, froze, poisoned, choked on smoke, shot, fell off the edge of the world, struck by
  lightning, unknown cause.
- **His cairn.** A settler who dies carrying anything leaves a cairn where he fell, holding what he carried. Hover over
  it: "Here lies Ingrid the Lumberjack: killed by Greydwarf, day 37". Open it with E, like a chest; nothing can
  damage it, and once it's empty it crumbles away. Every player who got the death message has a pin "Ingrid's cairn"
  on the map; it goes when you empty the cairn (or remove it by hand). Tools he had borrowed were copies: the
  originals are still in the chests. A settler who carried nothing leaves no cairn.
- The Town Hall takes the settler off its list, and a hut with auto-hire hires the next jobless settler, as before.
- Falling trees and rolling logs don't hurt settlers while `Colony.SettlersSafeFromTrees` is on (the default); they
  still hurt players.

## Homes and meals
- **A home:** every bed in a Longhouse is a settler's home (see [Buildings](Buildings.md#longhouse)). At night a settler
  with a home lies down in his bed (`Colony.SleepInBeds`; off: he stands by it). He doesn't use a bed a player lies in,
  or one a player has claimed as his own (his spawn point); then he stands by it. One without a home sleeps in his
  workplace, as before.
- **A meal a day, at the table:** after dawn, before work, each settler goes to breakfast, at his own moment within the
  first minute (so they don't all crowd one chest). He walks to the colony chest
  that holds the food he'll eat (the nearest; the Town Hall's when as near) and takes one. He eats it on a free seat
  within 8 m of that chest, or standing by the chest. Hover: "Eating (at breakfast)". If he can't get to the chest and
  take his food within a minute (a player has it open, no way there), he eats where he is.
- **What he eats:** the plainest food there is that isn't what he had last time (when there's a choice), so raspberries
  and mushrooms go before cooked meat, meals vary, and your best food is left for you. Any food a player can eat counts; meads and potions don't. Keep food you don't want eaten out of the colony's
  chests, or on a building's Keep in stock list (0.21: then it's eaten only when there's nothing else). Breakfast takes
  only food no building keeps. A table with benches by the Town Hall makes a fine breakfast place.
- **Hungry:** a settler who finds nothing is hungry till his next meal. Hovering over him says "Hungry", and he works at
  half speed (`Colony.HungryWorkSpeed`): he chops weaker and builds slower. Nobody starves or leaves. A new settler comes
  fed, so his first meal is due the next morning.
- Turn meals off with `Colony.SettlersEat`.
- **Newcomers:** once a day, in daylight, while the colony has a free bed (more Longhouse beds than settlers), at least
  5 food in the Town Hall's chest, and isn't unhappy (see [Mood](#mood)), a newcomer comes and eats that food (the
  plainest first). One a day (`Colony.NewcomersPerDay`; one more for a joyful colony), up to 30 settlers
  (`Colony.MaxSettlers`). So: build Longhouses, keep food in the Town Hall and your settlers content, and the colony
  grows.
- **Walking in:** a newcomer appears at the edge of the colony and walks to the Town Hall:
  - He comes from about 35 m out, on dry ground with a way in, where no player is looking (behind you, or past a wall
    or a hill), on the game's walkable ground (never inside a rock or under a floor). Only if every such spot is in
    view does he come into view, as far from every player as can be.
  - With no way in, he appears by the Town Hall.
  - Players in the colony are told: "Astrid is coming to live in the colony: a forager from the coast."
  - Hover: "Arriving (from the coast)". At the Town Hall he waves.
  - The first settlers of a new Town Hall walk in together the same way.
  - Setting `Colony.NewcomersWalkIn` (on).

## Mood
Each settler has a mood from 0 to 100. It starts at 50 (content), and each of these adds or takes away:

| Reason | Change |
|---|---|
| A home bed / no home | +5 / −15 |
| A cosy bed (the comfort around it, as for your own Rested: 4+ / 7+) | +5 / +10 |
| Ate today / hungry | +5 / −20 |
| Varied food: 3+ / 4+ different foods in his last 5 meals | +5 / +10 |
| The same food 5 meals running | −5 |
| Last evening by a burning fire / with at least two others | +5 / +5 |
| Works in the trade he's good at | +5 |
| Jobless for 2 days or more | −5 |
| A settler of the colony died in the last 3 days | −10 |
| A monster hit him yesterday or today | −5 |
| A raid on the colony was held off with nobody lost (2 days) | +5 |
| Cheerful / grumpy | +10 / −10 |

| Mood | From | Work |
|---|---|---|
| Joyful | 75 | 15% faster |
| Content | 40 | as normal |
| Unhappy | 20 | 15% slower |
| Miserable | 0 | 30% slower |

- **Seeing it:** hover over a settler ("Cheerful · good at foraging · Content"), or choose him in the Town Hall's
  Citizens tab: "Content (62): +5 home, +5 cosy bed, +5 ate, -10 Ingrid died". The tab's top line shows the colony's
  mood (the settlers' average).
- **Words:** an unhappy settler says his worst reason now and then ("Nowhere to lay my head.", "Same food every day.",
  "We lost Ingrid."). Hugin explains mood the first time one is unhappy near you.
- **Newcomers:** nobody joins an unhappy colony ("Next newcomer: nobody wants to join an unhappy colony"); a joyful one
  gets one more a day.
- Nobody leaves over it. A cosy Longhouse (a fire, rugs, a table), food of several kinds and an evening fire go a long
  way. The cheerful talk of good things, the grumpy grumble.
- Worked out once a minute. Turn it off with `Colony.Mood` (everyone content, newcomers as before).

## The evening
- From 0.70 of the day (about a minute and a half before night), work stops the way it does at nightfall: the
  lumberjack delivers what he carries, the builder leaves his site. Then the settlers gather at the colony's fire: the
  burning campfire or hearth inside the colony nearest the Town Hall (one under a roof first). With none burning,
  they gather at the Town Hall, and Hugin says so the first time.
- Each takes a free seat within 6 m of the fire, or his place on a ring round it, a metre from the next, facing it.
  Every other one sits on the ground (in rain all stand). Those standing raise a toast, laugh or cheer now and then,
  and they make evening small talk ("Good fire tonight.").
- At night they go indoors as before. A settler who stays out at night (no hut to go into) works through the evening.
- Setting `Colony.EveningGathering` (on).

## Keep in stock
- (0.21) Each building's **Keep in stock** list (see [Buildings](Buildings.md#keep-in-stock)) is what its chest keeps.
  Other settlers leave those items there: breakfast, meals, feeding fires and builders take only what's beyond the
  kept amount. The building's own worker uses all of it, and the Town Hall feeds newcomers from its own 10 food.
- **Hungry rather than not:** a settler whose meal is due eats spare food first; only when the colony has no other food
  does he eat kept food (the log says "… ate kept food: nothing else in the colony").
- **Carrying in free time:** a settler with nothing to do looks over the whole colony for a building short of a kept
  item and a chest that can spare it, takes up to 20 and brings them over (the nearest shortage first, from the chest
  that makes the shortest walk). One settler per building and item; it's part of free time, so not at night, and
  `Colony.FreeTime` off stops it too. Hover: "(carrying 10 Raspberries to the Town Hall)". Setting
  `Colony.CarryToStock` (on).

## Full chests
- (0.21) A lumberjack, forager or farmer whose hut chest is full takes his load to the Town Hall's chest, or the
  nearest colony chest with room, and goes back to work. Status: "Delivering (his chest is full)". He waits by his
  hut with "Storage full" only when every chest in the colony is full. The lumberjack keeps the seeds he holds for
  replanting. A settler without a job whose load won't fit in the Town Hall's chest takes it to another chest too.

## Keeping fires fed
- A settler in free time feeds a colony fire (campfire, hearth, bonfire) within 18 m of his hut (or the Town Hall)
  that is below half full: he takes its fuel (wood for most) from the nearest colony chest that has it, carries it there
  and puts it in, enough to take it past half. He never takes the last 10 of it from the colony's chests, nor what a
  building keeps (0.21), and only one settler goes to each fire. Hover: "(tending the fire)".
- Setting `Colony.TendFires` (on). It is part of free time, so `Colony.FreeTime` off stops it too.

## Night, attacks and raids
- **At night** settlers stop work and go into their hut through its door, which they shut behind them; hovering over
  one shows "Sleeping". A settler with a home lies down in his Longhouse bed and gets up beside it at dawn. The lumberjack delivers what he carries first; the builder puts his borrowed tool away and
  leaves his site till morning. At dawn they come out and carry on.
- **When a monster hunts them** they run into the nearest colony hut the monster isn't nearer to ("Sheltering") and
  come out 15 seconds after the last monster is gone. A monster that follows one inside makes him leave for another
  hut, or run.
- **During one of Valheim's raids** at the colony every settler stays indoors ("Sheltering") until it ends.
- They use their own hut when its building is finished and its door stands; otherwise (and without a job) the nearest
  such hut of the colony. Several settlers share a hut, standing by the chest on its door side, clear of the way in.
  A hut a settler can't get into within 45 seconds (its door blocked, or facing a cliff) is passed over for five minutes.
  Once inside, a settler never gives his hut up: if someone stands on his place, he stays where he is after a moment
  (not by the door).
- With no hut to go into, they behave as before: the lumberjack rests by his hut at night, the builder works on, and
  a settler a monster hunts runs to the Town Hall or his hut.
- Settings: `Colony.SettlersGoIndoorsAtNight` and `Colony.SettlersShelterInRaids` (both on).
