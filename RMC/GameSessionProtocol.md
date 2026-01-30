# GameSessionProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [CreateSession](#1-createsession) |
| 2 | [UpdateSession](#2-updatesession) |
| 3 | [DeleteSession](#3-deletesession) |
| 4 | [MigrateSession](#4-migratesession) |
| 5 | [LeaveSession](#5-leavesession) |
| 6 | [GetSession](#6-getsession) |
| 7 | [SearchSessions](#7-searchsessions) |
| 8 | [AddParticipants](#8-addparticipants) |
| 9 | [RemoveParticipants](#9-removeparticipants) |
| 10 | [GetParticipantCount](#10-getparticipantcount) |
| 11 | [GetParticipants](#11-getparticipants) |
| 12 | [SendInvitation](#12-sendinvitation) |
| 13 | [GetInvitationReceivedCount](#13-getinvitationreceivedcount) |
| 14 | [GetInvitationsReceived](#14-getinvitationsreceived) |
| 15 | [GetInvitationSentCount](#15-getinvitationsentcount) |
| 16 | [GetInvitationsSent](#16-getinvitationssent) |
| 17 | [AcceptInvitation](#17-acceptinvitation) |
| 18 | [DeclineInvitation](#18-declineinvitation) |
| 19 | [CancelInvitation](#19-cancelinvitation) |
| 20 | [SendTextMessage](#20-sendtextmessage) |
| 21 | [RegisterURLs](#21-registerurls) |
| 22 | [JoinSession](#22-joinsession) |
| 23 | [AbandonSession](#23-abandonsession) |
| 24 | [SearchSessionsWithParticipants](#24-searchsessionswithparticipants) |
| 25 | [GetSessions](#25-getsessions) |
| 26 | [GetParticipantsURLs](#26-getparticipantsurls) |
| 27 | [MigrateSessionHost](#27-migratesessionhost) |
| 28 | [SplitSession](#28-splitsession) |
| 29 | [SearchSocialSessions](#29-searchsocialsessions) |
| 30 | [ReportUnsuccessfulJoinSessions](#30-reportunsuccessfuljoinsessions) |

# (1) CreateSession

## Request

| Type | Name |
|------|------|
| GameSession | gameSession |

## Response

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

# (2) UpdateSession

## Request

| Type | Name |
|------|------|
| GameSessionUpdate | gameSessionUpdate |

## Response
This method does not return anything.

# (3) DeleteSession

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

## Response
This method does not return anything.

# (4) MigrateSession

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

## Response

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKeyMigrated |

# (5) LeaveSession

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

## Response
This method does not return anything.

# (6) GetSession

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

## Response

| Type | Name |
|------|------|
| GameSessionSearchResult | searchResult |

# (7) SearchSessions

## Request

| Type | Name |
|------|------|
| GameSessionQuery | gameSessionQuery |

## Response

| Type | Name |
|------|------|
| qlist<GameSessionSearchResult> | searchResults |

# (8) AddParticipants

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |
| qlist<uint32> | publicParticipantIDs |
| qlist<uint32> | privateParticipantIDs |

## Response
This method does not return anything.

# (9) RemoveParticipants

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |
| qlist<uint32> | participantIDs |

## Response
This method does not return anything.

# (10) GetParticipantCount

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

## Response

| Type | Name |
|------|------|
| uint32 | count |

# (11) GetParticipants

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| qlist<GameSessionParticipant> | participants |

# (12) SendInvitation

## Request

| Type | Name |
|------|------|
| GameSessionInvitation | invitation |

## Response
This method does not return anything.

# (13) GetInvitationReceivedCount

## Request

| Type | Name |
|------|------|
| uint32 | gameSessionTypeID |

## Response

| Type | Name |
|------|------|
| uint32 | count |

# (14) GetInvitationsReceived

## Request

| Type | Name |
|------|------|
| uint32 | gameSessionTypeID |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| qlist<GameSessionInvitationReceived> | invitations |

# (15) GetInvitationSentCount

## Request

| Type | Name |
|------|------|
| uint32 | gameSessionTypeID |

## Response

| Type | Name |
|------|------|
| uint32 | count |

# (16) GetInvitationsSent

## Request

| Type | Name |
|------|------|
| uint32 | gameSessionTypeID |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| qlist<GameSessionInvitationSent> | invitations |

# (17) AcceptInvitation

## Request

| Type | Name |
|------|------|
| GameSessionInvitationReceived | gameSessionInvitation |

## Response
This method does not return anything.

# (18) DeclineInvitation

## Request

| Type | Name |
|------|------|
| GameSessionInvitationReceived | gameSessionInvitation |

## Response
This method does not return anything.

# (19) CancelInvitation

## Request

| Type | Name |
|------|------|
| GameSessionInvitationSent | gameSessionInvitation |

## Response
This method does not return anything.

# (20) SendTextMessage

## Request

| Type | Name |
|------|------|
| GameSessionMessage | gameSessionMessage |

## Response
This method does not return anything.

# (21) RegisterURLs

## Request

| Type | Name |
|------|------|
| qlist<stationurl> | stationURLs |

## Response
This method does not return anything.

# (22) JoinSession

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

## Response
This method does not return anything.

# (23) AbandonSession

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

## Response
This method does not return anything.

# (24) SearchSessionsWithParticipants

## Request

| Type | Name |
|------|------|
| uint32 | gameSessionTypeID |
| qlist<uint32> | participantIDs |

## Response

| Type | Name |
|------|------|
| qlist<GameSessionSearchWithParticipantsResult> | searchResults |

# (25) GetSessions

## Request

| Type | Name |
|------|------|
| qlist<GameSessionKey> | gameSessionKeys |

## Response

| Type | Name |
|------|------|
| qlist<GameSessionSearchResult> | searchResults |

# (26) GetParticipantsURLs

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |
| qlist<uint32> | participantIDs |

## Response

| Type | Name |
|------|------|
| qlist<GameSessionParticipant> | participants |

# (27) MigrateSessionHost

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

## Response
This method does not return anything.

# (28) SplitSession

## Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

## Response

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKeyMigrated |

# (29) SearchSocialSessions

## Request

| Type | Name |
|------|------|
| GameSessionSocialQuery | gameSessionSocialQuery |

## Response

| Type | Name |
|------|------|
| qlist<GameSessionSearchWithParticipantsResult> | searchResults |

# (30) ReportUnsuccessfulJoinSessions

## Request

| Type | Name |
|------|------|
| qlist<GameSessionUnsuccessfulJoinSession> | unsuccessfulJoinSessions |

## Response
This method does not return anything.

# Types

## GameSessionKey ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_typeID |
| uint32 | m_sessionID |

## GameSession ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_typeID |
| qlist<Property> | m_attributes |

## GameSessionSearchResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| uint32 | m_hostPID |
| qlist<stationurl> | m_hostURLs |
| qlist<Property> | m_attributes |

## GameSessionUpdate ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| qlist<Property> | m_attributes |

## GameSessionParticipant ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_PID |
| string | m_name |
| qlist<stationurl> | m_stationURLs |

## GameSessionInvitation ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| qlist<uint32> | m_recipientPIDs |
| string | m_message |

## GameSessionInvitationSent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| uint32 | m_recipientPID |
| string | m_message |
| datetime | m_creationTime |

## GameSessionInvitationReceived ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| uint32 | m_senderPID |
| string | m_message |
| datetime | m_creationTime |

## GameSessionQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_typeID |
| uint32 | m_queryID |
| qlist<Property> | m_parameters |

## GameSessionSocialQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_typeID |
| uint32 | m_queryID |
| qlist<Property> | m_parameters |
| qlist<uint32> | m_participantIDs |

## GameSessionMessage ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| string | m_message |

## GameSessionSearchWithParticipantsResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `GameSessionSearchResult`.

| Type | Name |
|------|------|
| qlist<uint32> | m_participantIDs |

## GameSessionUnsuccessfulJoinSession ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| uint32 | m_errorCategory |
| int32 | m_errorCode |
