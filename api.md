# API

## Authentication

Except for [retrieving](api.md) one specific resource, authentication is mandatory to make any call to the API. For that, set the Headers `Authorization` of the request with a concatenation of `Bearer` and the [`token`](authentication.md) you have generated.

```javascript
Headers: {
  Authorization: Bearer + [JWT_TOKEN]
}
```

## Action

### Retrieve

{% tabs %}
{% tab title="GET" %}
`https://[domain].amaging.net/[cid]/Some/Path/to/some_file.jpg`
{% endtab %}

{% tab title="Headers" %}
```javascript
Headers: {
  Authorization: Bearer + [JWT_TOKEN]
}
```
{% endtab %}
{% endtabs %}

### List

{% tabs %}
{% tab title="GET" %}
`https://[domain].amaging.net/[cid]/Some/Path/`
{% endtab %}

{% tab title="Headers" %}
```javascript
Headers: {
  Authorization: Bearer + JWT_TOKEN
}
```
{% endtab %}

{% tab title="Response" %}
```javascript
[
  {"path":"/a","basename":"a","isDirectory":true,"ContentType":"application/x-directory","ContentLength":0,"ETag":"\"0\"","LastModified":"2018-09-07T08:58:29.000Z"},
  {"path":"/Picture.png","basename":"Picture.png","isDirectory":false,"ContentLength":37450,"ETag":"\"37450\"","LastModified":"2018-09-11T12:55:03.000Z","ContentType":"image/png"}
]
```
{% endtab %}
{% endtabs %}

### Modify / add a file

{% tabs %}
{% tab title="POST/PUT " %}
`https://[domain].amaging.net/[cid]/Some/Path/to/some_file.jpg`
{% endtab %}

{% tab title="Headers" %}
```javascript
Headers: {
  Content-Type: 'mime type of file',
  Content-Length: 'size of the file',
  Authorization: 'Bearer + [JWT_TOKEN]'
}
```
{% endtab %}
{% endtabs %}

### Add a folder

{% tabs %}
{% tab title="POST/PUT" %}
`https://[domain].amaging.net/[cid]/Some/Path/to/newFolder/`
{% endtab %}

{% tab title="Headers" %}
```javascript
Headers: {
  Authorization: Bearer + JWT_TOKEN
}
```
{% endtab %}

{% tab title="Response" %}
```javascript
{
  "success":true,
  "file": {"path":"/newFolder/","basename":"newFolder","isDirectory":true,"ContentType":"application/x-directory","ContentLength":0,"ETag":"\"0\"","LastModified":"2018-09-12T10:23:01.000Z"}
}
```
{% endtab %}
{% endtabs %}

### Delete

{% tabs %}
{% tab title="DELETE" %}
`https://[domain].amaging.net/[cid]/Some/Path/to/some_file.jpg`
{% endtab %}

{% tab title="Headers" %}
```javascript
Headers: {
  Authorization: Bearer + JWT_TOKEN
}
```
{% endtab %}

{% tab title="Response" %}
```javascript
{
  "success":true
}
```
{% endtab %}
{% endtabs %}

