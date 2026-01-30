# GameInfoProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [SetSessionMember](#1-setsessionmember) |
| 2 | [RemoveSessionMember](#2-removesessionmember) |
| 3 | [GetSessionMembersCount](#3-getsessionmemberscount) |
| 4 | [GetParticipantsFromParameter](#4-getparticipantsfromparameter) |
| 5 | [GetParticipantsFromOneParameterAndFilters](#5-getparticipantsfromoneparameterandfilters) |
| 6 | [GetParticipantsByHermesModeInHermesSession](#6-getparticipantsbyhermesmodeinhermessession) |
| 7 | [GetFileListOnGameStorage](#7-getfilelistongamestorage) |

# (1) SetSessionMember

## Request

| Type | Name |
|------|------|
| [SessionMember](#sessionmember-structure) | sesMember |

## Response

This method does not return anything.

# (2) RemoveSessionMember

## Request

This method does not take any parameters.

## Response

This method does not return anything.

# (3) GetSessionMembersCount

## Request

| Type | Name |
|------|------|
| [SessionMember](#sessionmember-structure) | sesMember |

## Response

| Type | Name |
|------|------|
| Uint32 | sesMemberCount |

# (4) GetParticipantsFromParameter

## Request

| Type | Name |
|------|------|
| Uint32 | param |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Participant](#participant-structure)> | participants |

# (5) GetParticipantsFromOneParameterAndFilters

## Request

| Type | Name |
|------|------|
| Uint32 | param |
| [SessionMember](#sessionmember-structure) | sesMember |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Participant](#participant-structure)> | participants |

# (6) GetParticipantsByHermesModeInHermesSession

## Request

| Type | Name |
|------|------|
| Uint32 | hermesMode |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Participant](#participant-structure)> | participants |

# (7) GetFileListOnGameStorage

## Request

| Type | Name |
|------|------|
| Uint32 | minNbElements |
| Uint32 | maxNbElements |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | fileName |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[File](#file-structure)> |  files |

# Types

## File ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | fileName |
| Uint32 | fileSize |

Name `fileSize` was assumed, example value was `58 484`.

## Participant ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

## SessionMember ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| Uint32 | unkUint3 |
| Uint32 | unkUint4 |
| Uint32 | unkUint5 |
| Uint32 | unkUint6 |
| Uint32 | unkUint7 |
| Uint32 | unkUint8 |
| Uint32 | unkUint9 |
