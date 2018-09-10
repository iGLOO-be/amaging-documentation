# API

## Representation

[https://`customer_id`.amaging.net/`scope_id`/presentation.pdf](https://customer_id.amaging.net/scope_id/presentation.pdf)

| param |  |
| :--- | :--- |
| customer\_id | sqdqsdsqd |
| scope\_id | sqdsqdsqd |

## Action

### Retrieve

{% tabs %}
{% tab title="Method" %}
`GET` [`https://customer_id.amaging.net/scope_id/presentation.pdf`](https://customer_id.amaging.net/scope_id/presentation.pdf)\`\`
{% endtab %}

{% tab title="Headers" %}
```javascript
Headers: {
    Authorization: Bearer + JWT_TOKEN // reference to authentification
}
```
{% endtab %}
{% endtabs %}

### Modify

{% tabs %}
{% tab title="Method" %}
`GET` [`https://customer_id.amaging.net/scope_id/presentation.pdf`](https://customer_id.amaging.net/scope_id/presentation.pdf)\`\`
{% endtab %}

{% tab title="Headers" %}
```javascript
Headers: {
     Content-Type: mime type of file,
     Content-Length: size of the file,
     Authorization: Bearer + JWT_TOKEN // reference to authentification
   }
```
{% endtab %}
{% endtabs %}

### Delete

{% tabs %}
{% tab title="Method" %}
`GET` [`https://customer_id.amaging.net/scope_id/presentation.pdf`](https://customer_id.amaging.net/scope_id/presentation.pdf)\`\`
{% endtab %}

{% tab title="Headers" %}
```javascript
 Headers: {
       Authorization: Bearer + JWT_TOKEN // reference to authentification
     }
```
{% endtab %}
{% endtabs %}
