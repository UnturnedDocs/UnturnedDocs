# SDG.Unturned.PlayerTool.getSteamPlayer

> This page is incomplete, please help finish it by contributing.

## SDG.Unturned.PlayerTool.getSteamPlayer(CSteamID)

Gets a Steam player using their [CSteamID](scripting/steamworks/csteamid).

```csharp
public static SteamPlayer getSteamPlayer(CSteamID steamID)
```

### Returns

Type | Description
------------ | -------------
[SteamPlayer](scripting/sdg/unturned/steamplayer) | The Steam player object returned; if no player was found, this will return `null`

### Parameters:

Type | Name | Description
------------ | ------------- | -------------
[CSteamID](scripting/steamworks/csteamid) | steamID | The id of the player you would like to find

----

## SDG.Unturned.PlayerTool.getSteamPlayer(string)

Gets a Steam player using their name.

```csharp
public static SteamPlayer getSteamPlayer(string name)
```

### Returns

Type | Description
------------ | -------------
[SteamPlayer](scripting/sdg/unturned/steamplayer) | The Steam player object returned; if no player was found, this will return `null`

### Parameters:

Type | Name | Description
------------ | ------------- | -------------
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | name | The name of the player you would like to find