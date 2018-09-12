# Instanciate Client

With the Amaging Client comes a `createClient()` method, taking an object in params containing :

* `host <String>` Correspond to the host part of the url.
* `cid <String>` CID provided by the amaging team.
* `token <String>` Token used for [authentication](../authentication.md).

```javascript
const client = AmagingClient.createClient({
    host: 'http://[DOMAIN].amaging.net',
    cid: [CID],
    token: [JWT]
})
```

{% hint style="info" %}
See [Authentication](../authentication.md) for further explanation about the `token`
{% endhint %}

An instance of a Client has two properties:

| Property |  |
| :--- | :--- |
| `amagingOptions` | Containing all the options usefull to all the services : `host`, `cid`, `accessKey`, `secret`, `token` |
| [`showFinderDialog()`](finder_dialog.md) | method to start the Finder Dialog with optional configuration params. |

