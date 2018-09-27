# SDG.Unturned.SteamPlayerID.nickname

> This member is client and server compatible.

The player's nickname.

```csharp
public string nickname;
```

### Returns:

Type | Description
------------ | -------------
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | The nickname of the player

### Example:

```csharp
using SDG.Unturned;
using Steamworks;

public sealed class CommandSetPlayerNickname : Command
{
    public CommandSetPlayerNickname(Local local)
    {
		localization = local;
        _command = "setplayernickname";
        _info = "setplayernickname [steamID]/[nickname]";
        _help = "Changes the nickname of the player.";
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
		
		string[] args = Parser.getComponentsFromSerial(parameter, '/');
		
		if (args.Length != 2 
			|| (!PlayerTool.tryGetSteamPlayer(args[0], out SteamPlayer player))
			|| (string.IsNullOrEmpty(args[1]))
		{
			CommandWindow.LogError(this.localization.format("InvalidParameterErrorText"));
			return;
		}

        player.playerID.nickname = args[1];
    }
}
```