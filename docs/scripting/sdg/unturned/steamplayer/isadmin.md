# SDG.Unturned.SteamPlayer.isAdmin

<blockquote><p><b>This page is incomplete, please help finish it by contributing.<p></b></blockquote>

> This member is client and server compatible.

Gets or sets the player's status as an admin.

```csharp
public bool isAdmin { get; set; }
```

### Returns:

Type | Description
------------ | -------------
[bool](https://docs.microsoft.com/en-us/dotnet/api/system.boolean?view=netframework-3.5) | Whether the player is an admin

### Remarks:
This will always return false on a client with streamer mode enabled, even if it's true.
