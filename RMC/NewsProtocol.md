# NewsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetChannels](#1-getchannels) |
| 2 | [GetChannelsByTypes](#2-getchannelsbytypes) |
| 3 | [GetSubscribableChannels](#3-getsubscribablechannels) |
| 4 | [GetChannelsByIDs](#4-getchannelsbyids) |
| 5 | [GetSubscribedChannels](#5-getsubscribedchannels) |
| 6 | [SubscribeChannel](#6-subscribechannel) |
| 7 | [UnsubscribeChannel](#7-unsubscribechannel) |
| 8 | [GetNewsHeaders](#8-getnewsheaders) |
| 9 | [GetNewsMessages](#9-getnewsmessages) |
| 10 | [GetNumberOfNews](#10-getnumberofnews) |
| 11 | [GetChannelByType](#11-getchannelbytype) |
| 12 | [GetNewsHeadersByType](#12-getnewsheadersbytype) |
| 13 | [GetNewsMessagesByType](#13-getnewsmessagesbytype) |

# (1) GetChannels

## Request

| Type | Name |
|------|------|
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (2) GetChannelsByTypes

## Request

| Type | Name |
|------|------|
| qlist<string> | newsChannelTypes |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (3) GetSubscribableChannels

## Request

| Type | Name |
|------|------|
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (4) GetChannelsByIDs

## Request

| Type | Name |
|------|------|
| qlist<uint32> | newsChannelIDs |

## Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (5) GetSubscribedChannels

## Request

| Type | Name |
|------|------|
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (6) SubscribeChannel

## Request

| Type | Name |
|------|------|
| uint32 | newsChannelID |

## Response
This method does not return anything.

# (7) UnsubscribeChannel

## Request

| Type | Name |
|------|------|
| uint32 | newsChannelID |

## Response
This method does not return anything.

# (8) GetNewsHeaders

## Request

| Type | Name |
|------|------|
| NewsRecipient | recipient |
| ResultRange | range |

## Response

| Type | Name |
|------|------|
| qlist<NewsHeader> | newsHeaders |

# (9) GetNewsMessages

## Request

| Type | Name |
|------|------|
| qlist<uint32> | newsMessageIDs |

## Response

| Type | Name |
|------|------|
| qlist<NewsMessage> | newsMessages |

# (10) GetNumberOfNews

## Request

| Type | Name |
|------|------|
| NewsRecipient | recipient |

## Response

| Type | Name |
|------|------|
| uint32 | numberOfNews |

# (11) GetChannelByType

## Request

| Type | Name |
|------|------|
| string | newsChannelType |

## Response

| Type | Name |
|------|------|
| NewsChannel | channel |

# (12) GetNewsHeadersByType

## Request

| Type | Name |
|------|------|
| string | newsChannelType |
| ResultRange | range |

## Response

| Type | Name |
|------|------|
| qlist<NewsHeader> | newsHeaders |

# (13) GetNewsMessagesByType

## Request

| Type | Name |
|------|------|
| string | newsChannelType |
| ResultRange | range |

## Response

| Type | Name |
|------|------|
| qlist<NewsMessage> | newsMessages |

# Types

## NewsChannel ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_ownerPID |
| string | m_name |
| string | m_description |
| datetime | m_creationTime |
| datetime | m_expirationTime |
| string | m_type |
| string | m_locale |
| bool | m_subscribable |

## NewsHeader ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_recipientID |
| uint32 | m_recipientType |
| uint32 | m_publisherPID |
| string | m_publisherName |
| datetime | m_publicationTime |
| datetime | m_displayTime |
| datetime | m_expirationTime |
| string | m_title |
| string | m_link |

## NewsMessage ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `NewsHeader`.

| Type | Name |
|------|------|
| string | m_body |

## NewsRecipient ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_recipientID |
| uint32 | m_recipientType |

## NewsFeedLink ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_newsChannelID |
| string | m_URL |
| string | m_description |
| datetime | m_feedUpdatedParseTime |
| datetime | m_lastUpdatedTime |
| datetime | m_nextRefreshTime |
| uint32 | m_refreshElapsedTimeMilliseconds |
| uint32 | m_refreshPeriodSeconds |
| bool | m_refreshEnabled |
| uint32 | m_refreshMethod |
| datetime | m_newestMessageTime |
| uint32 | m_messageAdded |
