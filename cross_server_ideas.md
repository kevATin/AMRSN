Ideas regarding coordination of multiple (unrelated) servers;

* simple central server, running on a RPi?
* main use is notifying online and offline players about what's happening on alti servers
* API for alti servers to hook into (also vanilla servers possible?)
* broadcasts all data to a website on the server, easily parse-able
* a bot that runs on the central server, nimbly account, dummy client possible so it doesn't waste resources? always online
* bot scans server list and forwards it to the server
* players can befriend the bot to receive in-game updates about other servers (player amount, map and game mode, score, etc)
* players can send specific commands to the bot to toggle notification settings (like frequency, etc)
* website shows server list
* website shows vapor/nimbly main server uptime status
* website shows player amount statistics (is this useful? https://altitudegame.com/genimg/playersToday.png )
* if vapor server appears to be offline send an alert to certain people so we can shout at the nimbly guys
* integration with other platforms? (steam, discord, whatsapp, telegram, sms?, email, matrix, etc)
* add those fancy website notifications
* website needs to work on mobile
* application to register custom URI on Linux, Windows, and macOS; altitude:IP:Port:[Password]:[special message that is sent to the main server upon connecting]
* has an index of all known servers; short "nicknames" can be defined for servers, if a server belongs to a group (like the 3 Official servers) then a name for the group is stored too, if a server is behind a lobby, then that lobby server is defined in the server index entry; settings to disregard either the lobby or the game server when it comes to notifications, or to show notifications for both regardless
* notification setting for minimum number of online players to notify
* notification setting for minimum time between individual notifications about the same server
* notification setting for minimum time between individual notifications about different servers

* player options: on website a player can enter their username/VaporID and request a passphrase; the bot then sends that player a message with a code if they're online; that code can then be entered on the website to enable the player to set up their notification settings in depth; could this also be used to allow custom settings for individual discord channels etc?

Custom data sent to the main server that the vapor server doesn't support:
* custom gamemode string, potentially only allow chosing from a pre-defined list
* 

Server Index Entry Data:
grouped by server group?
* server name
* server nickname
* server group (empty for none)
* server lobby (empty for none, multiple?)
* server location
* server owners
* password protection (empty for none, otherwise a sha-hash)
* locked (if the server is locked via xal's patch's whitelist; probably separate those from the main index)

Notification Formats:
* Standard: Alti:[servernickname]:[fullmapname]:[onlineplayers]
* Standard example: Alti:Off3:ball_planepark:7
Customizability:
* players can format the message themselves, including the Alti and the ":", etc
Variables:
* servername
* servernickname
* servergroup
* serverlobby
* gamemode
* fullmapname
* shortmapname (without the prefix)
* onlineplayers
* maxplayers
* ping (average ping of connected players?)

AltiArcade:
* a lobby server that players can idle in while waiting for other players
* has portals to all popular servers
* regularly broadcast the status of all connected servers in-game
