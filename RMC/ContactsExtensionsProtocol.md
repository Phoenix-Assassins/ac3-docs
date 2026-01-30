# ContactsExtensionsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [RetrieveContactSessionPS3](#1-retrievecontactsessionps3) |
| 2 | [RetrieveContactsSessionListPS3](2-retrievecontactssessionlistps3) |
| 3 | [RetrieveContactListByNames](3-retrievecontactlistbynames) |
| 4 | [RetrieveContactListByPIDs](4-retrievecontactlistbypids) |
| 5 | [UpdatePlayerRelations](5-updateplayerrelations) |
| 6 | [SendPlayerStatusUpdate](6-sendplayerstatusupdate) |

# (1) RetrieveContactSessionPS3

## Request

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | contactName |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Gathering](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure)> | sessions |

# (2) RetrieveContactsSessionListPS3

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)> | contactNames |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Gathering](https://github.com/kinnay/NintendoClients/wiki/Match-Making-Types#gathering-structure)> | sessions |

# (3) RetrieveContactListByNames

## Request

| Type | Name |
|------|------|
| qlist\<string> | names |

## Response

| Type | Name |
|------|------|
| qlist\<[ContactInfo](#ContactInfo-structure)> | contacts |

# (4) RetrieveContactListByPIDs

## Request

| Type | Name |
|------|------|
| qlist\<uint32> | pids |

## Response

| Type | Name |
|------|------|
| qlist\<[ContactInfo](#ContactInfo-structure)> | contacts |

# (5) UpdatePlayerRelations

## Request

| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist\<uint32> |  |

## Response
This method does not return anything.

# (6) SendPlayerStatusUpdate

## Request

| Type | Name |
|------|------|
| uint32 | status |

## Response
This method does not return anything.

# Types

## GameSessionByPlayerInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkString |
| uint32 | unkUint |
| bool | unkBool1 |
| bool | unkBool2 |
| [GameSessionSearchResult](https://github.com/kinnay/NintendoClients/wiki/Game-Session-Protocol#gamesessionsearchresult-structure) | gameSesSearchResult |

## ContactInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | unkString |
| uint32 | unkUint |
| uint8 | unkByte |
