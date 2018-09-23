# SDG.Unturned.SteamPlayerID.playerName

The name of the Steam account bound to this player.

```c#
public string playerName { get; }
```

### Returns:

Type | Description
------------ | -------------
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | The Steam name of the player

### Example:

```c#
using SDG.Unturned;
using Steamworks;

public sealed class CommandListSteamNames : Command
{
    public CommandListSteamNames(Local local)
    {
		localization = local;
        _command = "liststeamnames";
        _info = "liststeamnames";
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