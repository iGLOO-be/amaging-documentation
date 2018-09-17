# Client

## Install

`https://platform.amaging.net/v1/client/client.js`

Once script tag has been added it expose a global object `AmagingClient`.

## Code sample

Here is a sample of usage of `AmagingClient`: https://codesandbox.io/s/210z59319j

## Instanciate

With the Amaging Client comes a `AmagingClient.createClient()` method, taking an object in params containing :

| **Key** | **type** | **value** |
| :--- | :--- | :--- |
| `host` | `<string>` | Correspond to the host part of the url. |
| `cid` | `<string>` | CID provided by the amaging team. |
| `token` | `<string>` | Token used for [authentication](../authentication.md). |

```javascript
const client = AmagingClient.createClient({
    host: 'http://[domain].amaging.net',
    cid: [cid],
    token: [JWT]
})
```

{% hint style="info" %}
See [Authentication](../authentication.md) for further explanation about the `token`.
{% endhint %}

An instance of an `AmagingClient` has a property `finder` who expose a method [`showDialog`](finder_dialog.md), allowing you to to start a [`Finder Dialog`](finder_dialog.md) and browse your Amaging repository.

