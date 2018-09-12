# File

In Amaging, an instance of a file returned by the Dialog is composed by :

| key | description |
| :--- | :--- |
| `ContentLength` | The file content-length. |
| `ContentType` | The file mime type. |
| `ETag` | The file ETag. |
| `LastModified` | Timestampt of the last time the file was modified. |
| `isDirectory` | Is the file a direcotry or not. |
| `basename` | File name. |
| `path` | Relative path, relative to the `[CID]` folder. |
| `remotePath` | Absolute public path of the file |
| `represent() {}` | a method returning the url representation of the file |

{% hint style="info" %}
`options()`it's possible to chain represent with `option` method to add an array of Amaging [Filter](../filters/filters.md) to the url of the file.
{% endhint %}

```javascript
const file = {
    ContentLength: 206398
    ContentType: "application/octet-stream"
    ETag: ""90a7a02aaab76af19a203694773322a1""
    LastModified: "2018-09-03T15:47:32.000Z"
    isDirectory: false
    basename: "some_file.jpg"
    path: "/Some/Path/to/some_file.jpg"
    remotePath: "https://[DOMAIN].amaging.net/[CID]/Some/Path/to/some_file.jpg"
}

...

file.represent().options('1000', 'blur(100,20)').toString()
// https://[DOMAIN].amaging.net/[CID]/100&blur(100,20)&/Some/Path/to/some_file.jpg
```

