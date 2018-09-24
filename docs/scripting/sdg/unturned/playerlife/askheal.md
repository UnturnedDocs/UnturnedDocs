# SDG.Unturned.PlayerLife.askHeal(byte, bool, bool)

> This page is incomplete, please help finish it by contributing.

Adds some of the health stat to the player and/or repairs bleeding/broken legs.

If you want to damage the health stat, use [askDamage(byte, Vector3, EDeathCause, ELimb, CSteamID, out EPlayerKill)](scripting/sdg/unturned/playerlife/askdamage).

If you want damage the player's legs, use [breakLegs()](scripting/sdg/unturned/playerlife/breaklegs).

```C#
public void askHeal(byte amount, bool healBleeding, heal healBroken);
```

### Parameters:

Type | Name | Description
- | - | -
[byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte?view=netframework-3.5) | amount | The amount of the health stat to add
[bool](https://docs.microsoft.com/en-us/dotnet/api/system.boolean?view=netframework-3.5) | healBleeding | Whether or not to heal to stop the player from bleeding
[bool](https://docs.microsoft.com/en-us/dotnet/api/system.boolean?view=netframework-3.5) | healBroken | Whether or not to fix the player's legs