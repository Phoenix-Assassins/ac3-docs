# UplayWinProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetActions](#1-getactions) |
| 2 | [GetActionsCompleted](#2-getactionscompleted) |
| 3 | [GetActionsCount](#3-getactionscount) |
| 4 | [GetActionsCompletedCount](#4-getactionscompletedcount) |
| 5 | [GetRewards](#5-getrewards) |
| 6 | [GetRewardsPurchased](#6-getrewardspurchased) |
| 7 | [UplayWelcome](#7-uplaywelcome) |
| 8 | [SetActionCompleted](#8-setactioncompleted) |
| 9 | [SetActionsCompleted](#9-setactionscompleted) |
| 10 | [GetUserToken](#10-getusertoken) |
| 11 | [GetVirtualCurrencyUserBalance](#11-getvirtualcurrencyuserbalance) |
| 12 | [GetSectionsByKey](#12-getsectionsbykey) |

# (1) GetActions

## Request

| Type | Name |
|------|------|
| int32 | startRowIndex |
| int32 | maximumRows |
| string | sortExpression |
| string | cultureName |
| string | platformCode |
| string | gameCode |

## Response

| Type | Name |
|------|------|
| qlist<UplayAction> | actionList |

# (2) GetActionsCompleted

## Request

| Type | Name |
|------|------|
| int32 | startRowIndex |
| int32 | maximumRows |
| string | sortExpression |
| string | cultureName |
| string | platformCode |
| string | gameCode |

## Response

| Type | Name |
|------|------|
| qlist<UplayAction> | actionList |

# (3) GetActionsCount

## Request

| Type | Name |
|------|------|
| string | platformCode |
| string | gameCode |

## Response

| Type | Name |
|------|------|
| int32 | actionsCount |

# (4) GetActionsCompletedCount

## Request

| Type | Name |
|------|------|
| string | platformCode |
| string | gameCode |

## Response

| Type | Name |
|------|------|
| int32 | actionsCount |

# (5) GetRewards

## Request

| Type | Name |
|------|------|
| int32 | startRowIndex |
| int32 | maximumRows |
| string | sortExpression |
| string | cultureName |
| string | platformCode |
| string | gameCode |

## Response

| Type | Name |
|------|------|
| qlist<UplayReward> | rewardList |

# (6) GetRewardsPurchased

## Request

| Type | Name |
|------|------|
| int32 | startRowIndex |
| int32 | maximumRows |
| string | sortExpression |
| string | cultureName |
| string | platformCode |
| string | gameCode |

## Response

| Type | Name |
|------|------|
| qlist<UplayReward> | rewardList |

# (7) UplayWelcome

## Request

| Type | Name |
|------|------|
| string | cultureName |
| string | platformCode |
| string | gameCode |

## Response

| Type | Name |
|------|------|
| qlist<UplayAction> | actionList |

# (8) SetActionCompleted

## Request

| Type | Name |
|------|------|
| string | actionCode |
| string | cultureName |
| string | platformCode |
| string | gameCode |

## Response

| Type | Name |
|------|------|
| UplayAction | unlockedAction |

# (9) SetActionsCompleted

## Request

| Type | Name |
|------|------|
| qlist<string> | actionCodeList |
| string | cultureName |
| string | platformCode |
| string | gameCode |

## Response

| Type | Name |
|------|------|
| qlist<UplayAction> | actionList |

# (10) GetUserToken

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| string | token |

# (11) GetVirtualCurrencyUserBalance

## Request

| Type | Name |
|------|------|
| string | platformCode |

## Response

| Type | Name |
|------|------|
| int32 | virtualCurrencyUserBalance |

# (12) GetSectionsByKey

## Request

| Type | Name |
|------|------|
| string | cultureName |
| string | sectionKey |
| string | platformCode |
| string | gameCode |

## Response

| Type | Name |
|------|------|
| qlist<UplaySection> | sectionList |

# Types

## UplayActionPlatform ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_platformCode |
| bool | m_completed |
| string | m_specificKey |

## UplayRewardPlatform ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_platformCode |
| bool | m_purchased |

## UplayAction ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_code |
| string | m_name |
| string | m_description |
| int32 | m_value |
| string | m_gameCode |
| qlist<UplayActionPlatform> | m_platforms |

## UplayReward ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_code |
| string | m_name |
| string | m_description |
| int32 | m_value |
| string | m_rewardTypeName |
| string | m_gameCode |
| qlist<UplayRewardPlatform> | m_platforms |

## UplaySectionContentLocalized ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_key |
| string | m_culture |
| string | m_text |
| string | m_url |
| int32 | m_duration |
| string | m_size |
| string | m_width |
| string | m_height |

## UplaySectionContent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_key |
| string | m_name |
| int16 | m_order |
| string | m_typeName |
| UplaySectionContentLocalized | m_localizedInfo |

## UplaySection ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_key |
| string | m_name |
| string | m_typeName |
| string | m_menuTypeName |
| qlist<UplaySectionContent> | m_contentList |
| string | m_gameCode |
| string | m_platformCode |
