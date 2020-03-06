# JAR-mod wishlist:
* ability to set weapon mode per player (and bot)
* ability to set health per player (and bot)
* ability to set gravity per player (and bot; potential issues with projectiles?)

# Powerups:
powerup texture/selector: health (always for autouse), shield, missile, wall, bomb, demolition charge, ball;  
can be set for a specific team or neutral  
can be set to spawn at round start  
respawn time can be set  
multiple powerup types can be defined for one powerup (ideally not randomized but instead using different vanilla powerup types to distinguish between them; add map legend type description next to powerups)  
* Health: autouse, health,
* Shield: pickup, shield,
* Missile: pickup missile,
* Wall: pickup, wall,
* Ball: pickup, ball,
* Bomb_team: pickup, bomb,
* Bomb_neutral: pickup
* Demolition Charge: pickup
* Key_personal_autouse: autouse
* Key_personal_pickup: pickup
* Key_team_autouse: autouse
* Key_team_pickup: pickup
* Flag: autouse, health,
* KotH_Flag: autouse, health
* Checkpoint_personal: autouse
* Checkpoint_team: autouse
* Ball Reset_autouse:
* Ball Reset_pickup:
* Genocide_own team_autouse:
* Genocide_own team_pickup:
* Genocide_other teams_autouse:
* Genocide_other teams_pickup:
* Genocide_color_autouse: color can be any team color, also allow arrays?
* Genocide_color_pickup: color can be any team color, also allow arrays?
* Suicide_autouse:
* Suicide_pickup:
* Omnicide_autouse:
* Omnicide_pickup:
* Small Increase Time_autouse:
* Small Increase Time_pickup:
* Medium Increase Time_autouse:
* Medium Increase Time_pickup:
* Big Increase Time_autouse:
* Big Increase Time_pickup:
* Small Decrease Time_autouse:
* Small Decrease Time_pickup:
* Medium Decrease Time_autouse:
* Medium Decrease Time_pickup:
* Big Decrease Time_autouse:
* Big Decrease Time_pickup:

activation requirements:
* empty green perk
* empty blue perk
* certain superpowers can only be used with special autouse or pickup powerups (usage or carrying)
* use primary weapon
* use secondary weapon
* warmup
* cooldown
* ammunition, max uses per life? restocking?

* Brain's shockwave, different intensities?
* Brain's rumble, different intensities?
* Brain's gravity inversion
* Slippery Floor
* Suicide, instantly kills player upon usage, may be useful on coop maps with bouncy walls where self kills aren't quickly do-able, if possible it shouldn't give your last attacker a kill so it can be used to avoid giving the enemy veteran bars
* Boost, similar to the miranda dash, but for every plane and can't skip through walls, useful for escaping stalling
* Ninja teleport, got the idea while watching some newbies with bad ping skip around the map, requires jar modding or packet filter firewall,

Ideally superpowers should work consistently across maps and servers, with the same requirements;
unlock on per player basis on my mmorpg, available for all in standard gamemodes?
command to equip, can be set to be useable by player or only by server eg when executing via powerup collection
Superpowers:
* Ball Reset:
* Small Boost:
* Medium Boost:
* Big Boost: any plane, any red perk, no green perk, no blue perk, warmup 5s, cooldown 20s, using secondary attack when ready activates the ability, using secondary attack during warmup or cooldown works as normal
* Suicide: any plane, any red perk, either green or blue perk has to be empty (or both), 
