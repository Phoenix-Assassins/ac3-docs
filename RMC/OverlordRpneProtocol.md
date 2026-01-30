# RpneProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [SendEvent](#1-sendevent) |
| 2 | [GetSubscriptions](#2-getsubscriptions) |
| 3 | [SetSubscriptions](#3-setsubscriptions) |
| 4 | [RequestInteractiveEvents](#4-requestinteractiveevents) |
| 5 | [UpdateInteractiveEvents](#5-updateinteractiveevents) |

# (1) SendEvent
## Request
| Type | Name |
|------|------|
| string | unkString |
| List\<[OverlordProperty](#overlordproperty-structure)> | props |

## Response
This method does not return anything.

# (2) GetSubscriptions
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| List\<[Subscription](#subscription-structure)> | subs |

# (3) SetSubscriptions
## Request
| Type | Name |
|------|------|
| List\<[Subscription](#subscription-structure)> | subs |

## Response
This method does not return anything.

# (4) RequestInteractiveEvents
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| List\<[ProtoEventContent](#protoeventcontent-structure)> | events |

# (5) UpdateInteractiveEvents
## Request
| Type | Name |
|------|------|
| List\<[ProtoEventContent](#protoeventcontent-structure)> | events |

## Response
This method does not return anything.

# Types

## OverlordProperty ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type                                                                               | Name  |
| ---------------------------------------------------------------------------------- | ----- |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)   | key   |
| [Variant](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#variant) | value |

## Subscription ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | unkString |
| qlist\<[SubscriptionState](#subscriptionstate-structure)> | states |

## SubscriptionState ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | unkString |
| uint32 | unkUint |
| bool | unkBool |

## ProtoEventContent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | unkString1 |
| string | unkString2 |
| string | unkString3 |
| uint32 | unkUint1 |
| datetime | date1 |
| datetime | date2 |
| uint32 | unkUint2 |
