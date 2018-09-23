# SDG.Unturned.SteamPlayerID.streamerName

The name shown to clients when they are in streamer mode. The algorithm to calculate this is based on the player's [CSteamID](scripting/streamworks/csteamid).

```c#
public string streamerName { get; }
```

### Returns:

Type | Description
------------ | -------------
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | The steamer name of the player

### Remarks:

This is calculated using the following algorithm:

```c#
public string streamerName => 
	Provider.streamerNames[this.steamID.m_SteamID % Provider.streamerNames.Count];
```

### Example:

```c#
using SDG.Unturned;
using Steamworks;

public sealed class CommandListStreamerNames : Command
{
    public CommandListStreamerNames(Local local)
    {
		localization = local;
        _command = "liststreamernames";
        _info = "liststreamernames";
        _help = "Lists the players' steamID followed by their streamer name";
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
            CommandWindow.Log($"{player.playerID.steamID} : {player.playerID.steamID.streamerName}");
    }
}
```