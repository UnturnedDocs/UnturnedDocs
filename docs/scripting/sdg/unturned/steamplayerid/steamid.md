# SDG.Unturned.SteamPlayerID.steamID

> This member is client and server compatible.

The ID of the Steam account bound to this player.

```csharp
public string steamID { get; }
```

### Returns:

Type | Description
------------ | -------------
[CSteamID](scripting/steamworks/csteamid) | The Steam64ID of the player

### Example:

```csharp
using SDG.Unturned;
using Steamworks;

public sealed class CommandListSteamIDs : Command
{
    public CommandListSteamIDs(Local local)
    {
		localization = local;
        _command = "liststeamids";
        _info = "liststeamids";
        _help = "Lists the players' steamID followed by their Steam name";
    }

    protected override void execute(CSteamID caller, string parameters)
    {
        if (!Dedicator.isDedicated)
            return;

        if (!Provider.isServer)
        {
            CommandWindow.LogError(this.localization.format("NotRunningErrorText"));
            return;
        }

        foreach (SteamPlayer player in Provider.clients)
            CommandWindow.Log($"{player.playerID.steamID} : {player.playerID.steamID.playerName}");
    }
}
```