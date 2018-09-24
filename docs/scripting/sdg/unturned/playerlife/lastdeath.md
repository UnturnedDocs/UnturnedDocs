# SDG.Unturned.PlayerLife.lastDeath

> This page is incomplete, please help finish it by contributing.

Gets the timestamp of the last death of the player.

```csharp
public float lastDeath { get; }
```

### Returns:

Type | Description
------------ | -------------
[float](https://docs.microsoft.com/en-us/dotnet/api/system.single?view=netframework-3.5) | The timestamp of the last death of the player

### Exceptions:

Type | Description
------------ | -------------
[NullReferenceException](https://docs.microsoft.com/en-us/dotnet/api/system.nullreferenceexception?view=netframework-3.5) | Thrown when the player has not yet died

### Remarks:

This is not a system-time timestamp; moreover, this is the time since the server started to when the player last died.
