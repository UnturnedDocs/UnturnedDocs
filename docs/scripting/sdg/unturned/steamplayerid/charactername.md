# SDG.Unturned.SteamPlayerID.characterName

The public name of the player's character that they connected to the server with.

```C#
public string characterName { get; set; }
```

### Returns:

Type | Description
------------ | -------------
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | The current character name or the streamer name if in streamer mode

### Example:

```C#
using SDG.Unturned;
using Steamworks;

public sealed class CommandListCharacterNames : Command
{
    public CommandListCharacterNames(Local local)
    {
		localization = local;
        _command = "listcharacternames";
        _info = "listcharacternames";
        _help = "Lists the players' steamID followed by their character name.";
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
            CommandWindow.Log($"{player.playerID.steamID.m_SteamID} : {player.playerID.characterName}");
    }
}
```