# MatchMakingProtocolExt

| Method ID | Method Name |
|-----------|-------------|
| 1 | [EndParticipation](#1-endparticipation) |
| 2 | [GetParticipants](#2-getparticipants) |
| 3 | [GetDetailedParticipants](#3-getdetailedparticipants) |
| 4 | [GetParticipantsURLs](#4-getparticipantsurls) |
| 5 | [GetGatheringRelations](#5-getgatheringrelations) |
| 6 | [DeleteFromDeletions](#6-deletefromdeletions) |

# (1) EndParticipation

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (2) GetParticipants

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| bool | bOnlyActive |

## Response

| Type | Name |
|------|------|
| std_list<uint32> | lstParticipants |

# (3) GetDetailedParticipants

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| bool | bOnlyActive |

## Response

| Type | Name |
|------|------|
| std_list<ParticipantDetails> | lstParticipants |

# (4) GetParticipantsURLs

## Request

| Type | Name |
|------|------|
| std_list<uint32> | lstGatherings |

## Response

| Type | Name |
|------|------|
| std_list<GatheringURLs> | lstGatheringURLs |

# (5) GetGatheringRelations

## Request

| Type | Name |
|------|------|
| uint32 | id |
| string | descr |

## Response

| Type | Name |
|------|------|
| string | %retval% |

# (6) DeleteFromDeletions

## Request

| Type | Name |
|------|------|
| std_list<uint32> | lstDeletions |
| uint32 | pid |

# Types

## GatheringURLs ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_gid |
| std_list<stationurl> | m_lstStationURLs |

## ParticipantDetails ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_idParticipant |
| string | m_strName |
| string | m_strMessage |
