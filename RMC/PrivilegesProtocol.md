# PrivilegesProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetPrivileges](#1-getprivileges) |
| 2 | [ActivateKey](#2-activatekey) |
| 3 | [ActivateKeyWithExpectedPrivileges](#3-activatekeywithexpectedprivileges) |
| 4 | [GetPrivilegeRemainDuration](#4-getprivilegeremainduration) |
| 5 | [GetExpiredPrivileges](#5-getexpiredprivileges) |
| 6 | [GetPrivilegesEx](#6-getprivilegesex) |

# (1) GetPrivileges

## Request

| Type | Name |
|------|------|
| string | localeCode |

## Response

| Type | Name |
|------|------|
| std_map<uint32,Privilege> | privileges |

# (2) ActivateKey

## Request

| Type | Name |
|------|------|
| string | uniqueKey |
| string | languageCode |

## Response

| Type | Name |
|------|------|
| PrivilegeGroup | privilege |

# (3) ActivateKeyWithExpectedPrivileges

## Request

| Type | Name |
|------|------|
| string | uniqueKey |
| string | languageCode |
| qlist<uint32> | expectedPrivilegeIDs |

## Response

| Type | Name |
|------|------|
| PrivilegeGroup | privilege |

# (4) GetPrivilegeRemainDuration

## Request

| Type | Name |
|------|------|
| uint32 | privilegeID |

## Response

| Type | Name |
|------|------|
| int32 | seconds |

# (5) GetExpiredPrivileges

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| qlist<PrivilegeEx> | expiredPrivileges |

# (6) GetPrivilegesEx

## Request

| Type | Name |
|------|------|
| string | localeCode |

## Response

| Type | Name |
|------|------|
| qlist<PrivilegeEx> | privilegesEx |

# Types

## Privilege ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| string | m_description |

## PrivilegeEx ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| string | m_description |
| int32 | m_duration |

## PrivilegeGroup ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_description |
| qlist<Privilege> | m_privileges |
