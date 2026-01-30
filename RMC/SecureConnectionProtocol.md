# SecureConnectionProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [Register](#1-register) |
| 2 | [RequestConnectionData](#2-requestconnectiondata) |
| 3 | [RequestURLs](#3-requesturls) |
| 4 | [RegisterEx](#4-registerex) |

# (1) Register

## Request

| Type | Name |
|------|------|
| std_list<stationurl> | vecMyURLs |

## Response

| Type | Name |
|------|------|
| uint32 | pidConnectionID |
| stationurl | urlPublic |
| qresult | %retval% |

# (2) RequestConnectionData

## Request

| Type | Name |
|------|------|
| uint32 | cidTarget |
| uint32 | pidTarget |

## Response

| Type | Name |
|------|------|
| std_list<ConnectionData> | pvecConnectionsData |
| bool | %retval% |

# (3) RequestURLs

## Request

| Type | Name |
|------|------|
| uint32 | cidTarget |
| uint32 | pidTarget |

## Response

| Type | Name |
|------|------|
| std_list<stationurl> | plstURLs |
| bool | %retval% |

# (4) RegisterEx

## Request

| Type | Name |
|------|------|
| std_list<stationurl> | vecMyURLs |
| any<Data,string> | hCustomData |

## Response

| Type | Name |
|------|------|
| uint32 | pidConnectionID |
| stationurl | urlPublic |
| qresult | %retval% |

# Types

## ConnectionData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| stationurl | m_StationUrl |
| uint32 | m_ConnectionID |
