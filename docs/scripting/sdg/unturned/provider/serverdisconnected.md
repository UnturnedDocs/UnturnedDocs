# SDG.Unturned.Provider.ServerDisconnected

> This page is incomplete, please help finish it by contributing.

A delegate representing an action to be performed when a player leaves the server.

```csharp
public delegate void ServerDisconnected(CSteamID steamID)
```

### Parameters:

Type | Name | Description
------------ | ------------- | -------------
[CSteamID](scripting/steamworks/csteamid) | steamID | The ID of the player who left

### Remarks:

Remember that you can use [PlayerTool.getSteamPlayer(CSteamID)](scripting/sdg/unturned/playertool/getsteamplayer?id=sdgunturnedplayertoolgetsteamplayercsteamid) to get access to the player object instead of just an ID.