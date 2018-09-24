# SDG.Unturned.PlayerLife.askDamage(byte, Vector3, EDeathCause, ELimb, CSteamID, out EPlayerKill)

> This page is incomplete, please help finish it by contributing.

Applies damage to the player and outputs [EPlayerKill.PLAYER](scripting/sdg/unturned/eplayerkill) if the player is killed.

If you want to heal the player, use [askHeal(byte, bool, bool)](scripting/sdg/unturned/playerlife/askheal).

If you want damage the player's legs, use [breakLegs()](scripting/sdg/unturned/playerlife/breaklegs).

```C#
public void askDamage(byte amount, Vector3 newRagdoll, EDeathCause newCause, ELimb newLimb, CSteamID newKiller, out EPlayerKill kill);
```

### Parameters:

Type | Name | Description
- | - | -
[byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte?view=netframework-3.5) | amount | The amount of the health stat to subtract
[Vector3](https://docs.unity3d.com/550/Documentation/ScriptReference/Vector3.html) | newRagdoll | The direction and power to propel ragdoll if a death event is triggered
[EDeathCause](scripting/sdg/unturned/edeathcause) | newCause | The cause value returned if a death event is triggered
[ELimb](scripting/sdg/unturned/elimb) | elimb | The limb value returned if a death event is triggered
[CSteamID](scripting/steamworks/csteamid) | newKiller | The Steam64ID of the killer returned if a death event is triggered
out [EPlayerKill](scripting/sdg/unturned/eplayerkill) | kill | [EPlayerKill.PLAYER](scripting/sdg/unturned/eplayerkill) if the player was killed, else [EPlayerKill.NONE](scripting/sdg/unturned/eplayerkill)