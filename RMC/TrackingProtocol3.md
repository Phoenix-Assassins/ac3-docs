# TrackingProtocol3

| Method ID | Method Name |
|-----------|-------------|
| 1 | [SendTag](#1-sendtag) |
| 2 | [SendTagAndUpdateUserInfo](#2-sendtagandupdateuserinfo) |
| 3 | [SendUserInfo](#3-senduserinfo) |
| 4 | [GetConfiguration](#4-getconfiguration) |
| 5 | [SendTags](#5-sendtags) |

# (1) SendTag

## Request

| Type | Name |
|------|------|
| uint32 | trackingID |
| string | tag |
| string | attributes |
| uint32 | deltaTime |

## Response
This method does not return anything.

# (2) SendTagAndUpdateUserInfo

## Request

| Type | Name |
|------|------|
| uint32 | trackingID |
| string | tag |
| string | attributes |
| uint32 | deltaTime |
| string | userID |

## Response
This method does not return anything.

# (3) SendUserInfo

## Request

| Type | Name |
|------|------|
| TrackingInformation | userInfo |
| uint32 | deltaTime |

## Response

| Type | Name |
|------|------|
| TrackingInformation | userInfo |
| uint32 | trackingID |

# (4) GetConfiguration

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| std_list<string> | tags |

# (5) SendTags

## Request

| Type | Name |
|------|------|
| std_list<TrackingTag> | tagData |

## Response
This method does not return anything.

# Types

## TrackingInformation ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | ipn |
| string | userID |
| string | machineID |
| string | visitorID |
| string | utsVersion |

## TrackingTag ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | trackingID |
| string | tag |
| string | attributes |
| uint32 | deltaTime |
| string | newUserId |
