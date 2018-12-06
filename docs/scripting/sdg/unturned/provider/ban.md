# SDG.Unturned.Provider.ban(CSteamID, string, uint)

> This is a server-only member!

Kicks a player from the game. 

This DOES NOT perform a ban on the player, this just informs the player that they have been banned and must be used in conjunction with [SteamBlacklist.ban](scripting/sdg/unturned/steamblacklist/ban) in-order to issue a ban to the player.

```csharp
public static void ban (CSteamID steamID, string reason, uint duration);
```

### Parameters:

Type | Name | Description
------------ | ------------- | -------------
[CSteamID](scripting/steamworks/csteamid) | steamID | The id of the user to ban
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | reason | The reason displayed to the user after they have been banned
[ulong](https://docs.microsoft.com/en-us/dotnet/api/system.uint64?view=netframework-3.5) | reason | The time in seconds the ban will last