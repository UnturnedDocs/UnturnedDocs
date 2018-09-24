# SDG.Unturned.Provider

> This page is incomplete, please help finish it by contributing.

Serves as a central hub for most client/server functions.

```csharp
public class Provider : MonoBehaviour
```

### Functions:

Name | Description
------------ | -------------
[ban (CSteamID, string, uint)](scripting/sdg/unturned/provider/ban) | Bans a player from the game for a specified amount of time
[kick (CSteamID, string)](scripting/sdg/unturned/provider/kick) | Kicks a player from the game

### Properties:

Name | Description
------------ | -------------
[APP_VERSION](scripting/sdg/unturned/provider/app_version) | Gets the current version of Unturned the server is running
[clients](scripting/sdg/unturned/provider/clients) | Gets a list of all currently connected players
[maxPlayers](scripting/sdg/unturned/provider/maxplayers) | Gets or sets the maximum amount of players allowed to join
[serverName](scripting/sdg/unturned/provider/servername) | Gets or sets server's name
[serverPassword](scripting/sdg/unturned/provider/serverpassword) | Gets or sets the server's password
