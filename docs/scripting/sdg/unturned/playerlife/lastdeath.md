# SDG.Unturned.PlayerLife.lastDeath

<blockquote><p><b>This page is incomplete, please help finish it by contributing.<p></b></blockquote>

> This member is client and server compatible.

Gets the timestamp of the last death of the player.

```csharp
public float lastDeath { get; }
```

### Returns:

Type | Description
------------ | -------------
[float](https://docs.microsoft.com/en-us/dotnet/api/system.single?view=netframework-3.5) | The timestamp of the last death of the player

### Remarks:

This is not a system-time timestamp; moreover, this is the time since the server started to when the player last died or `0` if the player has not yet died.
