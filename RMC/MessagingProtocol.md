# MessagingProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [DeliverMessage](#1-delivermessage) |
| 2 | [DeliverMessageToMultiplePlayers](#2-delivermessagetomultipleplayers) |
| 3 | [GetNumberOfMessages](#3-getnumberofmessages) |
| 4 | [GetMessagesHeaders](#4-getmessagesheaders) |
| 5 | [RetrieveAllMessagesWithinRange](#5-retrieveallmessageswithinrange) |
| 6 | [RetrieveMessages](#6-retrievemessages) |
| 7 | [DeleteMessages](#7-deletemessages) |
| 8 | [DeleteAllMessages](#8-deleteallmessages) |

# (1) DeliverMessage

## Request

| Type | Name |
|------|------|
| any<Data,string> | oUserMessage |

## Response

| Type | Name |
|------|------|
| any<Data,string> | oModifiedMessage |
| std_map<uint32,std_list<uint32>> | mapParticipants |

# (2) DeliverMessageToMultiplePlayers

## Request

| Type | Name |
|------|------|
| any<Data,string> | oUserMessage |
| std_list<uint32> | lstPrincipals |

## Response

| Type | Name |
|------|------|
| any<Data,string> | oModifiedMessage |
| std_map<uint32,std_list<uint32>> | mapParticipants |

# (3) GetNumberOfMessages

## Request

| Type | Name |
|------|------|
| MessageRecipient | recipient |

## Response

| Type | Name |
|------|------|
| uint32 | uiNbMessages |

# (4) GetMessagesHeaders

## Request

| Type | Name |
|------|------|
| MessageRecipient | recipient |
| ResultRange | range |

## Response

| Type | Name |
|------|------|
| std_list<UserMessage> | lstMsgHeaders |

# (5) RetrieveAllMessagesWithinRange

## Request

| Type | Name |
|------|------|
| MessageRecipient | recipient |
| ResultRange | range |

## Response

| Type | Name |
|------|------|
| std_list<any<Data,string>> | lstMessages |

# (6) RetrieveMessages

## Request

| Type | Name |
|------|------|
| MessageRecipient | recipient |
| std_list<uint32> | lstMsgIDs |
| bool | bLeaveOnServer |

## Response

| Type | Name |
|------|------|
| std_list<any<Data,string>> | lstMessages |

# (7) DeleteMessages

## Request

| Type | Name |
|------|------|
| MessageRecipient | recipient |
| std_list<uint32> | lstMessagesToDelete |

## Response
This method does not return anything.

# (8) DeleteAllMessages

## Request

| Type | Name |
|------|------|
| MessageRecipient | recipient |

## Response

| Type | Name |
|------|------|
| uint32 | uiNbDeletedMessages |

# Types

## MessageRecipient ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_idRecipient |
| uint32 | m_uiRecipientType |

## ResultRange ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_uiOffset |
| uint32 | m_uiSize |
