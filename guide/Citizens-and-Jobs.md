# Citizens and jobs

Citizens are vikings with random looks and Norse names. Hover one to see its name, job and status. A settler near you who needs something says so above their head ("Needs 12 Wood", "Storage full", "Can't reach the hut", "Hungry"; setting `Messages.WordsAboveHeads`), while plain work shows nothing. In their free time they greet you and make small talk (see "Free time").

**Jobless** citizens spend their free time near the camp. **No colony** means their camp was destroyed (it must be missing for about 30 seconds). Any Chieftain's Camp within 50 m adopts them, including a new one you build.

### Danger and healing

Players can't hurt citizens, but monsters can. A citizen who dies is gone (see "When a settler dies" below).

When a monster comes within 12 m (or a monster nearby is alerted or hunting), or hits them, citizens run to their Chieftain's Camp or hut (status "Fleeing", with a red "!" over their head). If the monster is by both, they run straight away from it. They go back to what they were doing once no monster has been near for 15 seconds. Deer, birds and sleeping or penned animals don't scare them.

Settlers stand up to weak animals (1.5.0). A weak creature that goes for a settler is fought off instead of fled from. They swing what's in their hands (a lumberjack's axe, a builder's pickaxe) or their fists, and the words over their head say "Fighting off a Neck". What counts as weak grows with the camp's level: Necks, Greylings and Boars always, Greydwarfs from level 2, Skeletons from level 3, those two with no star (1.6.1); the others with one star at most.

They still run when hurt to half, from anything stronger (a Troll, a Wolf, a Draugr), from a stone or an arrow thrown from afar, in a raid or while the alarm sounds, and a timid settler still runs. A settler who has run from the same kind three times in ten minutes stands their ground for the next ten. A brave settler also fights one going for someone right beside them. Once it's dead or gone they go back to work.

An animal they can't reach (in the water, up on a rock) they leave be while they keep working. They don't chase one far either: past about 8 m from where the fight began, or with no blow landing for a while, they let it go for a minute. At night, in a raid or in bed they don't go out to fight. Guards keep their own way of fighting. With the setting `Colony.SettlersFightBack` (on) turned off, settlers run from everything again, and the guards' driving off (below) stops too.

Every settler heals (1.5.0): a little every few seconds once nothing has hurt them for 20 seconds, and whole again after a night in bed.

Citizens jog like a player normally does and only sprint when fleeing.

### Doors, queues and getting unstuck

Settlers open closed doors on their way (doors inside their colony's area that the colony's owner may open: no key, no one else's ward), walk through, and close them behind them once they are 2 m past. A door they didn't open is left as it is, and a door is never closed on someone standing in the doorway. A chest behind a wall or a window isn't reached through it; they walk round and in. A settler whose way is cut off by a wall looks for a door near them straight away, instead of first walking to where the way ends.

Settlers going through the same door take turns. The others wait beside it, out of the way (or a few steps straight back from it, at a gate with walls on both sides), and two coming from opposite sides let one through first. Anyone standing in the doorway (a player, or a settler run by another computer in multiplayer) is waited for, up to 12 seconds. A door with a stair or a bump right in front of it is used from further out, at the stair's foot.

A settler whose walk doesn't move them (a log, a step, someone in the way) hops after three seconds and steps aside after five. They do this twice, then leave it to their job to find something else to do. One who keeps trying to walk for two minutes without getting out of a few metres of ground (boxed in by walls) is moved to a free spot by the camp, out of sight, when no player is within 30 m (after five minutes, whoever is near). That never happens at night or in a raid, and at most twice in ten minutes. Waiting somewhere on purpose doesn't count, and a monster in a doorway is never waited for.

The backstop (1.4) catches the rest. One who has wanted to be somewhere else for four minutes without getting more than 10 m from where it started is moved the same way, whatever held them up (a door tried again and again, a way that ends short, going to and fro round a small place they can't get out of).

A few special cases have their own rescue:

- A settler standing on a roof more than 1.5 m above the ground for 8 seconds is put back down by the camp (1.4). A step out of a door under a low eave can land them there.
- One who keeps burning where they stand for four seconds (squeezed between a wall and a fire) is moved to a spot by the camp clear of any fire, and the fire on them is put out (1.4).
- One who tries to walk for half a minute inside a hut without getting anywhere is moved to just inside its door, behind its walls, at any time (0.20). That's at most twice in ten minutes, counted with the rescue above.
- Inside a hut, which side of its door a settler is on comes from the hut's shape (0.20). Before 0.20 the game's walking map decided, and inside a hut turned off the compass it could be wrong, trapping its worker inside after they fetched from the chest. When the walking map gives them no way to the door from inside, or one that brings them no closer, they walk to it straight, hopping over a lip and stepping round the chest.

## Who they are

Each settler is good at one trade, their calling: woodcutting, building, foraging or farming. One in five is a jack of all trades. In its trade a settler works 20% faster (`Colony.CallingBonus`). A hut hires a jobless settler good at its trade first, and newcomers often bring the trade an empty hut needs.

Every settler also has a trait:

- Hardworking (10% faster) or lazy (10% slower; they'd rather sit, and tend the fires half as often).
- Cheerful or grumpy.
- Chatty (talks and chats twice as often) or quiet (never starts a chat, sits by the fire instead).
- Brave (runs only when a monster is within 9 m, or a strong one, like a Troll, within 12 m) or timid (runs from 20 m).

Each one has an origin too: "from the coast", "from a farm in the Meadows", "from over the mountains"… The Saga says so: "Day 12: Astrid came from the coast: a forager, cheerful."

Hover over a settler for a third line with their trait and trade ("Cheerful · good at foraging"). On the People tab, a settler not loaded on your computer shows their last status and "(far away)", or "(seen day 12)" when the colony last saw them on an earlier day. One not where they should be is Missing.

In the Chieftain's Camp, choose a settler on the People tab and their page says who they are, how long they've been here, where they sleep ("Home: Longhouse bed 2."), how they feel and why, their skills, what they carry and their newest lines in the Saga (1.5.1). The hut's window says when its worker is good at its trade: "Astrid (good at foraging): Picking".

Settlers dress by trade, in the game's own clothes:

- the jobless in rags
- lumberjacks in leather
- builders in leather with a cap
- farmers in rags and leather trousers
- foragers in rags and troll-hide trousers

The clothes give no armour, and they never go in their cairn.

Settlers from before 0.16 get a trade, trait and origin from who they are (always the same), and their days count from the day you first play 0.16.

## Free time

A settler with nothing to do spends free time within 15 m of their hut (the camp for the jobless). That means a jobless settler, or a worker whose job has nothing to do just now: "No trees nearby", "Crops growing", "Nothing to pick", or the builder's "No work". Every 30–90 seconds they pick one of these:

- They take a seat on any free piece you can sit on (bench, chair, stool, throne, a mod's seat), one near a burning fire first. They stay 40–90 seconds and now and then laugh or raise a toast. With a table pushed up to the seat, they sit down from across the table, as you can (never across a wall).
- They sit by a burning campfire, hearth or bonfire (not a torch), on the ground 2–3 m from it, facing it. A fire in the Mead Hall with a cooking station or cauldron over it is the cook's and doesn't count.
- They chat with another settler in free time within 20 m. They meet halfway, face each other and take turns talking with their hands.
- They stroll somewhere near, or sit down on the ground for a while.
- They take up a pastime (1.6), below.

### Pastimes (1.6)

Pastimes are fun in free time, mostly at things you build within 30 m of their hut (or of the camp, when it stands within 60 m). They keep at one for a minute or two. Nothing is made or hurt: practice shots and blows are for show, and nothing is left behind.

- Archery at an archery target (two at a time, standing 9 m off with a practice bow, no arrows).
- Practice at a training dummy (two at a time), with their tool or fists.
- A board game for two on a table with two chairs or more. At the end one cheers and the other shrugs.
- A toast for two to four standing round such a table.
- Dancing round a pole: a maypole, or a banner pole (a 4 m log pole with a banner hung near its top, like the camp's). Up to six can dance.
- A story at a burning fire: one tells it, one to three listen.
- Admiring a trophy on an item stand or an armour stand.
- The map table (one at a time).
- Stretching and sparring with another settler, anywhere; a nap in the open; petting one of the colony's tame animals.

In the evening some of those standing at the colony's fire dance for a while. In rain only pastimes under a roof go on (and stretching).

Each trait has a favourite, taken twice as often: lazy a nap, chatty a board game, brave sparring, timid the map table, hardworking archery, cheerful any dance, grumpy the dummy, quiet the trophies.

Pastimes count toward mood too. Three kinds of pastime in the last two days give "varied free time" (+5), four or more give +10, and doing their favourite today gives "did what they love" (+3).

Hover shows what they're up to: "Jobless (practising archery)", "Jobless (playing hnefatafl with Astrid)", "(listening to Ulf's story)". The setting `Colony.Pastimes` is on; with it off, free time is as before 1.6.

### Seats and going back to work

In rain or snow nobody sits on the open ground, but seats and fires with a roof over them are still used. A seat you sit or stand on is yours: settlers leave it, and get up if you sit down there. They get up and go the moment their job has work again, a monster comes, night falls or you recall them.

Hover over them to see what they're doing: "Crops growing (taking a seat)", "Jobless (talking with Bjorn)". A settler on the way to a hut far from you (not loaded on your computer) says "Heading to work".

The setting `Colony.FreeTime` turns free time off, and they wait standing, as before 0.14. Give them somewhere to go: a few benches and a fire near the camp and each hut. Hugin says so the first time a settler has free time with nothing to use.

### Greetings and small talk

The first time each day you come within 6 m of a settler, they say "Hail, <your name>!" (and wave, if they're in free time).

Settlers in free time within 10 m say things above their heads. A chatting pair takes turns; others say a line every few minutes. What they talk about follows the colony: a settler who died in the last two days, the weather, a newcomer or a new building today, a raid held off in the last two days, or their job's wait. After that come their own trade (the lumberjack's trees, the farmer's crops, the guard's watch), their temper (cheerful or grumpy), and a boss fallen in your world: the camp's saga tells when the colony hears of it, and they talk of it for two days (1.4.2). At a pastime they talk about it, half the time, after a death or hunger: "Bullseye!", "Your move, Astrid.", "Again!" (1.6).

A need ("Needs 12 Wood") always comes first. "Hungry" shows for a few seconds every half minute, with their talk in between, and their hover always says it. The setting `Messages.SmallTalk` is your own.

## Lumberjack

Lumberjacks work within 40 m of their hut (setting `Lumberjack.WorkRadius`; 10 m more per hut level, `Lumberjack.RadiusPerLevel`). They chop trees with the best axe their hut's level allows (a flint axe of their own, or a copy of a better one in the colony's chests), then the logs and stump, pick up wood and seeds, and deliver to the hut when carrying 50 items (`Lumberjack.CarryCapacity`) or at night. Their hover says what they are doing (1.4.2): "Felling trees", "Gathering wood", or "Keeping clear of falling logs" while a felled tree comes down.

They replant a sapling where the tree stood, using a dropped seed or one from the hut's storage, while a **Cultivator** is in the hut's storage or another of the colony's chests (`Lumberjack.Replant`, `Lumberjack.ReplantNeedsCultivator`). Without one, seeds are delivered.

The **Trees…** list in the hut's window (0.22) has a line per tree kind with **Fell** and **Replant** ticks. They fell only the kinds ticked Fell, and plant the kinds ticked Replant in turn, each only where it grows and when they have its seed, so the forest becomes mixed. A kind is greyed when their level's axe can't fell it ("needs a level 2 hut"), it has no sapling, or it doesn't grow where the hut stands. Every kind the hut allows starts ticked, and the hut remembers what you untick.

Trees by your buildings stay (0.22). Lumberjacks don't fell a tree whose trunk stands within 3 m of a piece a player built (`Lumberjack.LeaveTreesNearBuildings`; 0 = off), measured from any part of it (0.26: a long wall's ends too). Plants, crops and saplings don't count. The builder still clears trees from a building site.

With the hut's **Stop at** amount of Wood in the colony's chests (0.22), they plant what they hold, finish the tree they felled last (its wood, logs and stump; 0.26), deliver their load and rest ("Enough wood"). They start again below that amount.

They stand at the trunk or beside a log on the uphill side, never under it, and only swing when their axe reaches. Several lumberjacks share the work: each claims their tree, the logs and stump where it fell, and the wood they fetch.

They fell trees away from your buildings, the colony's huts and unfinished building sites, and leave trees standing when every direction would hit something. They finish the logs and stump of a tree they felled before the next one, even when they landed or rolled outside their work area.

After the blow that fells a tree they step back to the side, out of the trunk's line, and wait until the logs lie still before they walk up to them. They never start on a log that is still rolling. Settlers working within 25 m of a tree another settler fells wait for it too, and step out of the way of a log that rolls at them. Logs floating in water don't keep them waiting.

Lumberjacks have a **Woodcutting skill** like the player's. They start as strong as a new character and improve with practice, at a quarter of a player's pace per hit since they chop all day (`Colony.LearningRate`; Shift+E on the hut shows their level). See [Skills](#skills) for the other workers'.

Statuses: Working, Delivering, Delivering (the hut's chest is full), Planting, Resting (night), No trees nearby, Enough wood, Storage full.

## Farmer

Farmers work from a Farm, on the **fields** assigned to it (see [Buildings](Buildings.md#field-markers)). A Farm has no ground of its own (0.20.1, as in MineColonies), and with no field they say "Needs a field". They farm as a player does: they cultivate a plot (with a copy of a Cultivator in the Farm's chest or another of the colony's), plant a seed there (the field's crop, or the Farm's list's ticked crops in turn), pick what's ripe on their plots and carry the harvest home (up to 20 items).

They take seeds for every plot waiting for that crop at once (0.20), up to 20, and hold them apart from their harvest. What's left goes back in the chest when they deliver. A field set to one crop is sown whenever its seed is in the chest (the seed-crop limit below is the Farm's list's).

They deal with things in this order: night and danger as for everyone, a full load home, what they just picked, a ripe crop, planting an empty cultivated plot, and last cultivating a new one. With nothing to do they wait by the Farm: "Crops growing", "Needs seeds" or "Needs Cultivator" (also above their head when you're near).

A crop is theirs when it stands on one of their plots. They never touch crops elsewhere, so your own garden stays yours. Crops grow by the game's own rules (sun, room, the right biome): barley and flax only in the Plains. They plant each plot only with a crop that grows on that very spot (a Farm by a biome's edge has plots in two).

A seed crop (the carrot-seed crop: a carrot sown to grow carrot seeds) is sown only while fewer than 6 of the seed it gives are in the chest and their hands, so the harvest isn't all sown again. Food crops are always sown.

A plant on their plots that can't grow there (too cold, no room, under a roof) is cleared after a minute and a half, and they leave that plot for half an hour. A plot they can't cultivate, plant or get to they leave for ten minutes.

With PlantEverything, a berry bush, mushroom, thistle or dandelion that mod makes plantable is on the Farm's list, unticked until you tick it. Ticked, they take its price from the Farm's chest (5 raspberries for a raspberry bush), plant it on a free plot, pick it each time it's ripe and leave it there to grow back. It isn't planted again (see [Buildings](Buildings.md#farm)).

## Forager

Foragers work from a Forager's Hut. They walk to the nearest wild plant on their hut's list that's ready within their area (40 m around the hut, 10 m more per level), pick it as a player does, gather what drops and carry it home: up to 20 items, then they deliver to the hut's chest. With nothing ready they wait by the hut ("Nothing to pick") and look again every 10 seconds. Bushes grow back on their own, as in the game. Hungry, they pick at half speed.

They pick only what grows wild and grows back, and only the kinds ticked on the hut's **What to pick** list (everything but flint and branches to start): raspberries, blueberries, cloudberries, mushrooms, dandelions, thistles … The list comes from the game itself, so a kind a mod adds that grows back shows up too. Your planted crops (carrots, turnips, barley …) don't grow back once picked, so they never touch them, nor anything a player placed or that grows on cultivated ground. They also leave what never grows back (stones, wild seeds, the Mistlands mushrooms), or they would strip the land for good.

Flint and branches grow back too. They're on the list but unticked until you tick them, and their wood and flint can feed the builder. Food someone dropped by a bush stays too: they gather only what fell from the plant they picked.

Food goes to the colony, and what isn't food (dandelions, thistles) waits in their chest for you. When their chest is full they take their load to the camp's chest, or the nearest colony chest with room (0.21, see [Full chests](#full-chests)). What they bring home feeds the colony, since settlers eat from every colony chest. Newcomers need food in the camp's chest, so move some there. At dusk they deliver what they carry, then go indoors.

## Guard

Guards work from a Watchtower (1.1), up to three guards to a tower (1.2). They stand at their post by its door, looking out (a tower's second and third guards beside them), and every 2–4 minutes walk a round to a spot outside one of the colony's buildings within their patrol (25 m round the tower, 5 m more per level) and back ("On watch", "Patrolling").

They fight a monster within their patrol that comes within 30 m of a colony building, a settler or a player: one attacking someone of the colony first, else the nearest ("Fighting Greyling"). They walk up and swing their weapon (the game's own attack, as the lumberjack swings their axe) until it is dead. They never follow it further than their patrol + 10 m from their tower (`Guards.ChaseBeyondPatrol`). Past that (or running out so fast they would stop past it) they let it go and walk back. A monster they can't walk up to (in the water, flying, on a roof), or one that has left their watch and takes no blow from them for 15 seconds, they leave alone for a minute. Their swing hurts only what they aim at, never a wall, a crop or a tree beside it.

Guards also drive off weak monsters (1.5.0). A weak monster (as settlers count them, see above) stirred up inside the colony's area, up to 30 m past their patrol, is theirs too before it bites anyone ("Driving off Greyling"). A calm Boar grazing is left be. Turn it off with `Colony.SettlersFightBack`.

They answer calls for help (1.3). A monster attacking a settler or a player inside the colony's area (the monster or the one it attacks inside) brings the guards of every tower within 80 m (`Guards.HelpRadius`; at least twice their patrol), even past their patrol. For that fight the leash is the help radius + the chase limit.

A tower's orders (1.3) are rounds, or holding the post (where a manager put it, or by the tower). While the camp's **alarm** sounds they go where it was sounded, each guard of the colony to their own spot round it (3 m apart), and fight any monster within 30 m of it. A call for help within their help radius still brings them (1.4). Each takes the nearest open spot they can walk to (1.4.3), never one behind a wall, inside a fenced yard or by the colony's fire.

On watch with nothing to fight, guards keep the colony's ballistas within their patrol loaded (1.3). A ballista under half full gets what the colony's chests can spare of its ammunition (real items: the ballista uses them up), carried over by them ("Loading the ballista"). What's left goes back (with no room, it goes with their load to the Chieftain's Camp). They do this only on rounds: a guard holding a post, or at the alarm, leaves the ballistas be. A ballista never takes a settler for its target, nor (inside a colony's area) a player, and its bolts never hurt a settler. Setting `Guards.LoadBallistas`.

In a raid at the colony (1.3), the first guard to go for a raider calls out where they come from ("Ulf: raiders coming from the north-east!"). The monsters each guard killed are tallied on their tower's window and the camp's People tab (1.3).

Guards never target players, settlers, tames, the Dvergr and other neutral creatures, or animals (deer, boars, necks…), unless one is attacking someone of the colony. The animals you can tame (boars, wolves, lox…) count as animals here (1.6.1): a wolf that goes for a settler or a player is fought, and one wandering by is left alone until it does. A raid's wolves are always fought. An animal you are taming (fed recently, or its taming has begun) is left alone, even while it charges at you over the fence, and settlers get out of its way instead of swinging at it (1.6.1). Once it bites a settler or a player (out of its pen), it is fought like any other. The game's own rules also keep their swings off players, settlers and tames.

Their gear depends on their tower's **Role** (1.2). Like every worker's tools it is copies: the items stay in the chest, and a copy is of the first quality.

- A **warrior** takes the best melee weapon in their tower's chest (else the colony's other chests) and a shield with a one-handed weapon. They hold the shield up while a monster is near, when it starts a blow and a moment after each of theirs, and it blocks as a player's does. After three blocks within 3 seconds they lower it for a moment (they have no stamina to spend). They never go more than 2.5 seconds within reach without striking.
- An **archer** takes the best bow or crossbow that has its ammunition in the chests, and that ammunition (it is never used up). They shoot a monster they can see within 25 m, fully drawn (a crossbow loaded between shots), from where they stand. One they can't see (behind a wall, a rock) they walk towards until they can; one closer than 5 m makes them step back, and cornered they shoot anyway. An archer also shoots what a sword can't reach: a monster that swims or flies, or one standing up to 15 m above the ground (1.4.2). Without a bow and ammunition they fight with a melee weapon from the chests, if any.
- Armour is the best helmet, chest, legs and cape in the chests, worn in place of their trade's clothes. It protects them as a player's does (other settlers' work clothes are for looks).
- With nothing to fight with anywhere, they say "Needs a weapon in the Watchtower's chest" (an archer: "a bow and arrows"), and they are a settler like any other (they shelter, go in at night).

Below 30% health (`Guards.RetreatHealth`) a guard is off duty. A monster after them makes them shelter or run as anyone, and otherwise they go back to their tower and rest ("Resting (hurt)"), healing in about a minute. At 80% they are on watch again.

Armed, they stay out. At night, in a raid and when monsters come they keep watch while everyone else shelters. They skip the breakfast table and the evening fire (they still eat, from the colony's chests). In a raid at the colony they fight raiders 1.5 times as far out.

**Fighting** grows with every hit they land (arrows too) and makes their hits stronger (as Woodcutting makes the lumberjack's), at `Colony.LearningRate`. It makes them tougher too: half again their health at 100 (1.2).

Everyone in a colony with a guard on duty is glad of it ("+3 a guard on watch"; one without a weapon doesn't count). Being hit doesn't sadden a guard, since it is their work. A guard killed by a monster "fell defending the colony against Greydwarf" in the Saga, and a raid held off names the guards on duty.

With `Guards.Enabled` off, guards don't fight. A guard only stands by their tower, and shelters as anyone.

## Courier

Couriers work from the **Storehouse** (1.5): one at levels 1–2, two at 3–4, three at 5. The storehouse works out the colony's carrying every few seconds and hands each courier the most urgent thing nobody else is carrying, in this order:

1. Deliveries to a building short of its Keep in stock (the camp's food for newcomers too), and to the Builder's Hut for its builder's current order. These come from the storehouse first, else from another hut's spare, the shortest walk.
2. A producer three-quarters full (a Lumberjack's or Forager's Hut, a Farm). What it doesn't keep goes to the storehouse, so its worker never has to walk off with a full load.
3. The drop-off. What you put in the storehouse's own chest goes to a building short of it, and the rest into the chests inside.
4. Producers' surplus, the hut with the most first (at least 10 things).
5. Sorting, from level 3. A kind still kept in two chests inside (put there by you, or before a chest had room) ends in the one with the most of it.

Couriers never take what a building keeps (its Keep in stock), what its worker works with (a Farm's seeds for its fields, a lumberjack's 10 seeds of each kind they replant), what a hut's own open build order still needs (1.5.1), anything from the camp or a Builder's Hut, anything from a hut whose **Couriers take the rest** is off (its Keep in stock tab), or anything that doesn't stack (gear keeps its quality where it lies).

A storehouse being taken down is emptied first. Couriers carry what its chests inside hold to a building short of it, else the camp, else the nearest chest with room, and then a builder takes it down.

A trip is 50 things at a level-1 storehouse, 25 more each level, 150 at level 5 (settings `Courier.Carry` and `Courier.CarryPerLevel`). They walk to each chest they take from and each chest they put into, one after another, never reaching through a wall. What goes into the storehouse goes into its chests inside, never its own chest, so your drop-off stays free. At every level they put like with like: each kind goes into a chest inside that already holds it (the one with the most first; if you have that chest open, they wait), else into the nearest with room. What they can't put (a full chest, a building gone) goes back to the storehouse, else the camp.

Hover shows what they're doing: "Delivering (carrying 50 Wood to the Builder's Hut)", "Picking up (at the Farm)", "Sorting the storehouse", "Emptying the storehouse". With nothing to carry they say "Nothing to carry" and have free time by the storehouse. With their hands full and no chest with room (or none they can get to), they say "Nowhere to put what they carry", take no new task until they've put it away, and try again every minute. At dusk they put what they hold in the storehouse first.

Their skill is **Hauling**, and a higher one takes and puts faster.

Couriers on different computers never carry the same thing: the storehouse's owner hands out the tasks and they're saved on the storehouse. The storehouse's **Needs** tab shows who is carrying what to whom, and what nobody has (see [Buildings](Buildings.md#storehouse)).

## Cook

The cook works at the **Mead Hall** (1.6) and keeps a hot meal for every settler and two more in the hall's chest. They take the raw meat and fish the colony's chests can spare (never what a building keeps in stock, its working stock or what a hut's build order holds), the plainest first and a different kind when there's a choice. They carry up to 20 at a time (setting `Cook.CarryCapacity`), put them on a cooking station inside the hall, and take each piece off when it's done into the hall's chest. Once the chest holds enough, they rest by the hall.

A station only cooks over a burning fire. When it's out the cook feeds it with wood the colony can spare. With no wood they wait, and hovering over them says "The hearth is out: wood in the chests?". No food goes on a cold station. A fire that has wood and still won't burn (rain on the hearth, or the station not over its flames) isn't helped by more: the cook takes their wood back to the chest, puts raw food only on a station that burns, and says "No fire burns under the cooking station: is it over a hearth's flames, out of the rain?".

Food is never burnt. While the hall has a cook, a piece that's done waits on the station, at night or while the cook is away, until the cook takes it off. What the station drops when a piece comes off is picked up and taken to the hall's chest, never left on the floor. Every done piece comes off first, then it's one walk to the chest with them all.

Hover shows "Roasting Deer meat", "Fetching Deer meat", "Taking the cooked food off", "Needs raw food in the colony's chests", "Needs a cooking station in the Mead Hall", "The Mead Hall has hot food for everyone".

They learn **Cooking**, and a skill of 100 takes food on and off twice as fast as 0.

## Builder

The builder works from the Builder's Hut and takes one building at a time: the one you marked **Do first** in the camp's Work orders tab, then their own hut, then the oldest waiting one, and never one you **set aside** there. When you mark another order first they leave their site for it within seconds. A site that waits on you for a minute is set aside by them for five minutes while they work elsewhere.

Before building they prepare the site: pick up items, remove plants (picking berries and the like first), fell trees away from the site, chop logs and stumps, break rocks and take down leftovers of old colony buildings. Then they flatten the ground, to 30 cm under the floor for a design with posts (the natural ground for a raised hut), or to the floors' underside for a design without posts. What they gather goes to their hut.

Tools stay in the colony's chests. The builder works with a copy of the best axe, pickaxe and hoe there, and fetches stone for raising low ground. The hoe levels the ground; a pickaxe is only needed for rocks and for ground more than half a metre too high. If one is missing they say so ("Needs a pickaxe (Antler pickaxe or better)") and wait.

While building, they clear whatever grows or falls into the site. What they can't clear is named in the hut window but doesn't stop the building. They never reshape the ground right next to another building. They fell a tree from behind it, opposite the way it will fall, step clear after the blow and wait for the logs to settle, like the lumberjack. Dropped items on a new site are picked up only if they're plain (wood, stone, berries…); a player's own gear stays.

They fetch materials (their hut, the camp, then the other huts' storage), then work from spots just outside the building. They reach 15 m (setting `Builder.Reach`) and never go inside, so they can't shut themselves in. They check every piece with the game's support rule before placing it, lowest pieces first. A piece that falls is tried again later, and after three falls it is skipped. Materials from fallen pieces are picked up again (not those lying on a roof or a wall top, which are left for you).

With nothing to build they mend the colony's damaged buildings: any piece a builder put up (and the huts' own chests) below three quarters of its health (1.5.0). The worst-damaged building comes first, finished before the next, and in it the nearest piece first. One swing of their hammer mends it, as yours does, and costs nothing. A big repair, ten pieces of one building or more, goes in the Saga ("Ulf mended 14 pieces of the Longhouse"). A new order takes them away once the piece in hand is mended.

Every minute a finished colony building is checked against its design. When pieces of it are broken (a troll, a fire, a falling tree), its order reopens as a **repair** for those pieces only, at the same level. A builder takes it like any order, fetches the materials and puts them back, while the hut keeps working. Not during a raid there or with monsters by the hut: it waits until they're gone.

A piece you take away with your hammer is left out and never put back, so you can knock a doorway into a hut. So are pieces already missing when you first play 0.13, and a piece that falls again soon after it was put back three times. To stop a repair under way, press **Leave as it is** on it in the camp's Work tab. The setting `Builder.RebuildMissingPieces` turns putting back off.

Builders take huts down (0.23) when you ask on a hut's window: every piece from the top, with the materials going to their hut, and the hut's chest last (its contents to the camp). A take-down needs no site preparation. The status reads "Taking down <hut> (12 pieces left)".

Statuses: Building <hut> (12/29), Repairing <hut> (30/32), Taking down <hut>, Mending the <hut>, Fetching materials, Needs 6 Fine wood, Waiting for space, Can't reach the building site, Can't place: no support for <piece>, No work, Clearing the building site, Flattening the ground, Needs a pickaxe (Antler pickaxe or better).

Waiting for space (1.4) means someone stands where the next piece goes. After a few seconds a settler there is asked to make way (they walk out by the door and keep away for half a minute: "Making way for the builder"), and moved out if they stay. For a player or an animal the builder works on other pieces and tries that one again later.

## Skills

Every worker learns at their work, as a player does (0.22; in MineColonies, skills make them faster). The lumberjack learns **Woodcutting** (they chop harder), the farmer and the forager **Farming**, the builder **Crafting**, the guard **Fighting** (1.1: they hit harder), the courier **Hauling** (1.5: they take and put faster) and the cook **Cooking** (1.6: they take food on and off the station faster). Farming and Crafting make them faster: a skill of 100 works twice as fast as 0. Practice comes with every action that happened (a plot cultivated, planted or harvested, a pick, a piece built, mended or taken down; 0.26: not a failed try) at `Colony.LearningRate` (0.25 of a player's pace per action; it was `Lumberjack.LearningRate` before 0.22, and your value moves over).

Shift+E on their hut shows their skill ("Farming 12"), and the camp's People tab shows every skill they have when you choose them. A settler brought back keeps their skills.

## When a settler dies

Players in the colony's area (the camp's `ColonyRadius`) or within 50 m of the spot see "Ingrid the Lumberjack has died (hit by a falling tree)" in the middle of the screen and as a line in the chat. With `Messages.DeathMessage = ChatOnly` it shows only in the chat (each player's own setting).

The cause shown is one of these: killed by *a monster's name*, attacked (the attacker is gone), hit by a falling tree, crushed, fell from a height, drowned, burned, froze, poisoned, choked on smoke, shot, fell off the edge of the world, struck by lightning, unknown cause.

A settler who dies carrying anything leaves a cairn where they fell, holding what they carried. Hover over it for "Here lies Ingrid the Lumberjack: killed by Greydwarf, day 37". Open it with E, like a chest. Nothing can damage it, and once it's empty it crumbles away. Every player who got the death message has a pin "Ingrid's cairn" on the map, and it goes when you empty the cairn (or remove it by hand). Tools they had borrowed were copies, so the originals are still in the chests. A settler who carried nothing leaves no cairn.

The camp takes the settler off its list, and a hut with auto-hire hires the next jobless settler, as before.

The colony can remember everyone it has lost, with no limit, on a **Memorial stone** (1.5.1); the Saga keeps only its last 60 lines. Raise one from the hammer's Misc tab, one per colony, inside its area (20 Stone, `Memorial.StoneCost`). Hover over it for how many it remembers. Press E to read it, like a runestone: "Here the colony remembers: Ulf, Forager, day 39, killed by Greydwarf …", newest first, 20 a page (E again for the next). An older colony's stone starts with the deaths its Saga still holds. The words are kept on the stone too, so a camp that takes over a lost one gets them back.

The fallen can return (1.5.1), but it's off by default (`Colony.FallenReturn`, a server's choice). With it on, a settler who dies walks back in from the colony's edge a few days later (`Colony.FallenReturnDays`, 3), as themselves: their name, looks, trait, trade and skills, but not their home, their hut or what they carried (that's in their cairn). One comes back a day, the earliest death first, while the colony has room for another settler. Food, beds and mood don't hold them back. The Saga says "Day 42: Ulf returned from beyond the veil", the colony stops mourning them, and the memorial stone shows them greyed, "(returned on day 42)". A death while it was off stays final, even if you turn it on later. Their way back is kept by the camp: if the camp is lost (or taken down) before they return, they don't, though the memorial stone still names them.

Falling trees and rolling logs don't hurt settlers while `Colony.SettlersSafeFromTrees` is on (the default). They still hurt players.

## Homes and meals

Every bed in a Longhouse is a settler's home (see [Buildings](Buildings.md#longhouse)). At night a settler with a home lies down in their bed (`Colony.SleepInBeds`; off, they stand by it). They don't use a bed a player lies in, or one a player has claimed as their own (their spawn point); then they stand by it. One without a home sleeps in their workplace, as before.

After dawn, before work, each settler goes to breakfast at their own moment within the first minute, so they don't all crowd one chest. They walk to the colony chest that holds the food they'll eat (the nearest; the camp's when as near) and take one, each from a place of their own round the chest, a step apart (1.6.1). When every place is taken, the rest wait their turn a little further out. They eat it on a free seat within 8 m of that chest, or standing in their place by the chest. The hover reads "Eating (at breakfast)". If they can't get to the chest and take their food within a minute (a player has it open, no way there), they eat where they are.

They eat the plainest food there is that isn't what they had last time (when there's a choice), so raspberries and mushrooms go before cooked meat, meals vary, and your best food is left for you. The Mead Hall's hot food (its cook's roasts in its chest) comes first among what they haven't had lately (1.6), and breakfast is at its table when its chest has their food. With one kind of hot food they still eat varied meals. Hot food you keep elsewhere (your stews in the camp's chest) is just food: the plainest still goes first, so your best is left for you. Any food a player can eat counts; meads and potions don't.

Keep food you don't want eaten out of the colony's chests, or on a building's Keep in stock list (0.21: then it's eaten only when there's nothing else). Breakfast takes only food no building keeps. A table with benches by the camp makes a fine breakfast place.

A settler who finds nothing is hungry. Hovering over them says "Hungry", and they work at half speed (`Colony.HungryWorkSpeed`): they chop weaker and build slower. By day a hungry settler looks again every half minute, so food you put in a chest later is eaten the same day (1.4.2). Nobody starves or leaves. A new settler comes fed, so their first meal is due the next morning. Turn meals off with `Colony.SettlersEat`.

### Newcomers and walking in

Once a day, in daylight, a newcomer comes and eats that food (the plainest first), as long as the colony has a free bed (more Longhouse beds than settlers), at least 5 food in the camp's chest, and isn't unhappy (see [Mood](#mood)). That's one a day (`Colony.NewcomersPerDay`; one more for a joyful colony), up to 30 settlers (`Colony.MaxSettlers`). So build Longhouses, keep food in the camp and your settlers content, and the colony grows.

If every settler dies before the first Longhouse stands, nobody is left to build one and no newcomer has a bed to come to. So the morning after, new settlers walk in to start again, as many as a new camp gets (`Colony.StartingCitizens`), without needing food. The camp's window says so ("Next newcomer: nobody is left: new settlers come to start again the next morning"), and the saga tells it (1.6.1).

A newcomer appears at the edge of the colony and walks to the camp. They come from about 35 m out, on dry ground with a way in, where no player is looking (behind you, or past a wall or a hill), on the game's walkable ground (never inside a rock or under a floor). Only if every such spot is in view do they come into view, as far from every player as can be. With no way in, they appear by the camp.

Players in the colony are told "Astrid is coming to live in the colony: a forager from the coast." The hover reads "Arriving (from the coast)", and at the camp they wave. The first settlers of a new camp walk in together the same way. Setting `Colony.NewcomersWalkIn` (on).

## Mood

Each settler has a mood from 0 to 100. It starts at 50 (content), and each of these adds or takes away:

| Reason | Change |
|---|---|
| A home bed / no home | +5 / −15 |
| A cosy bed (the comfort around it, as for your own Rested: 4+ / 7+) | +5 / +10 |
| Ate today / hungry | +5 / −20 |
| Varied food: 3+ / 4+ different foods in their last 5 meals | +5 / +10 |
| The same food 5 meals running | −5 |
| A hot meal: their last meal was cooked (a Mead Hall cook's, 1.6), while they're fed | +5 |
| Last evening by a burning fire / with at least two others | +5 / +5 |
| Works in the trade they're good at | +5 |
| Jobless for 2 days or more | −5 |
| A settler of the colony died in the last 3 days | −10 |
| A monster hit them yesterday or today | −5 |
| A raid on the colony was held off with nobody lost (2 days) | +5 |
| Cheerful / grumpy | +10 / −10 |

| Mood | From | Work |
|---|---|---|
| Joyful | 75 | 15% faster |
| Content | 40 | as normal |
| Unhappy | 20 | 15% slower |
| Miserable | 0 | 30% slower |

Hover over a settler to see their mood ("Cheerful · good at foraging · Content"), or choose them in the camp's People tab: "Content (62): +5 home, +5 cosy bed, +5 ate, -10 Ingrid died". The Overview shows the colony's mood (the settlers' average) and the reasons that weigh most across it.

An unhappy settler says their worst reason now and then ("Nowhere to lay my head.", "Same food every day.", "We lost Ingrid."). Hugin explains mood the first time one is unhappy near you.

Nobody joins an unhappy colony ("Next newcomer: nobody wants to join an unhappy colony"), and a joyful one gets one more a day. Nobody leaves over it. A cosy Longhouse (a fire, rugs, a table), food of several kinds and an evening fire go a long way. The cheerful talk of good things, the grumpy grumble.

Mood is worked out once a minute. Turn it off with `Colony.Mood` (everyone content, newcomers as before).

## The evening

From 0.70 of the day (about a minute and a half before night), work stops the way it does at nightfall: the lumberjack delivers what they carry, the builder leaves their site. Then the settlers gather at the colony's fire: the burning campfire or hearth inside the colony nearest the camp (one under a roof first), never a hut's own hearth or a fire in the Mead Hall with a cooking station or cauldron over it (1.6: that one is the cook's). With no such fire burning, they gather at the camp, and Hugin says so the first time.

Each takes a free seat within 6 m of the fire, or their place on a ring round it, a metre from the next, facing it. Every other one sits on the ground (in rain all stand). Those standing raise a toast, laugh or cheer now and then, and they make evening small talk ("Good fire tonight."). At night they go indoors as before. A settler who stays out at night (no hut to go into) works through the evening. Setting `Colony.EveningGathering` (on).

## Keep in stock

Each building's **Keep in stock** list (0.21; see [Buildings](Buildings.md#keep-in-stock)) is what its chest keeps. Other settlers leave those items there: breakfast, meals, feeding fires and builders take only what's beyond the kept amount. The building's own worker uses all of it, and the camp feeds newcomers from its own 10 food.

A settler whose meal is due eats spare food first, and eats kept food only when the colony has no other food (the log says "… ate kept food: nothing else in the colony").

In free time, a settler with nothing to do looks over the whole colony for a building short of a kept item and a chest that can spare it, takes up to 20 and brings them over (the nearest shortage first, from the chest that makes the shortest walk). One settler goes per building and item. It's part of free time, so it doesn't happen at night, and `Colony.FreeTime` off stops it too. The hover reads "(carrying 10 Raspberries to the camp)". Setting `Colony.CarryToStock` (on).

Once the colony's storehouse has a courier (1.5), couriers carry it instead, with bigger loads, and settlers' free time goes back to resting, chatting and the fire.

## Full chests

A lumberjack, forager or farmer whose hut chest is full (0.21) takes their load to the camp's chest, or the nearest colony chest with room, and goes back to work. The status reads "Delivering (the hut's chest is full)". They wait by their hut with "Storage full" only when every chest in the colony is full. The lumberjack keeps the seeds they hold for replanting. A settler without a job whose load won't fit in the camp's chest takes it to another chest too.

## Keeping fires fed

A settler in free time feeds a colony fire (campfire, hearth, bonfire) within 18 m of their hut (or the camp) that is below half full. They take its fuel (wood for most) from the nearest colony chest that has it, carry it there and put it in, enough to take it past half. They never take the last 10 of it from the colony's chests, nor what a building keeps (0.21), and only one settler goes to each fire. The hover reads "(tending the fire)".

Setting `Colony.TendFires` (on). It is part of free time, so `Colony.FreeTime` off stops it too.

## Night, attacks and raids

At night settlers stop work and go into their hut through its door, which they shut behind them; hovering over one shows "Sleeping". A settler with a home lies down in their Longhouse bed and gets up beside it at dawn. The lumberjack delivers what they carry first, and the builder puts their borrowed tool away and leaves their site till morning. At dawn they come out and carry on.

When a monster hunts them they run into the nearest colony hut the monster isn't nearer to ("Sheltering") and come out 15 seconds after the last monster is gone. A monster that follows one inside makes them leave for another hut, or run, as does one hitting them through a back or side wall. If a monster is outside the door, reaching in (a Troll), they stay inside, since going out would be going into it, until they are hurt to half, when they run for it (1.5.1).

During one of Valheim's raids at the colony every settler stays indoors ("Sheltering") until it ends. An armed guard (1.1) does none of this: they stay out on watch, day and night, and fight (see [Guard](#guard)).

They use their own hut when its building is finished and its door stands; otherwise (and without a job) the nearest such hut of the colony. Several settlers share a hut, standing by the chest on its door side, clear of the way in. A hut a settler can't get into within 45 seconds (its door blocked, or facing a cliff) is passed over for five minutes. Once inside, a settler never gives their hut up: if someone stands on their place, they stay where they are after a moment (not by the door).

With no hut to go into, they behave as before: the lumberjack rests by their hut at night, the builder works on, and a settler a monster hunts runs to the camp or their hut.

Settings: `Colony.SettlersGoIndoorsAtNight` and `Colony.SettlersShelterInRaids` (both on).
