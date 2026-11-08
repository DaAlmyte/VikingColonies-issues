# Settings

The settings live in `BepInEx/config/daalmyte.vikingcolonies.cfg` (or press F1 with a configuration manager mod). On a
server, everyone uses the server's values.

Six of them are each player's own, and since 1.7.0 you can change them in the game: open the camp's window, go to The
camp tab and use the Your settings box under Keep in stock. Hugin's tips, words over heads and small talk are ticks. A
death and Language are buttons that show your choice, and a click goes to the next. Window size has − and + in steps
of 5%. A change is saved at once, and a server never changes these for you.

| Section | Setting | Default | Range | Notes |
|---|---|---|---|---|
| Town Hall | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Town Hall | StoneCost | 10 | 0–500 | at once; on a server, the server's |
| Town Hall | Levels | true | none | the camp has levels 1–5, raised with the Forsaken's trophies, and each one widens the colony (1.4); off: as before 1.4 (area `Colony.ColonyRadius`, settlers up to `Colony.MaxSettlers`, huts limited by the Builder's Hut only) |
| Town Hall | RadiusPerLevel | 10 | 0–50 | metres added to the colony's area per camp level above 1 |
| Town Hall | SettlersAtLevel1 | 10 | 1–100 | settlers a level-1 colony grows to (never past `Colony.MaxSettlers`) |
| Town Hall | SettlersPerLevel | 5 | 0–50 | more settlers per level above 1 |
| Town Hall | Level2Cost … Level5Cost | see [Buildings](Buildings.md#chieftains-camp) | text | materials the camp uses up from its chest when it is raised, written as `Prefab:count` separated by commas (e.g. `Wood:40, Stone:20, DeerHide:10`); empty: only the trophies |
| Town Hall | BeatenBossesCount | true | none | a Forsaken the world has already beaten counts as if its trophy were shown at the camp (a trophy on the sacrificial stones can't be taken back); off: only trophies shown at the camp count |
| Colony | StartingCitizens | 4 | 0–10 | citizens who arrive when a Chieftain's Camp is founded |
| Colony | ColonyRadius | 50 | 20–150 | metres around a level-1 Chieftain's Camp (more per level: `Town Hall.RadiusPerLevel`) |
| Colony | MaxReach | 150 | 50–500 | how far from the camp the colony's area may reach with its Watchtowers (1.1); of a tower near it only the part of its circle within reach counts |
| Colony | SettlersSafeFromTrees | true | none | settlers aren't hurt by falling trees and rolling logs (players still are) |
| Colony | SettlersGoIndoorsAtNight | true | none | settlers stop work at night and sleep inside their huts |
| Colony | SettlersFightBack | true | none | settlers fight off a weak creature that goes for them (Necks, Greylings, Boars; Greydwarfs and Skeletons as the camp grows) and run only when hurt, and guards drive a weak monster out of the colony before it bites; off: settlers run from everything and guards wait for an attack, as before 1.5.0 |
| Colony | SettlersShelterInRaids | true | none | during a Valheim raid at the colony, settlers shelter inside their huts |
| Colony | SettlersEat | true | none | settlers eat one food item a day from the colony's chests; one who finds none is hungry |
| Colony | HungryWorkSpeed | 0.5 | 0.1–1 | how fast a hungry settler works (1 = as fast as a fed one) |
| Colony | NewcomersPerDay | 1 | 0–5 | newcomers who may arrive each day while there's a free bed and food; 0 = none |
| Colony | NewcomerFood | 5 | 0–50 | food items in the camp's chest a newcomer needs and eats on arrival |
| Colony | MaxSettlers | 30 | 1–100 | no newcomers past this many settlers, whatever the camp's level |
| Colony | FallenReturn | false | none | dead settlers come back at the camp after a few days, with their name, trait, trade and skills (1.5.1); off: death is final. Only a settler who died while it was on comes back |
| Colony | FallenReturnDays | 3 | 0–30 | with `Colony.FallenReturn` on: the days before they walk back in, one a day, in daylight, while the colony has room for another settler; 0: the same day |
| Colony | EveningGathering | true | none | in the evening, before night, settlers stop work and gather round the colony's fire (the camp with none) |
| Colony | SleepInBeds | true | none | at night a settler with a home lies in their Longhouse bed (off: they stand by it) |
| Colony | TendFires | true | none | settlers with nothing to do keep the colony's fires fed from its chests (always leaving 10 of the fuel) |
| Colony | LearningRate | 0.25 | 0.01–5 | practice per action at work (Woodcutting, Farming, Crafting, Fighting) compared with a player's per hit (1 = as fast); was Lumberjack.LearningRate before 0.22 |
| Colony | CarryToStock | true | none | settlers with nothing to do carry what a building keeps in stock and lacks from chests that can spare it (off: kept items are still left alone) |
| Colony | NewcomersWalkIn | true | none | newcomers and the first settlers walk in from the edge of the colony (off: they appear at the camp) |
| Colony | Pastimes | true | none | in free time settlers also take pastimes: archery, the training dummy, board games and toasts at a table, dancing round a banner pole or maypole, stories at a fire, trophies, the map table, stretching, sparring, naps, petting tame animals (1.6); on a server, the server's; off: free time as before 1.6 |
| Colony | CallingBonus | 0.2 | 0–1 | how much faster a settler works in the trade they're good at (0.2 = 20% faster) |
| Colony | Mood | true | none | settlers have a mood that speeds or slows their work and decides whether newcomers come (off: everyone content) |
| Colony | FreeTime | true | none | settlers with nothing to do sit on seats, sit by fires, chat and stroll near their hut or the camp; off: they wait standing |
| Colony | TownHallGraceDays | 3 | 0–10 | in-game days a colony lives on after losing its camp (a new one raised among its huts takes it over); 0 = it ends 30 seconds after |
| Lumberjack Hut | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Longhouse | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Forager Hut | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Forager | WorkRadius | 40 | 10–100 | metres around the hut |
| Forager | RadiusPerLevel | 10 | 0–50 | metres added per hut level above 1 |
| Forager | CarryCapacity | 20 | 1–200 | items carried before delivering |
| Farm | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Field | WoodCost | 4 | 0–500 | a field marker's cost; at once; on a server, the server's |
| Memorial | StoneCost | 20 | 0–500 | a memorial stone's cost; at once; on a server, the server's (1.5.1) |
| Watchtower | WoodCost | 20 | 0–500 | at once; on a server, the server's (1.1) |
| Storehouse | WoodCost | 20 | 0–500 | at once; on a server, the server's (1.5) |
| Courier | Carry | 50 | 1–500 | what a courier carries a trip at a level-1 storehouse; on a server, the server's (1.5) |
| Courier | CarryPerLevel | 25 | 0–500 | how many more a trip for each storehouse level above 1; on a server, the server's (1.5) |
| Mead Hall | WoodCost | 20 | 0–500 | at once; on a server, the server's (1.6) |
| Cook | CarryCapacity | 20 | 1–100 | how much raw food the Mead Hall's cook carries to the cooking station at once; on a server, the server's (1.6) |
| Cook | ReserveDays | 2 | 0–10 | days of the settlers' meals the Mead Hall's Kitchen list never uses: the cook makes your dishes only from the food beyond this (0: nothing kept back); on a server, the server's (1.7) |
| Guards | Enabled | true | none | Watchtower guards fight monsters near the colony; off: a guard shelters like any settler (1.1) |
| Guards | ChaseBeyondPatrol | 10 | 0–50 | metres past their patrol a guard follows a monster before letting it go |
| Guards | RetreatHealth | 0.3 | 0–0.75 | below this share of their health a guard goes back to their tower to heal (out again at 80%) |
| Guards | HelpRadius | 80 | 0–300 | how far from their tower a guard comes when a monster attacks someone inside the colony's area (at least twice their patrol; 1.3) |
| Guards | LoadBallistas | true | none | guards on watch keep the colony's ballistas in their patrol loaded from what the chests can spare (1.3) |
| Watchtower | StopsSpawns | true | none | no monsters spring up within a finished Watchtower's circle, as by a workbench or a fire (1.3) |
| Farmer | CarryCapacity | 20 | 1–200 | items carried before delivering |
| Lumberjack | WorkRadius | 40 | 10–100 | metres around the hut |
| Lumberjack | RadiusPerLevel | 10 | 0–50 | metres added per hut level above 1 |
| Lumberjack | CarryCapacity | 50 | 1–500 | items carried before delivering |
| Lumberjack | Replant | true | none | plant saplings where trees were cut |
| Lumberjack | ReplantNeedsCultivator | true | none | replant only while a Cultivator is in the hut's storage or another of the colony's chests |
| Lumberjack | LeaveTreesNearBuildings | 3 | 0–20 | metres round a piece a player built in which trees stay standing (0 = off) |
| Builder Hut | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Builder | Reach | 15 | 5–30 | metres the builder reaches from where they stand |
| Builder | SecondsPerPiece | 2 | 0.5–10 | hammer work per piece |
| Builder | CarryCapacity | 50 | 1–500 | items fetched per trip |
| Builder | RebuildMissingPieces | true | true/false | a finished colony building's gone pieces are put back by a builder |
| Storage | RowsPerLevel | 1 | 0–3 | rows added to a hut's chest per level above 1 (the camp's too since 1.4); never lower it on a world with upgraded huts: items in the rows it takes away may be lost |
| Placing | RaiseKey | PageUp | none | raise a hut 0.25 m while placing it (your own key, not the server's) |
| Placing | LowerKey | PageDown | none | lower a hut 0.25 m while placing it (your own key, not the server's) |
| Creative | CreativeMode | Auto | Auto, Off | creative mode (1.5): Auto turns it on in a world with No build cost and for an admin with debug mode's free building (B); Off never; on a server, the server's |
| Creative | LevelUpKey | Equals (=) | none | in creative, one level higher for the colony building you're placing (your own key) |
| Creative | LevelDownKey | Minus (-) | none | in creative, one level lower, down to "the builder builds it" (your own key) |
| Messages | DeathMessage | CentreAndChat | CentreAndChat, ChatOnly | how you're told a settler died (your own setting, not the server's) |
| Messages | HuginTips | true | none | Hugin explains the colony as you play, each tip once per character (with the game's raven hints on: Settings, "Enable raven hints"); your own setting |
| Messages | AskForFeedback | true | none | once on this computer, at a good moment, a small window asks what you think of the mod and links to its Discord and GitHub (nothing is sent from the game); off: it never asks, and the camp's Feedback button stays; on a server, the server's setting |
| Messages | WordsAboveHeads | true | none | a settler near you who needs you says so above their head; your own setting |
| Windows | Scale | 1.0 | 0.75–1.5 | the size of VikingColonies' windows on your screen (1.5.1); a window too tall for the screen is made to fit; your own setting |
| Messages | SmallTalk | true | none | settlers greet you once a day and make small talk above their heads in their free time (needs come first); your own setting |
| Messages | Language | Game | Game, English, or the name of your own file's language | the language of the mod's words (1.7.0): Game follows Valheim's; English keeps the mod in English whatever the game is set to; see [Your own words](#your-own-words) below; your own setting |
| Developer | VerboseLog | false | none | write every settler's step to the log (for a bug report); always on in test worlds; your own setting |

The other Developer settings (`CommandFile`, `SkipIntro`, `AutoStartCharacter`, `AutoStartWorld`, `TestFrameCap`) are for testing
the mod. Leave them off when playing.

## Your own words

The mod speaks English for now. Since 1.7.0 you can change any of its words, or put the whole mod in your language, with
a file of your own. Updates never touch it.

1. Open your profile's folder (r2modman: Settings, Browse profile folder) and make the folder
   `BepInEx/config/VikingColonies/Translations`.
2. In it, make a file named after the language your Valheim is set to, by Valheim's English name for it: `German.json`,
   `Russian.json`, `French.json`. Save it as UTF-8.
3. Put in the lines you want to change, copied from the mod's English file (`translations/English.json` on the
   [issues page](https://github.com/DaAlmyte/VikingColonies-issues)) and with your words after the colon:

   ```json
   {
     "vc_tab_people": "Leute",
     "vc_close": "Schließen"
   }
   ```

4. Start the game. The log (`BepInEx/LogOutput.log`) has a line for your file each time the game sets up its language:
   how many of its lines the mod took, and which it left out and why.

Keep each `{0}`, `{1}` and `<color=...>` of the English line in yours, in any order: the game fills them in. In a line
with them, a `{` or `}` of your own is written twice (`{{`). A line without them is left out, so the game never shows a wrong number, and the English one shows instead. Every line you
leave out stays English too. Only the mod's own words (the keys starting `vc_`) can be changed this way.

With Messages.Language set to English the mod stays English whatever the game is set to. Set it to your file's name
(`French`) to see your file while the game is in another language.

A file you'd like everyone to have is welcome on the [issues page](https://github.com/DaAlmyte/VikingColonies-issues)
or on Discord.
