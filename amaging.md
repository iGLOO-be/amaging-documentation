# Amaging

Any Amaging resources is identified by a well-known URL pattern:

```text
https://[domain].amaging.net/[cid]/[key]
```

The Amaging team will provide these informations:

| **Informations** | **Description** |
| :--- | :--- |
| **domain** | Every customer has a personnal domain name to access amaging. |
| **cid** | Every instance of amaging can use multiple cid's. By default, the first cid is named `main`. |
| **key** | The key is the path representing a resource in Amaging |
| **accessKey** | Public access key that will be used in integrations with various Amaging services. |
| **secretKey** | Secret key \(keep it safe!\) that will be used in integrations with various Amaging services. |

Here a sample of Amaging resource URI:

```text
https://staging.amaging.net/main/some/path/to/a/resource.jpg
```

