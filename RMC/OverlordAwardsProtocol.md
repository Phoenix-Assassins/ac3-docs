# AwardsProtocol

| Method ID | Method Name                                   |
| --------- | --------------------------------------------- |
| 1         | [UnlockAward1](#1-unlockaward1)               |
| 2         | [Unknown](#2-unknown)                         |
| 3         | [UnlockAward3](#3-unlockaward3)               |
| 4         | [SyncAwards](#4-syncawards)                   |
| 5         | [GetGroupDefinitions](#5-getgroupdefinitions) |
| 6         | [GetDefinitions](#6-getdefinitions)           |
| 7         | [GetAwards](#7-getawards)                     |

# (1) UnlockAward1
## Request
| Type   | Name    |
| ------ | ------- |
| uint32 | awardId |

## Response
This method does not return anything.

# (2) Unknown
## Request
| Type         | Name     |
| ------------ | -------- |
| List\<uint32> | unkUints |

## Response
This method does not return anything.

# (3) UnlockAward3
## Request
| Type   | Name |
| ------ | ---- |
| uint32 | awardId |

## Response
This method does not return anything.

# (4) SyncAwards
## Request
| Type   | Name |
| ------ | ---- |
| List<[Award](#award-structure)> | awards |

## Response
This method does not return anything.

# (5) GetGroupDefinitions
## Request
This method does not take any parameters.

## Response
| Type   | Name |
| ------ | ---- |
| List<[ProtoGroupInfo](#protogroupinfo-structure)> | groupDefs |

# (6) GetDefinitions
## Request
| Type   | Name |
| ------ | ---- |
| List\<uint32> | defIds |

## Response
| Type   | Name |
| ------ | ---- |
| List<[ProtoAwardInfo](#protoawardinfo-structure)> | definitions |

# (7) GetAwards

## Request
| Type   | Name |
| ------ | ---- |
| ProtoAwardsFilter | filter |
| List\<uint32> | ids |

## Response
| Type   | Name |
| ------ | ---- |
| List<[ProtoAwardGranted](#protoawardgranted-structure)> | awards |

# Types

## Award ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| datetime | date |

## ProtoGroupInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
| Type | Name |
|------|------|
| uint32 | unkUint |
| string | unkStr1 |
| string | unkStr2 |

## ProtoAwardInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| string | unkStr1 |
| string | unkStr2 |
| string | unkStr3 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| string | unkStr4 |
| string | unkStr5 |
| uint32 | unkUint4 |

## ProtoAwardGranted ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| datetime | date1 |
| datetime | date2 |
| uint32 | unkUint3 |
