# AccountManagementProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [CreateAccount](#1-createaccount) |
| 2 | [DeleteAccount](#2-deleteaccount) |
| 3 | [DisableAccount](#3-disableaccount) |
| 4 | [ChangePassword](#4-changepassword) |
| 5 | [TestCapability](#5-testcapability) |
| 6 | [GetName](#6-getname) |
| 7 | [GetAccountData](#7-getaccountdata) |
| 8 | [GetPrivateData](#8-getprivatedata) |
| 9 | [GetPublicData](#9-getpublicdata) |
| 10 | [GetMultiplePublicData](#10-getmultiplepublicdata) |
| 11 | [UpdateAccountName](#11-updateaccountname) |
| 12 | [UpdateAccountEmail](#12-updateaccountemail) |
| 13 | [UpdateCustomData](#13-updatecustomdata) |
| 14 | [FindByNameRegex](#14-findbynameregex) |
| 15 | [UpdateAccountExpiryDate](#15-updateaccountexpirydate) |
| 16 | [UpdateAccountEffectiveDate](#16-updateaccounteffectivedate) |
| 17 | [UpdateStatus](#17-updatestatus) |
| 18 | [GetStatus](#18-getstatus) |
| 19 | [GetLastConnectionStats](#19-getlastconnectionstats) |
| 20 | [ResetPassword](#20-resetpassword) |
| 21 | [CreateAccountWithCustomData](#21-createaccountwithcustomdata) |
| 22 | [RetrieveAccount](#22-retrieveaccount) |
| 23 | [UpdateAccount](#23-updateaccount) |
| 24 | [ChangePasswordByGuest](#24-changepasswordbyguest) |
| 25 | [FindByNameLike](#25-findbynamelike) |
| 26 | [CustomCreateAccount](#26-customcreateaccount) |
| 27 | [LookupOrCreateAccount](#27-lookuporcreateaccount) |
| 28 | [CreateAccountEx](#28-createaccountex) |
| 29 | [DisconnectPrincipal](#29-disconnectprincipal) |
| 30 | [DisconnectAllPrincipals](#30-disconnectallprincipals) |

# (1) CreateAccount

## Request

| Type | Name |
|------|------|
| string | strPrincipalName |
| string | strKey |
| uint32 | uiGroups |
| string | strEmail |

## Response

| Type | Name |
|------|------|
| qresult | %retval% |

# (2) DeleteAccount

## Request

| Type | Name |
|------|------|
| uint32 | idPrincipal |

## Response
This method does not return anything.

# (3) DisableAccount

## Request

| Type | Name |
|------|------|
| uint32 | idPrincipal |
| datetime | dtUntil |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| qresult | %retval% |

# (4) ChangePassword

## Request

| Type | Name |
|------|------|
| string | strNewKey |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (5) TestCapability

## Request

| Type | Name |
|------|------|
| uint32 | uiCapability |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (6) GetName

## Request

| Type | Name |
|------|------|
| uint32 | idPrincipal |

## Response

| Type | Name |
|------|------|
| string | strName |

# (7) GetAccountData

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| AccountData | oAccountData |
| qresult | %retval% |

# (8) GetPrivateData

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| any<Data,string> | oData |
| bool | %retval% |

# (9) GetPublicData

## Request

| Type | Name |
|------|------|
| uint32 | idPrincipal |

## Response

| Type | Name |
|------|------|
| any<Data,string> | oData |
| bool | %retval% |

# (10) GetMultiplePublicData

## Request

| Type | Name |
|------|------|
| std_list<uint32> | lstPrincipals |

## Response

| Type | Name |
|------|------|
| std_list<any<Data,string>> | oData |
| bool | %retval% |

# (11) UpdateAccountName

## Request

| Type | Name |
|------|------|
| string | strName |

## Response

| Type | Name |
|------|------|
| qresult | %retval% |

# (12) UpdateAccountEmail

## Request

| Type | Name |
|------|------|
| string | strName |

## Response

| Type | Name |
|------|------|
| qresult | %retval% |

# (13) UpdateCustomData

## Request

| Type | Name |
|------|------|
| any<Data,string> | oPublicData |
| any<Data,string> | oPrivateData |

## Response

| Type | Name |
|------|------|
| qresult | %retval% |

# (14) FindByNameRegex

## Request

| Type | Name |
|------|------|
| uint32 | uiGroups |
| string | strRegex |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| std_list<BasicAccountInfo> | plstAccounts |

# (15) UpdateAccountExpiryDate

## Request

| Type | Name |
|------|------|
| uint32 | idPrincipal |
| datetime | dtExpiry |
| string | strExpiredMessage |

## Response
This method does not return anything.

# (16) UpdateAccountEffectiveDate

## Request

| Type | Name |
|------|------|
| uint32 | idPrincipal |
| datetime | dtEffectiveFrom |
| string | strNotEffectiveMessage |

## Response
This method does not return anything.

# (17) UpdateStatus

## Request

| Type | Name |
|------|------|
| string | strStatus |

## Response
This method does not return anything.

# (18) GetStatus

## Request

| Type | Name |
|------|------|
| uint32 | idPrincipal |

## Response

| Type | Name |
|------|------|
| string | strStatus |

# (19) GetLastConnectionStats

## Request

| Type | Name |
|------|------|
| uint32 | idPrincipal |

## Response

| Type | Name |
|------|------|
| datetime | dtLastSessionLogin |
| datetime | dtLastSessionLogout |
| datetime | dtCurrentSessionLogin |

# (20) ResetPassword

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (21) CreateAccountWithCustomData

## Request

| Type | Name |
|------|------|
| string | strPrincipalName |
| string | strKey |
| uint32 | uiGroups |
| string | strEmail |
| any<Data,string> | oPublicData |
| any<Data,string> | oPrivateData |

## Response
This method does not return anything.

# (22) RetrieveAccount

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| AccountData | oAccountData |
| any<Data,string> | oPublicData |
| any<Data,string> | oPrivateData |

# (23) UpdateAccount

## Request

| Type | Name |
|------|------|
| string | strKey |
| string | strEmail |
| any<Data,string> | oPublicData |
| any<Data,string> | oPrivateData |

## Response
This method does not return anything.

# (24) ChangePasswordByGuest

## Request

| Type | Name |
|------|------|
| string | strPrincipalName |
| string | strEmail |
| string | strKey |

## Response
This method does not return anything.

# (25) FindByNameLike

## Request

| Type | Name |
|------|------|
| uint32 | uiGroups |
| string | strLike |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| std_list<BasicAccountInfo> | plstAccounts |

# (26) CustomCreateAccount

## Request

| Type | Name |
|------|------|
| string | strPrincipalName |
| string | strKey |
| uint32 | uiGroups |
| string | strEmail |
| any<Data,string> | oAuthData |

## Response

| Type | Name |
|------|------|
| uint32 | pid |

# (27) LookupOrCreateAccount

## Request

| Type | Name |
|------|------|
| string | strPrincipalName |
| string | strKey |
| uint32 | uiGroups |
| string | strEmail |
| any<Data,string> | oAuthData |

## Response

| Type | Name |
|------|------|
| uint32 | pid |

# (28) CreateAccountEx

## Request

| Type | Name |
|------|------|
| int8 | principalType |
| string | strPrincipalName |
| string | strKey |
| uint32 | uiGroups |
| string | strEmail |
| uint64 | context |

## Response

| Type | Name |
|------|------|
| qresult | %retval% |

# (29) DisconnectPrincipal

## Request

| Type | Name |
|------|------|
| uint32 | idPrincipal |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (30) DisconnectAllPrincipals

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# Types

## AccountData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_pid |
| string | m_strName |
| uint32 | m_uiGroups |
| string | m_strEmail |
| datetime | m_dtCreationDate |
| datetime | m_dtEffectiveDate |
| string | m_strNotEffectiveMsg |
| datetime | m_dtExpiryDate |
| string | m_strExpiredMsg |

## BasicAccountInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_pidOwner |
| string | m_strName |

## PublicData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `Data`.

This class does not declare any variables.

## PrivateData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `Data`.

This class does not declare any variables.
