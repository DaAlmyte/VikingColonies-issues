# Settings

File: `BepInEx/config/daalmyte.vikingcolonies.cfg` (or press F1 with a configuration manager mod). On a server the
server's values are used by everyone.

| Section | Setting | Default | Range | Notes |
|---|---|---|---|---|
| Town Hall | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Town Hall | StoneCost | 10 | 0–500 | at once; on a server, the server's |
| Town Hall | Levels | true | — | the Town Hall has levels 1–5, raised with the Forsaken's trophies, each widening the colony (1.4); off: as before 1.4 (area `Colony.ColonyRadius`, settlers up to `Colony.MaxSettlers`, huts limited by the Builder's Hut only) |
| Town Hall | RadiusPerLevel | 10 | 0–50 | metres added to the colony's area per Town Hall level above 1 |
| Town Hall | SettlersAtLevel1 | 10 | 1–100 | settlers a level-1 colony grows to (never past `Colony.MaxSettlers`) |
| Town Hall | SettlersPerLevel | 5 | 0–50 | more settlers per level above 1 |
| Town Hall | Level2Cost … Level5Cost | see [Buildings](Buildings.md#town-hall) | text | materials raising the hall uses up from its chest, as `Prefab:count` by commas (e.g. `Wood:40, Stone:20, DeerHide:10`); empty: only the trophies |
| Town Hall | BeatenBossesCount | true | — | a Forsaken the world has already beaten counts as if its trophy were shown at the hall (a trophy on the sacrificial stones can't be taken back); off: only trophies shown at the hall |
| Colony | StartingCitizens | 4 | 0–10 | citizens who arrive when a Town Hall is founded |
| Colony | ColonyRadius | 50 | 20–150 | metres around a level-1 Town Hall (more per level: `Town Hall.RadiusPerLevel`) |
| Colony | MaxReach | 150 | 50–500 | how far from the Town Hall the colony's area may reach with its Watchtowers (1.1); of a tower near it only the part of its circle within reach counts |
| Colony | SettlersSafeFromTrees | true | — | settlers aren't hurt by falling trees and rolling logs (players still are) |
| Colony | SettlersGoIndoorsAtNight | true | — | settlers stop work at night and sleep inside their huts |
| Colony | SettlersShelterInRaids | true | — | during a Valheim raid at the colony, settlers shelter inside their huts |
| Colony | SettlersEat | true | — | settlers eat one food item a day from the colony's chests; one who finds none is hungry |
| Colony | HungryWorkSpeed | 0.5 | 0.1–1 | how fast a hungry settler works (1 = as fast as a fed one) |
| Colony | NewcomersPerDay | 1 | 0–5 | newcomers who may arrive each day while there's a free bed and food; 0 = none |
| Colony | NewcomerFood | 5 | 0–50 | food items in the Town Hall's chest a newcomer needs and eats on arrival |
| Colony | MaxSettlers | 30 | 1–100 | no newcomers past this many settlers, whatever the Town Hall's level |
| Colony | EveningGathering | true | — | in the evening, before night, settlers stop work and gather round the colony's fire (the Town Hall with none) |
| Colony | SleepInBeds | true | — | at night a settler with a home lies in their Longhouse bed (off: they stand by it) |
| Colony | TendFires | true | — | settlers with nothing to do keep the colony's fires fed from its chests (always leaving 10 of the fuel) |
| Colony | LearningRate | 0.25 | 0.01–5 | practice per action at work (Woodcutting, Farming, Crafting, Fighting) compared with a player's per hit (1 = as fast); was Lumberjack.LearningRate before 0.22 |
| Colony | CarryToStock | true | — | settlers with nothing to do carry what a building keeps in stock and lacks from chests that can spare it (off: kept items are still left alone) |
| Colony | NewcomersWalkIn | true | — | newcomers and the first settlers walk in from the edge of the colony (off: they appear at the Town Hall) |
| Colony | CallingBonus | 0.2 | 0–1 | how much faster a settler works in the trade they're good at (0.2 = 20% faster) |
| Colony | Mood | true | — | settlers have a mood that speeds or slows their work and decides whether newcomers come (off: everyone content) |
| Colony | FreeTime | true | — | settlers with nothing to do sit on seats, sit by fires, chat and stroll near their hut or the Town Hall; off: they wait standing |
| Colony | TownHallGraceDays | 3 | 0–10 | in-game days a colony lives on after losing its Town Hall (a new one built among its huts takes it over); 0 = it ends 30 seconds after |
| Lumberjack Hut | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Longhouse | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Forager Hut | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Forager | WorkRadius | 40 | 10–100 | metres around the hut |
| Forager | RadiusPerLevel | 10 | 0–50 | metres added per hut level above 1 |
| Forager | CarryCapacity | 20 | 1–200 | items carried before delivering |
| Farm | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Field | WoodCost | 4 | 0–500 | a field marker's cost; at once; on a server, the server's |
| Watchtower | WoodCost | 20 | 0–500 | at once; on a server, the server's (1.1) |
| Guards | Enabled | true | — | Watchtower guards fight monsters near the colony; off: a guard shelters like any settler (1.1) |
| Guards | ChaseBeyondPatrol | 10 | 0–50 | metres past their patrol a guard follows a monster before letting it go |
| Guards | RetreatHealth | 0.3 | 0–0.75 | below this share of their health a guard goes back to their tower to heal (out again at 80%) |
| Guards | HelpRadius | 80 | 0–300 | how far from their tower a guard comes when a monster attacks someone inside the colony's area (at least twice their patrol; 1.3) |
| Guards | LoadBallistas | true | — | guards on watch keep the colony's ballistas in their patrol loaded from what the chests can spare (1.3) |
| Watchtower | StopsSpawns | true | — | no monsters spring up within a finished Watchtower's circle, as by a workbench or a fire (1.3) |
| Farmer | CarryCapacity | 20 | 1–200 | items carried before delivering |
| Lumberjack | WorkRadius | 40 | 10–100 | metres around the hut |
| Lumberjack | RadiusPerLevel | 10 | 0–50 | metres added per hut level above 1 |
| Lumberjack | CarryCapacity | 50 | 1–500 | items carried before delivering |
| Lumberjack | Replant | true | — | plant saplings where trees were cut |
| Lumberjack | ReplantNeedsCultivator | true | — | replant only while a Cultivator is in the hut's storage or another of the colony's chests |
| Lumberjack | LeaveTreesNearBuildings | 3 | 0–20 | metres round a piece a player built in which trees stay standing (0 = off) |
| Builder Hut | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Builder | Reach | 15 | 5–30 | metres the builder reaches from where they stand |
| Builder | SecondsPerPiece | 2 | 0.5–10 | hammer work per piece |
| Builder | CarryCapacity | 50 | 1–500 | items fetched per trip |
| Builder | RebuildMissingPieces | true | true/false | a finished colony building's gone pieces are put back by a builder |
| Storage | RowsPerLevel | 1 | 0–3 | rows added to a hut's chest per level above 1 (the Town Hall's too since 1.4); never lower it on a world with upgraded huts: items in the rows it takes away may be lost |
| Placing | RaiseKey | PageUp | — | raise a hut 0.25 m while placing it (your own key, not the server's) |
| Placing | LowerKey | PageDown | — | lower a hut 0.25 m while placing it (your own key, not the server's) |
| Messages | DeathMessage | CentreAndChat | CentreAndChat, ChatOnly | how you're told a settler died (your own setting, not the server's) |
| Messages | HuginTips | true | — | Hugin explains the colony as you play, each tip once per character (with the game's tutorials on); your own setting |
| Messages | WordsAboveHeads | true | — | a settler near you who needs you says so above their head; your own setting |
| Messages | SmallTalk | true | — | settlers greet you once a day and make small talk above their heads in their free time (needs come first); your own setting |
| Developer | VerboseLog | false | — | write every settler's step to the log (for a bug report); always on in test worlds; your own setting |

The other Developer settings (`CommandFile`, `SkipIntro`, `AutoStartCharacter`, `AutoStartWorld`) are for testing the
mod; leave them off when playing.
