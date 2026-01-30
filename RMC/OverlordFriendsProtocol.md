# OverlordFriendsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [RequestFriends](#1-requestfriends) |
| 2 | [SyncUbiFriends](#2-syncubifriends) |

# (1) RequestFriends
## Request
| Type | Name |
|------|------|
| uint32 | unkUint |
| List\<string> | friendNames |

## Response
This method does not return anything.

# (2) SyncUbiFriends
## Request
| Type | Name |
|------|------|
| List\<[UbiFriend](#UbiFriend-structure)> | friends |

## Response
This method does not return anything.

# Types

## UbiFriend ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
| Type | Name |
|------|------|
| string | unkStr1 |
| string | unkStr2 |
