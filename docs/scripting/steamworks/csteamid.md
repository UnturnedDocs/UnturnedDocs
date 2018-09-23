# Steamworks.CSteamID

The interop structure for the native representation of a Steam64ID;

```C#
[Serializable, StructLayout(System.Runtime.InteropServices.LayoutKind.Sequential, Pack = 4)]
public struct CSteamID : System.IEquatable<CSteamID>, System.IComparable<CSteamID>
```

### Fields:

Name | Description
------------ | -------------
[m_SteamID](scripting/steamworks/csteamid/m_steamid) | The `ulong` representation of a `CSteamID`.
