# TicketGrantingProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [Login](#1-login) |
| 2 | [LoginEx](#2-loginex) |
| 3 | [RequestTicket](#3-requestticket) |
| 4 | [GetPID](#4-getpid) |
| 5 | [GetName](#5-getname) |
| 6 | [LoginWithContext](#6-loginwithcontext) |

# (1) Login

## Request

| Type | Name |
|------|------|
| string | strUserName |

## Response

| Type | Name |
|------|------|
| uint32 | pidPrincipal |
| buffer | pbufResponse |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |
| qresult | %retval% |

# (2) LoginEx

## Request

| Type | Name |
|------|------|
| string | strUserName |
| any<Data,string> | oExtraData |

## Response

| Type | Name |
|------|------|
| uint32 | pidPrincipal |
| buffer | pbufResponse |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |
| qresult | %retval% |

# (3) RequestTicket

## Request

| Type | Name |
|------|------|
| uint32 | idSource |
| uint32 | idTarget |

## Response

| Type | Name |
|------|------|
| buffer | bufResponse |
| qresult | %retval% |

# (4) GetPID

## Request

| Type | Name |
|------|------|
| string | strUserName |

## Response

| Type | Name |
|------|------|
| uint32 | %retval% |

# (5) GetName

## Request

| Type | Name |
|------|------|
| uint32 | id |

## Response

| Type | Name |
|------|------|
| string | %retval% |

# (6) LoginWithContext

## Request

| Type | Name |
|------|------|
| any<Data,string> | loginData |

## Response

| Type | Name |
|------|------|
| uint32 | pidPrincipal |
| buffer | pbufResponse |
| RVConnectionData | pConnectionData |
| qresult | %retval% |

# Types

## RVConnectionData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| stationurl | m_urlRegularProtocols |
| std_list<byte> | m_lstSpecialProtocols |
| stationurl | m_urlSpecialProtocols |

## LoginData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `Data`.

| Type | Name |
|------|------|
| int8 | m_principalType |
| string | m_userName |
| uint64 | m_context |
| uint32 | m_similarConnection |

## UbiAuthenticationLoginCustomData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `Data`.

| Type | Name |
|------|------|
| string | m_userName |
| string | m_onlineKey |
| string | m_password |
