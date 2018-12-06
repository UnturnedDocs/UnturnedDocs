# SDG.Unturned.SteamPlayerID.streamerName

> This member is client and server compatible.

The name shown to clients when they are in streamer mode. The algorithm to calculate this is based on the player's [CSteamID](scripting/streamworks/csteamid).

```csharp
public string streamerName { get; }
```

### Returns:

Type | Description
------------ | -------------
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | The steamer name of the player

### Remarks:

This is calculated using the following algorithm:

```csharp
public string streamerName => 
	Provider.streamerNames[this.steamID.m_SteamID % Provider.streamerNames.Count];
```