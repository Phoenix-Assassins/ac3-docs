# ClientLoginProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [Authenticate](#1-authenticate) |
| 2 | [Recommend](#2-recommend) |
| 3 | [GetFriendStatus](#3-getfriendstatus) |
| 4 | [GetServerTime](#4-getservertime) |
| 5 | [GetCXBVersion](#5-getcxbversion) |
| 6 | [OnCXBChanged](#6-oncxbchanged) |
| 7 | [GetCommunityEffort](#7-getcommunityeffort) |
| 8 | [Unknown](#8-unknown) |
| 9 | [Unknown](#9-unknown) |

# (1) Authenticate
## Request
| Type | Name |
|------|------|
| int32 | unkInt1 |
| string | unkString |
| int32 | unkInt2 |
| bool | unkBool |

## Response
| Type | Name |
|------|------|
| bool | unkBool |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| string | unkString1 |
| string | unkString2 |

# (2) Recommend
## Request
| Type | Name |
|------|------|
| int32 | unkInt |
| string | unkString |
| string | unkString |

## Response
| Type | Name |
|------|------|
| bool | unkBool |

# (3) GetFriendStatus
## Request
| Type | Name |
|------|------|
| int32 | unkInt |
| string | unkString |
| qlist<string> | unkStrings |

## Response
| Type | Name |
|------|------|
| bool | unkBool |
| qlist<[FriendInfo](#FriendInfo)> | friendInfos |

# (4) GetServerTime
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| datetime | serverTime |

# (5) GetCXBVersion
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| uint32 | cxbVersion |

# (6) OnCXBChanged
## Request
This method does not take any parameters.

## Response
This method does not return anything.

# (7) GetCommunityEffort
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| int32 | unkInt1 |
| int32 | unkInt2 |
| int32 | unkInt3 |
| int32 | unkInt4 |
| int32 | unkInt5 |

# (8) Unknown
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| uint32 | unkUint |

# (9) Unknown
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| bool | unkBool |

# Types

## FriendInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | name |
| uint32 | pid |
| bool | online |
