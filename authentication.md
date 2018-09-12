---
description: How to auth in Amaging ?
---

# Authentification

## Access token / authentification

Authentication to Amaging is made via a [`JSON Web Token`](https://jwt.io/) using signing algorithm `HS256`. The JWT must contain **at least** the [`accessKey`](./amaging.md) the Amaging team provided to you.

```
{
    accessKey: ACCESS_KEY
}
```

You can adjust the restrictions of the token with optional conditions, allowing (or not) specific action or access.
By default, everything is permitted on every path.

TODO

```
{
    accessKey: ACCESS_KEY,
    data: [
        ['eq', 'key', value]
    ]
}
```


## Token Generation ???

sign from amaging-policy ???

