# ACOnlineSaveProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [WriteSave](#1-writesave) |
| 2 | [ReadSave](#2-readsave) |
| 3 | [WriteWebSave](#3-writewebsave) |
| 4 | [ReadWebSave](#4-readwebsave) |
| 5 | [TestServerSideWriteSave](#5-testserversidewritesave) |

# (1) WriteSave

## Request

| Type | Name |
|------|------|
| qBuffer | buffer |

## Response
This method does not return anything.

# (2) ReadSave

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| bool | dataRetrieved |
| qBuffer | bufferOut |

# (3) WriteWebSave

## Request

| Type | Name |
|------|------|
| string | username |
| string | buffer |

## Response

| Type | Name |
|------|------|
| bool | isSuccess |

# (4) ReadWebSave

## Request

| Type | Name |
|------|------|
| string | username |

## Response

| Type | Name |
|------|------|
| string | buffer |

# (5) TestServerSideWriteSave

## Request
This method does not take any parameters.

## Response
This method does not return anything.
