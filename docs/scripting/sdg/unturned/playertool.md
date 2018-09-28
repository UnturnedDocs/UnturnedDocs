# SDG.Unturned.PlayerTool

> This page is incomplete, please help finish it by contributing.

This is a utility class containing many static methods allowing the easy conversion of player IDs into `SteamPlayer` or `Player` objects.

```csharp
public class PlayerTool
```

### Static Universal Functions:

Name | Description
------------ | -------------
[getPlayer(CSteamID)](scripting/sdg/unturned/playertool/getplayer?id=sdgunturnedplayertoolgetplayercsteamid) | Finds a player using their [CSteamID](scripting/steamworks/csteamid)
[getPlayer(string)](scripting/sdg/unturned/playertool/getplayer?id=sdgunturnedplayertoolgetplayerstring) | Finds a player using their name
[getSteamPlayer(CSteamID)](scripting/sdg/unturned/playertool/getsteamplayer?id=sdgunturnedplayertoolgetsteamplayercsteamid) | Finds a steam player using their [CSteamID](scripting/steamworks/csteamid)
[getSteamPlayer(string)](scripting/sdg/unturned/playertool/getsteamplayer?id=sdgunturnedplayertoolgetsteamplayerstring) | Finds a steam player using their name
[getSteamPlayer(ulong)](scripting/sdg/unturned/playertool/getsteamplayer?id=sdgunturnedplayertoolgetsteamplayerulong) | Finds a steam player using their ID as a [ulong](https://docs.microsoft.com/en-us/dotnet/api/system.uint64?view=netframework-3.5)