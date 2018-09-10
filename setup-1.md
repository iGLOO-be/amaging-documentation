---
description: How to install & configure Amaging
---

# Setup

## Client

[https://platform.amaging.net/client/client.js](https://platform.amaging.net/client/client.js)

## Instanciate client

```javascript
const client = AmagingClient.createClient({
    host: '', cid: '', access: '', token: 'jwt' ??? secret
})
```

| Options |  |
| :--- | :--- |
| host | sqd qd qsd  |
| cid | qsdsqdqsd |
| access |  |
| token |  |

{% hint style="info" %}
Token used for authentification
{% endhint %}

## Configure client

Different options can be set to configurate the client

```javascript
 client.showFinderDialog({
      startPath: '',
      restrictPath: '',
      title: '',
      onFileSelect (foile) {}
      onDialogOpen // advanced
    })
    .then(file => {
      // result instance of File // reference to File
    })
```

| Options |  |
| :--- | :--- |
| startPath | Folder where the user will arrive first opening amaging Finder Dialog, do not limit the access of the user.cid |
| title | Title of the Finder window |
| onFileSelect | Action to make when a file has been returned \(choosen by the user\) // reference to file |
| .then\(\) | Action to make when a file has been returned \(choosen by the user\), \(promise implementation\) // reference to file |

## File

Instance of a file returned by the client when a file has been chosen.

```javascript
{
    ContentLength: 206398
    ContentType: "application/octet-stream"
    ETag: ""90a7a02aaab76af19a203694773322a1""
    LastModified: "2018-09-03T15:47:32.000Z"
    isDirectory: false
    basename: "1.jpg"
    path: "/PuppyKitten/11/1.jpg"
    remotePath: "https://staging.amaging.net/main/PuppyKitten/11/1.jpg"
    represent () {}

```

| Key |  |
| :--- | :--- |
| represent\(\) | Method to create the url representation of the file |



