# Steamworks.CSteamID.m_SteamID

The `ulong` representation of a `CSteamID`.

```c#
public ulong m_SteamID;
```

### Examples:

```C#
using SDG.Unturned;
using Steamworks;

public sealed class CommandListIDs : Command
{
	public CommandListIDs()
	{
		_command = "listids";
		_info = "listids";
		_help = "Lists the players' names followed by their SteamID.";
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
			CommandWindow.Log($"{player.playerID.playerName} : {player.playerID.steamID.m_SteamID}");
	}
}
```
