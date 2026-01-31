# LadderProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [RegisterNewGame](#1-registernewgame) |
| 2 | [ParticipateGame](#2-participategame) |
| 3 | [EndGame](#3-endgame) |
| 4 | [Unknown](#4-unknown) |
| 5 | [RunSimulation](#5-runsimulation) |

# (1) RegisterNewGame

## Request
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| [LadderInfo](#LadderInfo-structure) | unkObj |

## Response

| Type | Name |
|------|------|
| int32 | unkInt |

# (2) ParticipateGame

## Request

| Type | Name |
|------|------|
| [LadderInfo](#LadderInfo-structure) | unkObj |

## Response

This method does not return anything.

# (3) EndGame

## Request

| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist\<[LadderInfo](#LadderInfo-structure)> | unkObjs |

## Response

| Type | Name |
|------|------|
| qlist\<[LadderInfo](#LadderInfo-structure)> | list |

# (4) Unknown

## Request
Payload unknown.

## Response

| Type | Name |
|------|------|
| qlist\<[LadderInfo](#LadderInfo-structure)> | list |

# (5) RunSimulation

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| int32 | unkInt |

# Types

## LadderInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkInt1 |
| uint32 | unkInt2 |
| [qBuffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#qbuffer) | data |
