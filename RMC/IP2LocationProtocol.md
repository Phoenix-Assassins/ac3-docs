# IP2LocationProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetLocationFromIP](#1-getlocationfromip) |

# (1) GetLocationFromIP

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| IPLocation | location |

# Types

## IPLocation ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ipStart |
| string | m_countryCode |
| string | m_countryName |
| string | m_regionCode |
| string | m_regionName |
| string | m_cityName |
| float | m_latitude |
| float | m_longitude |
| uint32 | m_countryGeoCode |
| uint32 | m_regionGeoCode |
| uint32 | m_cityGeoCode |
