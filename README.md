# AMRSN
Altitude MMORPG Server Network; an MMORPG-like experience realized within Altitude, using alti+server and a patched game jar

# Server Coordination:
The MMORPG consists of multiple interconnected servers each running their own dedicated map.

Every server but mmorpg_lobby is whitelisted via xal's patch, and prevents every player from joining by default. In addition every server but mmorpg_lobby is in LAN mode so that the server list isn't spammed with dozens of servers that can't be joined anyways.

The lobby server acts as the gateway to the game; every player has to join it every time they connect to the server network.

From mmorpg_lobby to the game:

1. Player moves to the Join Game portal to initiate the teleport.
2. The server checks for the last server/map the player was located on. If this is their first join, their spawn location is mmorpg_overworld_center_city inside the spawn building.
3. The server checks if that server is online.
4. The server checks for their last location on that server and sets the player's spawn point.
5. The lobby server runs "/xx add allow VaporID" on the target server.
6. The lobby server runs "/serverRequestPlayerChangeServer PlayerName {CurrentIP}:{ServerPort} to transfer the player.
7. The player is NOT de-whitelisted on the lobby server.

From one non-lobby server to another:

1. Player moves to a certain location on a map or initiates a teleport some other way.
2. Server checks if target server is online.
3. "/xx add allow VaporID" is run on the destination server.
4. "/serverRequestPlayerChangeServer PlayerName {CurrentIP}:{ServerPort}" is run on the current server.
6. "/xx remove allow VaporID" is run on the previous server.
7. Once the player disconnects, they are automatically de-whitelisted, so that they can only join the lobby server at their next join

# Player Spawning Mechanic:

A player's default spawn is in the center city. Other, alternative spawns, are in the norther, southern, western, and eastern cities. Players can change their spawn points by unlocking them via quests and then paying coins at the spawn location of their choice. 

These spawn points are only used when a player has died; when joining a server they spawn at their last location.

# Database:

A central database for the mmorpg will hold the following entries:
* VaporID
* UserName
* LastMap
* LastLocationX
* LastLocationY
* CurrentPlane
* CurrentColor
* CurrentRedPerk
* CurrentGreenPerk
* CurrentBluePerk
* Spawn
* Level
* Coins
* UnlockedPerks

Player location has to be logged at least once every second, ideally less.
