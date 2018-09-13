# Finder Dialog

## showDialog\(\[options\]\)

The `showDialog` method accept several options:

| Options | Type |  |
| :--- | :--- | :--- |
| `startPath` | `<string>` | Key prefix that define the starting folder when opening `Finder Dialog`. **Do not limit the access of the parent folder.** |
| `restrictPath` | `<string>` | Key prefix that define the starting folder when opening `Finder Dialog` if no `startPath`. Limit the access exclusively to this folder and its subfolder. |
| `title` | `<string>` | Title of the `Finder Dialog` window. |
| `onFileSelect` | `<function>` | A [file](file.md) selected in the `Finder Dialog` will be passed to this function. As `showDialog` return a promise, you could also chain it with `.then()` to execute something with the received [file](file.md). |
| `onDialogOpen` | `<function>` | Advanced feature |

{% hint style="info" %}
`startPath` and `restrictPath` can be combined. However if `restrictPath` point to a more specific folder than `startPath`, then `startPath` will be ignored.

Ex: if `startPath = '/a/b'` and `restrictPath = '/a/b/c'` then `Finder Dialog` will open in folder `c` and folders `a` and `b` won't be accessible.
{% endhint %}

```javascript
  client.finder.showDialog({
    startPath: '/a/b/c',
    restrictPath: '/a',
    title: 'My Finder Dialog',
    onDialogOpen, // advanced feature

    onFileSelect: file => {
      // Make something with File choose from `onFileSelect`'
    }
  })

  .then(file => {
    // Same as `onFileSelect`
  })
```

