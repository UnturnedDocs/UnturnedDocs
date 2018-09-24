# SDG.Unturned.PlayerLife.lastRespawn

> This page is incomplete, please help finish it by contributing.

Gets the timestamp of the last respawn of the player.

```csharp
public float lastRespawn { get; }
```

### Returns:

Type | Description
------------ | -------------
[float](https://docs.microsoft.com/en-us/dotnet/api/system.single?view=netframework-3.5) | The timestamp of the last respawn of the player

### Exceptions:

Type | Description
------------ | -------------
[NullReferenceException](https://docs.microsoft.com/en-us/dotnet/api/system.nullreferenceexception?view=netframework-3.5) | Thrown when the player has not yet respawned

### Remarks:

This is not a system-time timestamp; moreover, this is the time since the server started to when the player last respawned.