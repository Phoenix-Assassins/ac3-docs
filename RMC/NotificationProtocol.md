# NotificationProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [ProcessNotificationEvent](#1-processnotificationevent) |

# (1) ProcessNotificationEvent

## Request

| Type | Name |
|------|------|
| NotificationEvent | oEvent |

## Response
This method does not return anything.

# Types

## NotificationEvent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_pidSource |
| uint32 | m_uiType |
| uint32 | m_uiParam1 |
| uint32 | m_uiParam2 |
| string | m_strParam |
| uint32 | m_uiParam3 |