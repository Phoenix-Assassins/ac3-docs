# OverlordCoreProtocol

| Method ID | Method Name                   |
| --------- | ----------------------------- |
| 1         | [GetSettings](#1-getsettings) |

# (1) GetSettings

## Request
This method does not take any parameters.
## Response
| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[OverlordProperty](#overlordproperty-structure)> | settings |

# Types

## OverlordProperty ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type                                                                               | Name  |
| ---------------------------------------------------------------------------------- | ----- |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)   | key   |
| [Variant](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#variant) | value |
