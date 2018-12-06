# Steamworks.CSteamID

> This page is incomplete, please help finish it by contributing.

The interop structure for the native representation of a Steam64ID;

```csharp
[Serializable, StructLayout(LayoutKind.Sequential, Pack = 4)]
public struct CSteamID : IEquatable<CSteamID>, IComparable<CSteamID>
```

### Fields:

Name | Description
------------ | -------------
[m_SteamID](scripting/steamworks/csteamid/m_steamid) | The [ulong](https://docs.microsoft.com/en-us/dotnet/api/system.uint64?view=netframework-3.5) representation of this ID.
