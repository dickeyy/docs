---
description: Endpoints for various time functions.
---

# Time

**Base URL**

```
https://api.dickey.gg/time
```

***

### /now

Returns the current server time in various formats

```
GET /now
```

> Example: `GET /time/now`

Response:

```typescript
{
    "time": {
        "unix": {
            "seconds": number,
            "ms": number
        },
        "utc": string,
        "local": string,
        "iso": string,
        "date": string,
        "time": string,
        "day" number,
        "month": number,
        "year": number,
        "hours": number,
        "minutes": number,
        "seconds": number,
        "milliseconds": number,
        "timezone": string,
        "timezoneName": string
    },
    "message": string
}
```

***

### /unix

Converts a unix timestamp (seconds) to various formats

```
GET /unix/:t
```

> Example: `GET /time/unix/1709884384`

#### Response:

```typescript
{
    "time": {
        "unix": {
            "seconds": number,
            "ms": number
        },
        "utc": string,
        "local": string,
        "iso": string,
        "date": string,
        "time": string,
        "day" number,
        "month": number,
        "year": number,
        "hours": number,
        "minutes": number,
        "seconds": number,
        "milliseconds": number,
        "timezone": string,
        "timezoneName": string
    },
    "message": string
}
```

***

### /unix/ms

Converts a unix timestamp (milliseconds) to various formats

```
GET /unix/ms/:t
```

> Example: `GET /time/unix/ms/1709884384193`

#### Response:

```typescript
{
    "time": {
        "unix": {
            "seconds": number,
            "ms": number
        },
        "utc": string,
        "local": string,
        "iso": string,
        "date": string,
        "time": string,
        "day" number,
        "month": number,
        "year": number,
        "hours": number,
        "minutes": number,
        "seconds": number,
        "milliseconds": number,
        "timezone": string,
        "timezoneName": string
    },
    "message": string
}
```

***
