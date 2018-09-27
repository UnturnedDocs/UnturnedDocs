# SDG.Unturned.Provider.ban(CSteamID, string, uint)

> This is a server-only member!

Bans a player from the game for a specified amout of time.

```csharp
public static void ban (CSteamID steamID, string reason, uint duration);
```

### Parameters:

Type | Name | Description
------------ | ------------- | -------------
[CSteamID](scripting/steamworks/csteamid) | steamID | The id of the user to ban
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | reason | The reason displayed to the user after they have been banned
[ulong](https://docs.microsoft.com/en-us/dotnet/api/system.uint64?view=netframework-3.5) | reason | The time in seconds the ban will last

### Example:

```csharp
using SDG.Framework.Modules;
using SDG.Unturned;
using Steamworks;

public sealed class ProfanityNameBan : IModuleNexus
{
	public void initialize()
	{
		Provider.OnServerConnected += CheckProfanity;
	}
	
	public void shutdown()
	{
		Provider.OnServerConnected -= CheckProfanity;
	}
	
	private void CheckProfanity(CSteamID steamID)
	{
		SteamPlayer player = PlayerTool.getSteamPlayer(steamID);
		
		foreach (string word in ProfanityFilter.getCurseWords())
		{
			if (player.playerID.characterName.Contains(word))
			{
				Provider.ban(steamID, "You were banned because of a curse word in your name.", uint.MaxValue);
				CommandWindow.Log($"{player.playerID.m_SteamID} was banned because of a curse word in their name. ({player.playerID.characterName})");
			}
		}
	}
}
```