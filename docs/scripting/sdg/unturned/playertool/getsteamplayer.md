# SDG.Unturned.PlayerTool.getSteamPlayer

> This page is incomplete, please help finish it by contributing.

## Overloads:

Name | Description
------------ | -------------
[getSteamPlayer(CSteamID)](scripting/sdg/unturned/playertool/getsteamplayer?id=sdgunturnedplayertoolgetsteamplayercsteamid) | Finds a steam player using their [CSteamID](scripting/steamworks/csteamid)
[getSteamPlayer(string)](scripting/sdg/unturned/playertool/getsteamplayer?id=sdgunturnedplayertoolgetsteamplayerstring) | Finds a steam player using their name
[getSteamPlayer(ulong)](scripting/sdg/unturned/playertool/getsteamplayer?id=sdgunturnedplayertoolgetsteamplayerulong) | Finds a steam player using their ID as a [ulong](https://docs.microsoft.com/en-us/dotnet/api/system.uint64?view=netframework-3.5)

----

## SDG.Unturned.PlayerTool.getSteamPlayer(CSteamID)

Gets a Steam player using their [CSteamID](scripting/steamworks/csteamid).

```csharp
public static SteamPlayer getSteamPlayer(CSteamID steamID);
```

### Returns:

Type | Description
------------ | -------------
[SteamPlayer](scripting/sdg/unturned/steamplayer) | The Steam player object returned; if no player was found, this will return `null`

### Parameters:

Type | Name | Description
------------ | ------------- | -------------
[CSteamID](scripting/steamworks/csteamid) | steamID | The ID of the player you would like to find

----

## SDG.Unturned.PlayerTool.getSteamPlayer(string)

Gets a Steam player using their name.

```csharp
public static SteamPlayer getSteamPlayer(string name);
```

### Returns:

Type | Description
------------ | -------------
[SteamPlayer](scripting/sdg/unturned/steamplayer) | The Steam player object returned; if no player was found, this will return `null`

### Parameters:

Type | Name | Description
------------ | ------------- | -------------
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | name | The name of the player you would like to find

----

## SDG.Unturned.PlayerTool.getSteamPlayer(ulong)

Gets a Steam player using their ID.

```csharp
public static SteamPlayer getSteamPlayer(ulong steamID);
```

### Returns:

Type | Description
------------ | -------------
[SteamPlayer](scripting/sdg/unturned/steamplayer) | The Steam player object returned; if no player was found, this will return `null`

### Parameters:

Type | Name | Description
------------ | ------------- | -------------
[ulong](https://docs.microsoft.com/en-us/dotnet/api/system.uint64?view=netframework-3.5) | steamID | The ID of the player you would like to find