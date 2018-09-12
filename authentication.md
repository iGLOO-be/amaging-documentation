# Authentication

## Access token / authentification

Authentication to Amaging is made via a [`JSON Web Token`](https://jwt.io/) using signing algorithm `HS256`. The JWT must contain **at least** the [`accessKey`](amaging.md) the Amaging team provided to you.

```json
{
  "accessKey": "[ACCESS_KEY]"
}
```

### Conditions

You can adjust the restrictions of the token with optional conditions, allowing \(or not\) specific action or access. By default, everything is permitted on every path.

Conditions can be declared in a `data` array:
```json
{
  "accessKey": "[ACCESS_KEY]",
  "data": [
    ["eq", "action", "create"],
    ["eq", "key", "some/key.jpg"]
  ]
}
```

This previous condition will only allow to create a file with key equal to `some/key.jpg`.

A condition is encoded as an `array`. The first value is the `validator`, the second is the `key` on which the validator is applied. The rest is the validator arguments.

#### Conditions validators

- `eq`
- `starts-with`
- `ends-with`
- `regex`
- `in`
- `range`

See [validators.js](https://github.com/iGLOO-be/amaging-policy/blob/master/src/lib/validators.js).

#### Conditions keys

- `action` (`create`/`update`/`delete`)
- `key`
- `Content-Length`
- `Content-Type`


## JWT Generation samples

- Node.js

```javascript
var jwt = require('jsonwebtoken');
var token = jwt.sign({ accessKey: [ACCESS_KEY] }, 'secret');
```

- PHP

```php
<?php

use \Firebase\JWT\JWT;

$secret = "secret";
$data = array(
    "accessKey" => [ACESS_KEY]
);

$token = JWT::encode($data, $secret);

?>
```

