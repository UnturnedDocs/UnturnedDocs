# SDG.Unturned.PlayerLife.lastRespawn

<blockquote><p><b>This page is incomplete, please help finish it by contributing.<p></b></blockquote>

> This member is client and server compatible.

Gets the timestamp of the last respawn of the player.

```csharp
public float lastRespawn { get; }
```

### Returns:

Type | Description
------------ | -------------
[float](https://docs.microsoft.com/en-us/dotnet/api/system.single?view=netframework-3.5) | The timestamp of the last respawn of the player

### Remarks:

This is not a system-time timestamp; moreover, this is the time since the server started to when the player last respawned or `0` if the player has not yet respawned.