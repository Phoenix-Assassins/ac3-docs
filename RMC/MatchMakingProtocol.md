# MatchMakingProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [RegisterGathering](#1-registergathering) |
| 2 | [UnregisterGathering](#2-unregistergathering) |
| 3 | [UnregisterGatherings](#3-unregistergatherings) |
| 4 | [UpdateGathering](#4-updategathering) |
| 5 | [Invite](#5-invite) |
| 6 | [AcceptInvitation](#6-acceptinvitation) |
| 7 | [DeclineInvitation](#7-declineinvitation) |
| 8 | [CancelInvitation](#8-cancelinvitation) |
| 9 | [GetInvitationsSent](#9-getinvitationssent) |
| 10 | [GetInvitationsReceived](#10-getinvitationsreceived) |
| 11 | [Participate](#11-participate) |
| 12 | [CancelParticipation](#12-cancelparticipation) |
| 13 | [GetParticipants](#13-getparticipants) |
| 14 | [AddParticipants](#14-addparticipants) |
| 15 | [GetDetailedParticipants](#15-getdetailedparticipants) |
| 16 | [GetParticipantsURLs](#16-getparticipantsurls) |
| 17 | [FindByType](#17-findbytype) |
| 18 | [FindByDescription](#18-findbydescription) |
| 19 | [FindByDescriptionRegex](#19-findbydescriptionregex) |
| 20 | [FindByID](#20-findbyid) |
| 21 | [FindBySingleID](#21-findbysingleid) |
| 22 | [FindByOwner](#22-findbyowner) |
| 23 | [FindByParticipants](#23-findbyparticipants) |
| 24 | [FindInvitations](#24-findinvitations) |
| 25 | [FindBySQLQuery](#25-findbysqlquery) |
| 26 | [LaunchSession](#26-launchsession) |
| 27 | [UpdateSessionURL](#27-updatesessionurl) |
| 28 | [GetSessionURL](#28-getsessionurl) |
| 29 | [GetState](#29-getstate) |
| 30 | [SetState](#30-setstate) |
| 31 | [ReportStats](#31-reportstats) |
| 32 | [GetStats](#32-getstats) |
| 33 | [DeleteGathering](#33-deletegathering) |
| 34 | [GetPendingDeletions](#34-getpendingdeletions) |
| 35 | [DeleteFromDeletions](#35-deletefromdeletions) |
| 36 | [MigrateGatheringOwnership](#36-migrategatheringownership) |
| 37 | [FindByDescriptionLike](#37-findbydescriptionlike) |
| 38 | [RegisterLocalURL](#38-registerlocalurl) |
| 39 | [RegisterLocalURLs](#39-registerlocalurls) |
| 40 | [UpdateSessionHost](#40-updatesessionhost) |
| 41 | [GetSessionURLs](#41-getsessionurls) |

# (1) RegisterGathering

## Request

| Type | Name |
|------|------|
| any<Gathering,string> | anyGathering |

## Response

| Type | Name |
|------|------|
| uint32 | %retval% |

# (2) UnregisterGathering

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (3) UnregisterGatherings

## Request

| Type | Name |
|------|------|
| std_list<uint32> | lstGatherings |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (4) UpdateGathering

## Request

| Type | Name |
|------|------|
| any<Gathering,string> | anyGathering |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (5) Invite

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| std_list<uint32> | lstPrincipals |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (6) AcceptInvitation

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (7) DeclineInvitation

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (8) CancelInvitation

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| std_list<uint32> | lstPrincipals |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (9) GetInvitationsSent

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |

## Response

| Type | Name |
|------|------|
| std_list<Invitation> | lstInvitations |

# (10) GetInvitationsReceived

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| std_list<Invitation> | lstInvitations |

# (11) Participate

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (12) CancelParticipation

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (13) GetParticipants

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |

## Response

| Type | Name |
|------|------|
| std_list<uint32> | lstParticipants |

# (14) AddParticipants

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| std_list<uint32> | lstParticipants |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (15) GetDetailedParticipants

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |

## Response

| Type | Name |
|------|------|
| std_list<ParticipantDetails> | lstParticipants |

# (16) GetParticipantsURLs

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |

## Response

| Type | Name |
|------|------|
| std_list<stationurl> | lstStationURL |

# (17) FindByType

## Request

| Type | Name |
|------|------|
| string | strType |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| std_list<any<Gathering,string>> | lstGathering |

# (18) FindByDescription

## Request

| Type | Name |
|------|------|
| string | strDescription |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| std_list<any<Gathering,string>> | lstGathering |

# (19) FindByDescriptionRegex

## Request

| Type | Name |
|------|------|
| string | strDescriptionRegex |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| std_list<any<Gathering,string>> | lstGathering |

# (20) FindByID

## Request

| Type | Name |
|------|------|
| std_list<uint32> | lstID |

## Response

| Type | Name |
|------|------|
| std_list<any<Gathering,string>> | lstGathering |

# (21) FindBySingleID

## Request

| Type | Name |
|------|------|
| uint32 | id |

## Response

| Type | Name |
|------|------|
| bool | bResult |
| any<Gathering,string> | pGathering |

# (22) FindByOwner

## Request

| Type | Name |
|------|------|
| uint32 | id |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| std_list<any<Gathering,string>> | lstGathering |

# (23) FindByParticipants

## Request

| Type | Name |
|------|------|
| std_list<uint32> | pid |

## Response

| Type | Name |
|------|------|
| std_list<any<Gathering,string>> | lstGathering |

# (24) FindInvitations

## Request

| Type | Name |
|------|------|
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| std_list<any<Gathering,string>> | lstGathering |

# (25) FindBySQLQuery

## Request

| Type | Name |
|------|------|
| string | strQuery |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| std_list<any<Gathering,string>> | lstGathering |

# (26) LaunchSession

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| string | strURL |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (27) UpdateSessionURL

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| string | strURL |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (28) GetSessionURL

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |

## Response

| Type | Name |
|------|------|
| string | strURL |
| bool | %retval% |

# (29) GetState

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |

## Response

| Type | Name |
|------|------|
| uint32 | uiState |
| bool | %retval% |

# (30) SetState

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| uint32 | uiNewState |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (31) ReportStats

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| std_list<GatheringStats> | lstStats |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (32) GetStats

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| std_list<uint32> | lstParticipants |
| std_list<byte> | lstColumns |

## Response

| Type | Name |
|------|------|
| std_list<GatheringStats> | plstStats |
| bool | %retval% |

# (33) DeleteGathering

## Request

| Type | Name |
|------|------|
| uint32 | gid |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (34) GetPendingDeletions

## Request

| Type | Name |
|------|------|
| uint32 | uiReason |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| std_list<DeletionEntry> | lstDeletions |
| bool | %retval% |

# (35) DeleteFromDeletions

## Request

| Type | Name |
|------|------|
| std_list<uint32> | lstDeletions |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (36) MigrateGatheringOwnership

## Request

| Type | Name |
|------|------|
| uint32 | gid |
| std_list<uint32> | lstPotentialNewOwnersID |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (37) FindByDescriptionLike

## Request

| Type | Name |
|------|------|
| string | strDescriptionLike |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| std_list<any<Gathering,string>> | lstGathering |

# (38) RegisterLocalURL

## Request

| Type | Name |
|------|------|
| uint32 | gid |
| string | url |

## Response
This method does not return anything.

# (39) RegisterLocalURLs

## Request

| Type | Name |
|------|------|
| uint32 | gid |
| std_list<stationurl> | lstUrls |

## Response
This method does not return anything.

# (40) UpdateSessionHost

## Request

| Type | Name |
|------|------|
| uint32 | gid |

## Response
This method does not return anything.

# (41) GetSessionURLs

## Request

| Type | Name |
|------|------|
| uint32 | gid |

## Response

| Type | Name |
|------|------|
| std_list<stationurl> | lstURLs |

# Types

## ParticipantDetails ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_idParticipant |
| string | m_strName |
| string | m_strMessage |

## Gathering ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_idMyself |
| uint32 | m_pidOwner |
| uint32 | m_pidHost |
| uint16 | m_uiMinParticipants |
| uint16 | m_uiMaxParticipants |
| uint32 | m_uiParticipationPolicy |
| uint32 | m_uiPolicyArgument |
| uint32 | m_uiFlags |
| uint32 | m_uiState |
| string | m_strDescription |

## Invitation ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_idGathering |
| uint32 | m_idGuest |
| string | m_strMessage |

## GatheringStats ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_pidParticipant |
| uint32 | m_uiFlags |
| std_list<float> | m_lstValues |

## DeletionEntry ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_idGathering |
| uint32 | m_pid |
| uint32 | m_uiReason |
