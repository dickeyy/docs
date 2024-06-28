---
description: Endpoints for various text manipulation functions.
---

# Text

**Base URL**

```
https://api.kyle.so/text
```

---

### /reverse

Reverses the input text (`x`)

```
GET /reverse?text=x
```

> Example: `GET /text/reverse?text=hello`

#### Response:

```typescript
{
    "reversed": string,
    "original": string
}
```

#### Errors:

-   `400`: No text provided

---

### /length

Returns the length of the input text (`x`)

```
GET /length?text=x
```

> Example: `GET /text/length?text=hello`

#### Response:

```typescript
{
    "length": {
        "characters": number,
        "words": number
    },
    "text": string
}
```

#### Errors:

-   `400`: No text provided

---

### /uppercase

Converts the input text (`x`) to uppercase

```
GET /uppercase?text=x
```

> Example: `GET /text/uppercase?text=hello`

#### Response:

```typescript
{
    "uppercase": string,
    "original": string
}
```

#### Errors:

-   `400`: No text provided

---

### /lowercase

Converts the input text (`x`) to lowercase

```
GET /lowercase?text=x
```

> Example: `GET /text/lowercase?text=HELLO`

#### Response:

```typescript
{
    "lowercase": string,
    "original": string
}
```

#### Errors:

-   `400`: No text provided

---

### /replace

Replaces all occurrences of `search` with `replace` in the input text (`x`)

```
GET /replace?text=x&search=y&replace=z
```

> Example: `GET /text/replace?text=hello&search=he&replace=no`

#### Response:

```typescript
{
    "replaced": string,
    "original": string
}
```

#### Errors:

-   `400`: No text provided

---

### /lorem

Generates `x` words of lorem ipsum text

```
GET /lorem?length=x
```

> Example: `GET /text/lorem?length=10`

#### Response:

```typescript
{
    "lorem": string,
    "length": number
}
```

#### Constraints:

-   0 < `x` < 2000

#### Errors:

-   `400`: Invalid parameter

---
