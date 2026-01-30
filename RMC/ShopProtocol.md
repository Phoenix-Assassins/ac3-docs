# ShopProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [RequestItems](#1-requestitems) |
| 2 | [Unknown](#2-unknown) |
| 3 | [AddCurrency](#3-addcurrency) |
| 4 | [GetCurrency](#4-getcurrency) |
| 5 | [BuyItem](#5-buyitem) |
| 6 | [UnlockItem](#6-unlockitem) |
| 7 | [RequestBoughtItems](#7-requestboughtitems) |

# (1) RequestItems

## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| qlist\<[ShopPricing](#ShopPricing)\> | items |

# (2) Unknown

## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| [ShopItem](#ShopItem) | item |
| uint32 | unkUint1 |
| uint32 | unkUint2 |

# (3) AddCurrency

## Request
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |

## Response
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |

# (4) GetCurrency

## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |

# (5) BuyItem

## Request
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |

## Response
| Type | Name |
|------|------|
| bool | unkBool |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| [PlayerBoughtShopItem](#PlayerBoughtShopItem) | item |

# (6) UnlockItem

## Request
| Type | Name |
|------|------|
| uint32 | unkUint |

## Response
| Type | Name |
|------|------|
| bool | unkBool |
| [PlayerBoughtShopItem](#PlayerBoughtShopItem) | item |

# (7) RequestBoughtItems

## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| qlist\<[PlayerBoughtShopItem](#PlayerBoughtShopItem)\> | items |

# Types

## ShopPricing ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| int32 | unkInt1 |
| int32 | unkInt2 |
| int32 | unkInt3 |
| int32 | unkInt4 |

## ShopItem ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| int32 | unkInt1 |
| string | unkString |
| int32 | unkInt2 |
| int32 | unkInt3 |
| int32 | unkInt4 |
| int32 | unkInt5 |
| int32 | unkInt6 |
| int32 | unkInt7 |

## PlayerBoughtShopItem ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| datetime | time1 |
| datetime | time2 |
