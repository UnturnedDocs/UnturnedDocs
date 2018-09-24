# SDG.Unturned.PlayerLife

> This page is incomplete, please help finish it by contributing.

The class holding fields relating to the life and health of a player.

```C#
public class PlayerLife : PlayerCaller
```

### Functions:

Name | Description
------------ | -------------
[askDamage(byte, Vector3, EDeathCause, ELimb, CSteamID, out EPlayerKill)](scripting/sdg/unturned/playerlife/askdamage) | Applies damage to the player and returns a death cause if applicable
[askDehydrate(byte)](scripting/sdg/unturned/playerlife/askdehydrate) | Subtracts a given amount of hydration from the player
[askDisinfect(byte)](scripting/sdg/unturned/playerlife/askdisinfect) | Subtracts a given amount of infection from the player (increases the value)
[askDrink(byte)](scripting/sdg/unturned/playerlife/askdrink) | Adds a given amount of hydration to the player
[askEat(byte)](scripting/sdg/unturned/playerlife/askeat) | Adds a given amount of food to the player
[askHeal(byte, bool, bool)](scripting/sdg/unturned/playerlife/askheal) | Adds health and/or repairs bleeding or broken bones
[askInfect(byte)](scripting/sdg/unturned/playerlife/askinfect) | Adds a given amount of infection to the player (decreases the value)
[askStarve(byte)](scripting/sdg/unturned/playerlife/askstarve) | Subtracts a given amount of food from the player
[breakLegs()](scripting/sdg/unturned/playerlife/breaklegs) | Breaks the player's legs

### Properties:

Name | Description
------------ | -------------
[food](scripting/sdg/unturned/playerlife/food) | Gets the current food stat of the player
[health](scripting/sdg/unturned/playerlife/health) | Gets the current health stat of the player
[isBleeding](scripting/sdg/unturned/playerlife/isbleeding) | Gets whether the player is bleeding or not
[isBroken](scripting/sdg/unturned/playerlife/isbroken) | Gets whether the player has broken legs or not
[isDead](scripting/sdg/unturned/playerlife/isdead) | Gets whether the player is dead or not
[lastDeath](scripting/sdg/unturned/playerlife/lastdeath) | Gets the timestamp of the last death of the player
[lastRespawn](scripting/sdg/unturned/playerlife/lastrespawn) | Gets the timestamp of the last respawn of the player
[oxygen](scripting/sdg/unturned/playerlife/oxygen) | Gets the current oxygen stat of the player
[player](scripting/sdg/unturned/playerlife/player) | Gets the player object this class is attached to
[stamina](scripting/sdg/unturned/playerlife/stamina) | Gets the current stamina stat of the player
[tempurature](scripting/sdg/unturned/playerlife/tempurature) | Gets the current tempurature status of the player
[virus](scripting/sdg/unturned/playerlife/virus) | Gets the current virus stat of the player
[warmth](scripting/sdg/unturned/playerlife/warmth) | Gets the current warmth stat of the player
[water](scripting/sdg/unturned/playerlife/water) | Gets the current water stat of the player