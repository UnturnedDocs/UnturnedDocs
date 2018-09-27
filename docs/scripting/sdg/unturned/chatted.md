# SDG.Unturned.Chatted

> This page is incomplete, please help finish it by contributing.

A delegate representing an action to be performed when a player chats.

```csharp
public delegate void Chatted(SteamPlayer player, EChatMode mode, ref Color chatted, ref bool isRich, string text, ref bool isVisible)
```

### Parameters:

Type | Name | Description
------------ | ------------- | -------------
[SteamPlayer](scripting/sdg/unturned/steamplayer) | player | The player who chatted
[EChatMode](scripting/sdg/unturned/echatmode) | player | The chatmode of the message
ref [Color](https://docs.unity3d.com/550/Documentation/ScriptReference/Color.html) | chatted | The color of the message to be sent
ref [bool](https://docs.microsoft.com/en-us/dotnet/api/system.boolean?view=netframework-3.5) | isRich | Whether any present [rich text](https://docs.unity3d.com/550/Documentation/Manual/StyledText.html) should be formatted
[string](https://docs.microsoft.com/en-us/dotnet/api/system.string?view=netframework-3.5) | text | The text to be displayed
ref [bool](https://docs.microsoft.com/en-us/dotnet/api/system.boolean?view=netframework-3.5) | isVisible | Should the message be sent or not