# LiveEventsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [ReceiveMessages](#1-receivemessages) |
| 2 | [Unknown](#2-unknown) |
| 3 | [Unknown](#3-unknown) |
| 4 | [Unknown](#4-unknown) |

# (1) ReceiveMessages

## Request
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |

## Response

| Type | Name |
|------|------|
| qlist\<[Message](#message-structure)> | messages |
| uint32 | unkUint |

# (2) Unknown

## Request
Payload unknown.

## Response
This method does not return anything.

# (3) Unknown

## Request
Payload unknown.

## Response
This method does not return anything.

# (4) Unknown

## Request
Payload unknown.

## Response
This method does not return anything.

# Types

## Message ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| bool | unkBool |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint64 | unkLong1 |
| uint64 | unkLong2 |
| uint8 | unkByte |
| qBuffer | data |
