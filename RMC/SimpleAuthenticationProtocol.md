# SimpleAuthenticationProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [Authenticate](#1-authenticate) |
| 2 | [LoginWithToken](#2-loginwithtoken) |
| 3 | [LoginWithTokenEx](#3-loginwithtokenex) |
| 4 | [Login](#4-login) |
| 5 | [LoginWithSubAccount](#5-loginwithsubaccount) |
| 6 | [Register](#6-register) |
| 7 | [RegisterEx](#7-registerex) |
| 8 | [LoginWithTokenCafe](#8-loginwithtokencafe) |
| 9 | [LoginWithTokenCafeEx](#9-loginwithtokencafeex) |

# (1) Authenticate

## Request

| Type | Name |
|------|------|
| string | strUserName |

## Response

| Type | Name |
|------|------|
| uint32 | pidPrincipal |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |
| qresult | %retval% |

# (2) LoginWithToken

## Request

| Type | Name |
|------|------|
| string | strToken |

## Response

| Type | Name |
|------|------|
| uint32 | pidPrincipal |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |
| qresult | %retval% |

# (3) LoginWithTokenEx

## Request

| Type | Name |
|------|------|
| string | strToken |
| any<Data,string> | oAnyData |

## Response

| Type | Name |
|------|------|
| uint32 | pidPrincipal |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |
| qresult | %retval% |

# (4) Login

## Request

| Type | Name |
|------|------|
| string | strUsername |
| string | strPassword |

## Response

| Type | Name |
|------|------|
| uint32 | pidPrincipal |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |
| qresult | %retval% |

# (5) LoginWithSubAccount

## Request

| Type | Name |
|------|------|
| any<Data,string> | loginData |

## Response

| Type | Name |
|------|------|
| uint32 | pidPrincipal |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |
| qresult | %retval% |

# (6) Register

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

# (7) RegisterEx

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

# (8) LoginWithTokenCafe

## Request

| Type | Name |
|------|------|
| string | strNintendoToken |

## Response

| Type | Name |
|------|------|
| uint32 | pidPrincipal |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |
| qresult | %retval% |

# (9) LoginWithTokenCafeEx

## Request

| Type | Name |
|------|------|
| string | strNintendoToken |
| any<Data,string> | oAnyData |

## Response

| Type | Name |
|------|------|
| uint32 | pidPrincipal |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |
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
