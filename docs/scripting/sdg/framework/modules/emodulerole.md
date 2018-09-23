# SDG.Framework.Modules.EModuleRole

> This page is incomplete, please help finish it by contributing.

The enum representing the role of a module.

```C#
public enum EModuleRole
```

### Values:

Name | Description
------------ | -------------
None | unknown
Client | The value when the module is designed to only work on the client
Server | The value when the module is designed to only work on the server
Both_Optional | The value when the module is designed to be optional on both the client or the server
Both_Required | The value when the module is designed to be required on all clients connecting to the server
