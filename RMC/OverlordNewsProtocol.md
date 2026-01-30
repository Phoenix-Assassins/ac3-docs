# OverlordNewsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetNews](#1-getnews) |
| 2 | [GetNewsCount](#2-getnewscount) |

# (1) GetNews
## Request
| Type | Name |
|------|------|
| [NewsPredicate](#newspredicate-structure) | predicate |
| [ResultRange](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#resultrange-structure) | range |

## Response
| Type | Name |
|------|------|
| List<[NewsMessage](#newsmessage-structure)> | messages |

# (2) GetNewsCount
## Request
| Type | Name |
|------|------|
| [NewsPredicate](#newspredicate-structure) | predicate |

## Response
| Type | Name |
|------|------|
| uint32 | newsCount |

# Types

## NewsPredicate ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

One of:
- [ProtoPredicateGameNews](#protopredicategamenews-structure)
- [ProtoPredicatePrincipals](#protopredicateprincipals-structure)

## ProtoPredicateGameNews ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends [`AnyDataHolder`](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#anydataholder).
| Type | Name |
|------|------|
| string | channelType |
| string | newsType |

## ProtoPredicatePrincipals ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends [`AnyDataHolder`](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#anydataholder).
| Type | Name |
|------|------|
| uint32 | nbPlayers |
| List\<uint32> | playerIds |

## NewsHeader ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_recipientID |
| uint32 | m_recipientType |
| uint32 | m_publisherPID |
| string | m_publisherName |
| datetime | m_publicationTime |
| datetime | m_displayTime |
| datetime | m_expirationTime |
| string | m_title |
| string | m_link |

## NewsMessage ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends [`NewsHeader`](#newsheader-structure).

| Type | Name |
|------|------|
| string | m_body |
