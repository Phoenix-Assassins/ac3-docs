# OverlordDareProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [RequestDareInfo](#1-requestdareinfo) |
| 2 | [DeleteDare](#2-deletedare) |
| 3 | [PostDare](#3-postdare) |
| 4 | [ChangeStatus](#4-changestatus) |
| 5 | [RequestUnreadCount](#5-requestunreadcount) |

# (1) RequestDareInfo
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| datetime | date |
| List<[ProtoDareInfo](#protodareinfo-structure)> | dareInfos |

# (2) DeleteDare
## Request
| Type | Name |
|------|------|
| uint32 | dareId |

## Response
This method does not return anything.

# (3) PostDare
## Request
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |

## Response
This method does not return anything.

# (4) ChangeStatus
## Request
| Type | Name |
|------|------|
| List\<uint32> | unkUints |
| uint32 | unkUint |

## Response
This method does not return anything.

# (5) RequestUnreadCount
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| uint32 | unreadCount |

# Types

## ProtoDareInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| datetime | date |
| uint32 | unkUint3 |
| uint32 | unkUint4 |
| uint32 | unkUint5 |
