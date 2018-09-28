# SDG.Unturned.Provider

> This page is incomplete, please help finish it by contributing.

Serves as a central hub for most client/server functions.

```csharp
public class Provider : MonoBehaviour
```

### Static Server Functions:

Name | Description
------------ | -------------
[ban (CSteamID, string, uint)](scripting/sdg/unturned/provider/ban) | Bans a player from the game for a specified amount of time
[kick (CSteamID, string)](scripting/sdg/unturned/provider/kick) | Kicks a player from the game

### Static Universal Properties:

Name | Description
------------ | -------------
[APP_VERSION](scripting/sdg/unturned/provider/app_version) | Gets the current version of Unturned the server is running
[clients](scripting/sdg/unturned/provider/clients) | Gets a list of all currently connected players

### Static Server Properties:

Name | Description
------------ | -------------
[maxPlayers](scripting/sdg/unturned/provider/maxplayers) | Gets or sets the maximum amount of players allowed to join
[serverName](scripting/sdg/unturned/provider/servername) | Gets or sets server's name
[serverPassword](scripting/sdg/unturned/provider/serverpassword) | Gets or sets the server's password

### Static Server Events:

Name | Description
------------ | -------------
[onServerConnected](scripting/sdg/unturned/provider/onserverconnected) | An event called on the server when a player joins
[onServerDisconnected](scripting/sdg/unturned/provider/onserverdisconnected) | An event called on the server when a player leaves

### Delegates:

Name | Description
------------ | -------------
[ServerConnected (CSteamID)](scripting/sdg/unturned/provider/serverconnected) | A delegate representing an action to be performed when a player joins the server
[ServerDisconnected (CSteamID)](scripting/sdg/unturned/provider/serverdisconnected) | A delegate representing an action to be performed when a player joins the server