# Multiplayer

- Every player and the server need VikingColonies and Jotunn, with the same first two numbers of VikingColonies'
  version. 1.4.2 and 1.4.3 play together, but a 1.5 player can't join a 1.4 server (on a crossplay server, check the
  versions yourselves).
- Crossplay works for players on PC who have the mod. They join with the join code (tested on a dedicated server with
  1.4.3). Players on Xbox or PlayStation can't install mods, so they can't use the colony.
- Make sure everyone has the mod. On a crossplay server the game doesn't check it for you; without crossplay it turns
  away a player with no mods, saying "Incompatible version". A player without the mod gets in but can't see the camp or
  the settlers, and settlers near only that player may stop working.
- A join code only exists while crossplay is on, and it changes each time the server starts. It needs no router setup.
  Without crossplay, join with **Join IP** (the server's address and port, usually 2456), from the server list, or, for
  a world a Steam friend hosts from the menu, from the **Friends** tab. A dedicated server in your home, joined by
  address, needs UDP ports 2456–2458 open on the router for friends outside the house.
- If you use r2modman or the Thunderstore app, start the game from it (Start modded). Started straight from Steam it
  has no mods, and a server without crossplay turns you away with "Incompatible version".
- Citizens and buildings are saved with the world and look the same for everyone.
- The server's settings count. The colony buildings' costs, and every other colony setting marked as synced, come from
  the server when you join it, and the hammer asks the server's cost at once. In a world of your own you get your own
  again.
- The colony's mood, and each settler's mood and its reasons, read the same on every computer.
- Only the player who built a colony's camp, and the players they put on one of their wards covering the hut, can
  manage that colony. They alone can hire, fire, switch auto-hire, change the replanting list, order a building or an
  upgrade, or cancel one, or place a new hut in the colony. For everyone else those buttons are greyed out (and a new
  hut's outline is red) with the reason. Anyone may look. Valheim remembers who built every Chieftain's Camp, so this
  holds for colonies built before 0.4 too. The camp's builder adds the friends who share the colony to a ward (Guard
  stone) covering the huts. If that player has left the server for good, nobody else can manage the colony.
- Every request is checked by the computer that controls the building, so two players pressing buttons at once can't
  clash, and a refused request tells the player who asked.
- Settlers hand chests over like players do. The computer that has a hut chest sends its latest contents first, and
  the settler's computer reloads them before changing the chest, so what a friend just put in or took out is kept.
  While a friend has a hut chest open, a settler who needs it waits by it until it's closed.
- Hiring, firing and joining a colony are applied by the computer that runs the citizen, which checks the citizen is
  still free first, so two huts can't hire the same citizen.
- A building has to be missing for about 30 seconds before citizens treat it as destroyed, so a player still loading
  into a big base doesn't make anyone lose their colony or job.
- When a Chieftain's Camp is lost, each hut and each settler notices on its own (on the computer that runs it) and
  keeps the colony for the grace days (`Colony.TownHallGraceDays`, shared from the server). The huts remember who built
  the Chieftain's Camp, so the same players may still manage them and the settlers still open the colony's doors. A new
  camp takes the colony over from the huts and settlers the placing player's computer has loaded, and whoever builds it
  is the colony's owner from then on.
- Settlers left behind (1.7.0) are handled by the server (or the player hosting), which sees every settler, loaded or
  not. Once a minute it sends the ones whose camp is gone on to their owner's newest camp, never to a friend's camp. A
  settler someone is near is asked on that player's computer and walks. One nobody is near is changed by the server and
  turns up at the camp's edge when the walk's time is over. They're moved, never copied. The camp's builder is told
  once, if online: "3 settlers left behind at your old camp are on their way to your new one."
- Send away (1.7.0) goes like this. The camp's computer checks the request (who may manage the colony), the server
  finds the settler wherever they are and asks the computer that runs them, and that computer hands their load back to
  the camp's chest.
- The computer that ran the settler raises the cairn, once. Every player told of the death gets their own map pin, and
  a player's pin goes when that player empties the cairn. Whoever opens the cairn takes it over, like any chest.
- Settlers run by one computer take turns at a door. A settler waits up to 12 seconds for anyone else standing in the
  doorway (a player, or a settler run by another computer).
- The computer that controls a finished hut checks it against its design every minute. A piece any player removes with
  the hammer is left out for everyone, and only players who may manage the colony can press Leave as it is.
- A hut is built from the designs saved on the computer that runs it when its building or upgrade is ordered (for a new
  hut, the player who placed it), and the order keeps that design. The hut window's upgrade line shows the viewer's own
  designs' cost. A design one player saved with `vc_blueprint save` is used on others' computers only if they have a
  copy of it in their own designs folder.
- A citizen keeps working when you're away only while someone is near it (Valheim only runs areas near players).
