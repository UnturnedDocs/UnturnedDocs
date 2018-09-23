# SDG.Unturned.Provider.kick(CSteamID, string)

Kicks a player from the game.

```C#
public static void kick (CSteamID steamID, string reason);
```

### Parameters:

Type | Name | Description
------------ | ------------- | -------------
[CSteamID](scripting/steamworks/csteamid) | steamID | The id of the user to kick
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | reason | The reason displayed to the user after they have been kicked

### Example:

```C#
using SDG.Unturned;
using Steamworks;

public sealed class CommandKickAll : Command
{
	public CommandKickAll()
	{
		_command = "kickall";
		_info = "KickAll [reason]";
		_help = "Kicks all players except the caller from the server.";
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
		
		if (string.IsNullOrEmpty(reason))
			reason = "You have been kicked from the server.";
		
		foreach (SteamPlayer player in Provider.clients)
		{
			CSteamID id = player.playerID.steamID;
			
			if (id == caller)
				continue;
				
			Provider.kick(id, reason);
		}
	}
}
```