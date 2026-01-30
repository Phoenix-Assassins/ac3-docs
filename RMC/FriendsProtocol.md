# FriendsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [AddFriend](#1-addfriend) |
| 2 | [AddFriendByName](#2-addfriendbyname) |
| 3 | [AddFriendWithDetails](#3-addfriendwithdetails) |
| 4 | [AddFriendByNameWithDetails](#4-addfriendbynamewithdetails) |
| 5 | [AcceptFriendship](#5-acceptfriendship) |
| 6 | [DeclineFriendship](#6-declinefriendship) |
| 7 | [BlackList](#7-blacklist) |
| 8 | [BlackListByName](#8-blacklistbyname) |
| 9 | [ClearRelationship](#9-clearrelationship) |
| 10 | [UpdateDetails](#10-updatedetails) |
| 11 | [GetList](#11-getlist) |
| 12 | [GetDetailedList](#12-getdetailedlist) |
| 13 | [GetRelationships](#13-getrelationships) |

# (1) AddFriend

## Request

| Type | Name |
|------|------|
| uint32 | uiPlayer |
| uint32 | uiDetails |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (2) AddFriendByName

## Request

| Type | Name |
|------|------|
| string | strPlayerName |
| uint32 | uiDetails |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (3) AddFriendWithDetails

## Request

| Type | Name |
|------|------|
| uint32 | uiPlayer |
| uint32 | uiDetails |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| RelationshipData | relationshipData |

# (4) AddFriendByNameWithDetails

## Request

| Type | Name |
|------|------|
| string | strPlayerName |
| uint32 | uiDetails |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| RelationshipData | relationshipData |

# (5) AcceptFriendship

## Request

| Type | Name |
|------|------|
| uint32 | uiPlayer |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (6) DeclineFriendship

## Request

| Type | Name |
|------|------|
| uint32 | uiPlayer |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (7) BlackList

## Request

| Type | Name |
|------|------|
| uint32 | uiPlayer |
| uint32 | uiDetails |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (8) BlackListByName

## Request

| Type | Name |
|------|------|
| string | strPlayerName |
| uint32 | uiDetails |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (9) ClearRelationship

## Request

| Type | Name |
|------|------|
| uint32 | uiPlayer |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (10) UpdateDetails

## Request

| Type | Name |
|------|------|
| uint32 | uiPlayer |
| uint32 | uiDetails |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (11) GetList

## Request

| Type | Name |
|------|------|
| byte | byRelationship |
| bool | bReversed |

## Response

| Type | Name |
|------|------|
| std_list<uint32> | lstFriendsList |

# (12) GetDetailedList

## Request

| Type | Name |
|------|------|
| byte | byRelationship |
| bool | bReversed |

## Response

| Type | Name |
|------|------|
| std_list<FriendData> | lstFriendsList |

# (13) GetRelationships

## Request

| Type | Name |
|------|------|
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| uint32 | uiTotalCount |
| std_list<RelationshipData> | lstRelationshipsList |

# Types

## FriendData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_pid |
| string | m_strName |
| byte | m_byRelationship |
| uint32 | m_uiDetails |
| string | m_strStatus |

## RelationshipData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_pid |
| string | m_strName |
| byte | m_byRelationship |
| uint32 | m_uiDetails |
| byte | m_byStatus |
