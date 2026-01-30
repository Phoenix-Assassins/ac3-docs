# OfflineGameNotificationsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [PollNotifications](#1-pollnotifications) |

# (1) PollNotifications

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| qlist<NotificationEvent> | listNotifications |
| int32 | ret |

## NotificationEvent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_pidSource |
| uint32 | m_uiType |
| uint32 | m_uiParam1 |
| uint32 | m_uiParam2 |
| string | m_strParam |
| uint32 | m_uiParam3 |
