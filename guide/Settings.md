# Settings

File: `BepInEx/config/daalmyte.vikingcolonies.cfg` (or press F1 with a configuration manager mod). On a server the
server's values are used by everyone.

| Section | Setting | Default | Range | Notes |
|---|---|---|---|---|
| Town Hall | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Town Hall | StoneCost | 10 | 0–500 | at once; on a server, the server's |
| Colony | StartingCitizens | 4 | 0–10 | citizens who arrive when a Town Hall is founded |
| Colony | ColonyRadius | 50 | 20–150 | metres around the Town Hall |
| Colony | SettlersSafeFromTrees | true | — | settlers aren't hurt by falling trees and rolling logs (players still are) |
| Colony | SettlersGoIndoorsAtNight | true | — | settlers stop work at night and sleep inside their huts |
| Colony | SettlersShelterInRaids | true | — | during a Valheim raid at the colony, settlers shelter inside their huts |
| Colony | SettlersEat | true | — | settlers eat one food item a day from the colony's chests; one who finds none is hungry |
| Colony | HungryWorkSpeed | 0.5 | 0.1–1 | how fast a hungry settler works (1 = as fast as a fed one) |
| Colony | NewcomersPerDay | 1 | 0–5 | newcomers who may arrive each day while there's a free bed and food; 0 = none |
| Colony | NewcomerFood | 5 | 0–50 | food items in the Town Hall's chest a newcomer needs and eats on arrival |
| Colony | MaxSettlers | 30 | 1–100 | no newcomers past this many settlers |
| Colony | EveningGathering | true | — | in the evening, before night, settlers stop work and gather round the colony's fire (the Town Hall with none) |
| Colony | SleepInBeds | true | — | at night a settler with a home lies in his Longhouse bed (off: he stands by it) |
| Colony | TendFires | true | — | settlers with nothing to do keep the colony's fires fed from its chests (always leaving 10 of the fuel) |
| Colony | LearningRate | 0.25 | 0.01–5 | practice per action at work (Woodcutting, Farming, Crafting) compared with a player's per hit (1 = as fast); was Lumberjack.LearningRate before 0.22 |
| Colony | CarryToStock | true | — | settlers with nothing to do carry what a building keeps in stock and lacks from chests that can spare it (off: kept items are still left alone) |
| Colony | NewcomersWalkIn | true | — | newcomers and the first settlers walk in from the edge of the colony (off: they appear at the Town Hall) |
| Colony | CallingBonus | 0.2 | 0–1 | how much faster a settler works in the trade he's good at (0.2 = 20% faster) |
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
| Farmer | CarryCapacity | 20 | 1–200 | items carried before delivering |
| Lumberjack | WorkRadius | 40 | 10–100 | metres around the hut |
| Lumberjack | RadiusPerLevel | 10 | 0–50 | metres added per hut level above 1 |
| Lumberjack | CarryCapacity | 50 | 1–500 | items carried before delivering |
| Lumberjack | Replant | true | — | plant saplings where trees were cut |
| Lumberjack | ReplantNeedsCultivator | true | — | replant only while a Cultivator is in the hut's storage |
| Lumberjack | LeaveTreesNearBuildings | 3 | 0–20 | metres round a piece a player built in which trees stay standing (0 = off) |
| Builder Hut | WoodCost | 20 | 0–500 | at once; on a server, the server's |
| Builder | Reach | 15 | 5–30 | metres he reaches from where he stands |
| Builder | SecondsPerPiece | 2 | 0.5–10 | hammer work per piece |
| Builder | CarryCapacity | 50 | 1–500 | items fetched per trip |
| Builder | RebuildMissingPieces | true | true/false | a finished colony building's gone pieces are put back by a builder |
| Storage | RowsPerLevel | 1 | 0–3 | rows added to a hut's chest per level above 1 (not the Town Hall's); never lower it on a world with upgraded huts: items in the rows it takes away may be lost |
| Placing | RaiseKey | PageUp | — | raise a hut 0.25 m while placing it (your own key, not the server's) |
| Placing | LowerKey | PageDown | — | lower a hut 0.25 m while placing it (your own key, not the server's) |
| Messages | DeathMessage | CentreAndChat | CentreAndChat, ChatOnly | how you're told a settler died (your own setting, not the server's) |
| Messages | HuginTips | true | — | Hugin explains the colony as you play, each tip once per character (with the game's tutorials on); your own setting |
| Messages | WordsAboveHeads | true | — | a settler near you who needs you says so above his head; your own setting |
| Messages | SmallTalk | true | — | settlers greet you once a day and make small talk above their heads in their free time (needs come first); your own setting |
| Developer | VerboseLog | false | — | write every settler's step to the log (for a bug report); always on in test worlds; your own setting |

The other Developer settings (`CommandFile`, `SkipIntro`, `AutoStartCharacter`, `AutoStartWorld`) are for testing the
mod; leave them off when playing.
