# OverlordChallengeProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetChallengeDefinitions](#1-getchallengedefinitions) |
| 2 | [EnterChallenge](#2-enterchallenge) |
| 3 | [QuitChallenge](#3-quitchallenge) |
| 4 | [ReportChallenge](#4-reportchallenge) |
| 5 | [RequestRecords](#5-requestrecords) |

# (1) GetChallengeDefinitions
## Request
| Type | Name |
|------|------|
| [ProtoChallengeFilter](#protochallengefilter-structure) | filter |
| [ResultRange](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#resultrange-structure) | range |

## Response
| Type | Name |
|------|------|
| List<[ProtoChallengeDefinition](#protochallengedefinition-structure)> | challengeDefs |

# (2) EnterChallenge
## Request
| Type | Name |
|------|------|
| uint32 | unkUint |
| List<[OverlordProperty](#overlordproperty-structure)> | props |

## Response
This method does not return anything.

# (3) QuitChallenge
## Request
| Type | Name |
|------|------|
| uint32 | unkUint |

## Response
This method does not return anything.

# (4) ReportChallenge
## Request
| Type | Name |
|------|------|
| uint32 | unkUint |
| List<[OverlordProperty](#overlordproperty-structure)> | props |

## Response
| Type | Name |
|------|------|
| [ProtoChallengeRecord](#protochallengerecord-structure) | challenge |

# (5) RequestRecords
## Request
| Type | Name |
|------|------|
| [ProtoChallengeFilter](#protochallengefilter-structure) | filter |
| [ResultRange](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#resultrange-structure) | range |

## Response
| Type | Name |
|------|------|
| List<[ProtoChallengeRecord](#protochallengerecord-structure)> | challenges |

# Types

## ProtoChallengeDefinition ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| string | unkString1 |
| string | unkString2 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |
| datetime | date1 |
| datetime | date2 |
| string | unkString3 |
| string | unkString4 |
| List<[OverlordProperty](#overlordproperty-structure)> | props1 |
| List<[OverlordProperty](#overlordproperty-structure)> | props2 |
| uint32 | unkUint5 |
| datetime | date3 |

## OverlordProperty ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type                                                                               | Name  |
| ---------------------------------------------------------------------------------- | ----- |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)   | key   |
| [Variant](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#variant) | value |

## ProtoChallengeFilter ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends [`Data`](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#data-structure).

## ProtoChallengeRecord ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| datetime | date1 |
| datetime | date1 |
| datetime | date1 |
| List<[OverlordProperty](#overlordproperty-structure)> | props |
