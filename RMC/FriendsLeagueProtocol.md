# FriendsLeagueProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetCurrentGoals](#1-getcurrentgoals) |
| 2 | [SavePlayerProgress](#2-saveplayerprogress) |

# (1) GetCurrentGoals

## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| qlist\<[FriendsLeagueGoal](#FriendsLeagueGoal)\> | goals |
| uint64 | unkUint |
| datetime | time |

# (2) SavePlayerProgress

## Request
| Type | Name |
|------|------|
| uint64 | unkUint |

## Response
This method does not return anything.

# Types

## FriendsLeagueGoal ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint8 | unkByte |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
