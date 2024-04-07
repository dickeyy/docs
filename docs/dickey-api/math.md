---
description: Endpoints for various math functions.
---

# Math

**Base URL:**

```
https://api.dickey.gg/math
```

***

### /prime

Calculates if `n` is a prime.

```
GET /prime/:n
```

> Example: `GET /math/prime/20`

#### **Response:**

```typescript
{
    "isPrime": boolean,
    "divisors": [
        number, number
    ],
    "message": string
}
```

#### **Constraints:**

* `n` must be > 1
* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /fibonacci

Calculates the first `n` digits in the Fibonacci Sequence

```
GET /fibonacci/:n
```

> Example: `GET /math/fibonacci/5`

#### Response:

```typescript
{
    "sequence": number[] (of size n),
    "message": string
}
```

#### Constraints:

* 0 < `n` < 1476
* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /random-number

Generates a random number between `x` and `y` (if `x` and `y` are omitted, `x=0 y=1000`)

```
GET /random-number?min=x&max=y
```

> Example: `GET /math/random-number?min=10&max=100`

#### Response:

```typescript
{
    "number": number,
    "message": string,
    "range": [x,y]
}
```

#### Constraints:

* `x (min)` < `y (max)`
* `x` and `y` must be numbers

#### Errors:

* `400`: Invalid parameter(s)

***

### /factorial

Calculates the factorial of `n` (`n!`)

```
GET /factorial/:n
```

> Example: `GET /math/factorial/5`

#### Response:

```typescript
{
    "number": number,
    "message": string
}
```

#### Constraints:

* 0 < `n` < 170
* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /sqrt

Calculates the square root of `n`

```
GET /sqrt/:n
```

> Example: `GET /math/sqrt/25`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` > 0
* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /abs

Calculates the absolute value of `n`

```
GET /abs/:n
```

> Example: `GET /math/abs/-5`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /round

Rounds `n` to the nearest integer

```
GET /round/:n
```

> Example: `GET /math/round/5.5`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /ceil

Rounds `n` up to the nearest integer

```
GET /ceil/:n
```

> Example: `GET /math/ceil/5.1`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /floor

Rounds `n` down to the nearest integer

```
GET /floor/:n
```

> Example: `GET /math/floor/5.9`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /sin

Calculates the sine of `n` (in radians)

```
GET /sin/:n
```

> Example: `GET /math/sin/0`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /cos

Calculates the cosine of `n` (in radians)

```
GET /cos/:n
```

> Example: `GET /math/cos/0`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /tan

Calculates the tangent of `n` (in radians)

```
GET /tan/:n
```

> Example: `GET /math/tan/0`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /log

Calculates the natural logarithm of `n`

```
GET /log/:n
```

> Example: `GET /math/log/10`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` > 0
* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /log10

Calculates the base 10 logarithm of `n`

```
GET /log10/:n
```

> Example: `GET /math/log10/10`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` > 0
* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /log2

Calculates the base 2 logarithm of `n`

```
GET /log2/:n
```

> Example: `GET /math/log2/10`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` > 0
* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /exp

Calculates `e` raised to the power of `n`

```
GET /exp/:n
```

> Example: `GET /math/exp/1`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `n` must be a number

#### Errors:

* `400`: Invalid parameter

***

### /pow

Calculates `x` raised to the power of `y`

```
GET /pow/?base=x&exponent=y
```

> Example: `GET /math/pow/?base=2&exponent=3`

#### Response:

```typescript
{
    "result": number,
    "message": string
}
```

#### Constraints:

* `x` and `y` must be numbers
* `x` and `y` must be present

#### Errors:

* `400`: Invalid parameter(s)

***
