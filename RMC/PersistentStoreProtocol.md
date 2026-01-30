# PersistentStoreProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [FindByGroup](#1-findbygroup) |
| 2 | [InsertItem](#2-insertitem) |
| 3 | [RemoveItem](#3-removeitem) |
| 4 | [GetItem](#4-getitem) |
| 5 | [InsertCustomItem](#5-insertcustomitem) |
| 6 | [GetCustomItem](#6-getcustomitem) |
| 7 | [FindItemsBySQLQuery](#7-finditemsbysqlquery) |
| 8 | [InsertCustomItemWithValue](#8-insertcustomitemwithvalue) |
| 9 | [GetCustomItemWithValue](#9-getcustomitemwithvalue) |

# (1) FindByGroup

## Request

| Type | Name |
|------|------|
| uint32 | uiGroup |

## Response

| Type | Name |
|------|------|
| std_list<string> | lstTags |

# (2) InsertItem

## Request

| Type | Name |
|------|------|
| uint32 | uiGroup |
| string | strTag |
| buffer | bufData |
| bool | bReplace |

## Response

| Type | Name |
|------|------|
| bool | bResult |

# (3) RemoveItem

## Request

| Type | Name |
|------|------|
| uint32 | uiGroup |
| string | strTag |

## Response

| Type | Name |
|------|------|
| bool | bResult |

# (4) GetItem

## Request

| Type | Name |
|------|------|
| uint32 | uiGroup |
| string | strTag |

## Response

| Type | Name |
|------|------|
| buffer | bufData |
| bool | bResult |

# (5) InsertCustomItem

## Request

| Type | Name |
|------|------|
| uint32 | uiGroup |
| string | strTag |
| any<Data,string> | hData |
| bool | bReplace |

## Response
This method does not return anything.

# (6) GetCustomItem

## Request

| Type | Name |
|------|------|
| uint32 | uiGroup |
| string | strTag |

## Response

| Type | Name |
|------|------|
| any<Data,string> | hData |

# (7) FindItemsBySQLQuery

## Request

| Type | Name |
|------|------|
| uint32 | uiGroup |
| string | strTag |
| string | strQuery |

## Response

| Type | Name |
|------|------|
| std_list<any<Data,string>> | lstData |

# (8) InsertCustomItemWithValue

## Request

| Type | Name |
|------|------|
| uint32 | uiGroup |
| string | strTag |
| buffer | bufData |
| any<Data,string> | hData |
| bool | bReplace |

## Response
This method does not return anything.

# (9) GetCustomItemWithValue

## Request

| Type | Name |
|------|------|
| int32 | uiGroup |
| string | strTag |

## Response

| Type | Name |
|------|------|
| buffer | bufData |
| any<Data,string> | hData |

# Types

## StoreItem ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `Data`.

This class does not declare any variables.
