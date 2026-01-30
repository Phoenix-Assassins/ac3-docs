# UserAccountManagementProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [LookupSceNpIds](#1-lookupscenpids) |
| 2 | [LookupPrincipalIDs](#2-lookupprincipalids) |
| 3 | [LookupFirstPartyIds](#3-lookupfirstpartyids) |
| 4 | [UserHasPlayed](#4-userhasplayed) |
| 5 | [IsUserPlaying](#5-isuserplaying) |
| 6 | [updateSonyAccountInfo](#6-updatesonyaccountinfo) |

# (1) LookupSceNpIds

## Request

| Type | Name |
|------|------|
| std_list<uint32> | pids |

## Response

| Type | Name |
|------|------|
| std_map<uint32,qBuffer> | npids |

# (2) LookupPrincipalIDs

## Request

| Type | Name |
|------|------|
| std_list<string> | firstPartyIds |
| uint32 | platformId |

## Response

| Type | Name |
|------|------|
| std_map<string,uint32> | pids |

# (3) LookupFirstPartyIds

## Request

| Type | Name |
|------|------|
| std_list<uint32> | pids |
| uint32 | platformId |

## Response

| Type | Name |
|------|------|
| std_map<uint32,string> | firstPartyIds |

# (4) UserHasPlayed

## Request

| Type | Name |
|------|------|
| std_list<string> | FirstPartyIds |
| uint32 | platformId |

## Response

| Type | Name |
|------|------|
| std_map<string,bool> | UserPresence |

# (5) IsUserPlaying

## Request

| Type | Name |
|------|------|
| std_list<string> | firstPartyIds |
| uint32 | platformId |

## Response

| Type | Name |
|------|------|
| std_map<string,bool> | UserPresence |

# (6) updateSonyAccountInfo

## Request

| Type | Name |
|------|------|
| qBuffer | ticketData |
| uint32 | ticketSize |

## Response
This method does not return anything.
