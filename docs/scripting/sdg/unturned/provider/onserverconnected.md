# SDG.Unturned.Provider.onServerConnected

<blockquote><p><b>This page is incomplete, please help finish it by contributing.<p></b></blockquote>

> This is a server-only member!

A delegated call representing an action to be performed when a player joins the server.

```csharp
public static Provider.ServerConnected onServerConnected;
```

### Returns:

Type | Description
------------ | -------------
[Provider.ServerConnected](scripting/sdg/unturned/provider/serverconnected) | The delegate used in this call

### Remarks:

Remember that you can use [PlayerTool.getSteamPlayer(CSteamID)](scripting/sdg/unturned/playertool/getsteamplayer?id=sdgunturnedplayertoolgetsteamplayercsteamid) to get access to the player object instead of just an ID.