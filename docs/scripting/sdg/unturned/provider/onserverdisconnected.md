# SDG.Unturned.Provider.onServerDisconnected

> This page is incomplete, please help finish it by contributing.

A delegated call representing an action to be performed when a player leaves the server.

```csharp
public static Provider.ServerDisconnected onServerDisconnected;
```

### Returns:

Type | Description
------------ | -------------
[Provider.ServerDisconnected](scripting/sdg/unturned/provider/serverdisconnected) | The delegate used in this call

### Remarks:

Remember that you can use [PlayerTool.getSteamPlayer(CSteamID)](scripting/sdg/unturned/playertool/getsteamplayer?id=sdgunturnedplayertoolgetsteamplayercsteamid) to get access to the player object instead of just an ID.