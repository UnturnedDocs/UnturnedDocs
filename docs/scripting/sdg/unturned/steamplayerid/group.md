# SDG.Unturned.SteamPlayerID.group

The group the player is currently in.

```c#
public CSteamID group;
```

### Returns:

Type | Description
------------ | -------------
[CSteamID](scripting/steamworks/csteamid) | The Steam64ID of the group

### Example:

```c#
using SDG.Unturned;
using Steamworks;

public sealed class CommandSetPlayerGroup : Command
{
    public CommandSetPlayerGroup(Local local)
    {
		localization = local;
        _command = "setplayergroup";
        _info = "setplayergroup [steamID]/[groupID]";
        _help = "Changes the group the player is currently in.";
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
			|| !ulong.TryParse(args[1], out ulong groupID))
		{
			CommandWindow.LogError(this.localization.format("InvalidParameterErrorText"));
			return;
		}

        player.playerID.group = new CSteamID(groupID);
    }
}
```