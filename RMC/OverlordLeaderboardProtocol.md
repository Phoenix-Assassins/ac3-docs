# LeaderboardProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [ReportStats](#1-reportstats) |
| 2 | [ReportArbitratedStats](#2-reportarbitratedstats) |
| 3 | [ReadBoard](#3-readboard) |

# (1) ReportStats
## Request
| Type | Name |
|------|------|
| List<[ReportedStat](#reportedstat-structure)> | stats |

## Response
This method does not return anything.

# (2) ReportArbitratedStats
## Request
| Type | Name |
|------|------|
| uint32 | unkUint |
| List<[ReportedStat](#reportedstat-structure)> | stats |

## Response
This method does not return anything.

# (3) ReadBoard
## Request
| Type | Name |
|------|------|
| List<[ProtoBoardQueryValues](#protoboardqueryvalues-structure)> | queryValues |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| [ProtoFilter](#protofilter-structure) | filter |

## Response
| Type | Name |
|------|------|
| List<[ProtoBoardResultValues](#protoboardresultvalues-structure)> | boardResults |

# Types

## ProtoBoardQueryValues ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| List\<uint32> | unkUints |

## ProtoFilter
Extends `Data`.

## ReportedStat ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| List<[ProtoProperty](#protoproperty-structure)> | props |

## ProtoProperty ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| [Variant](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#variant) | variant |

## ProtoBoardResultValues ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| string | unkString |
| uint32 | unkUint3 |
| uint32 | unkUint4 |
| uint32 | unkUint5 |
| uint64 | unkLong |
| uint32 | unkUint6 |
| List<[ProtoProperty](#protoproperty-structure)> | props |
