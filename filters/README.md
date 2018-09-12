# Image processing

Amaging allows you to modify your images through a long [list of filters](./filters.md). They will be explained later with examples. Pretty easy to use, you just have to add filters in the URL to get the changes back to you. In the case you want to add differents filters to image, you have to use the'&' as delimiter at each end of the filter's name.

{% hint style="warning" %}
The filters are always located between the **scope\_id** and the **resource\_name** and should always end with an **&**.
{% endhint %}

## Supported image mime types list

* image/jpeg
* image/png
* image/gif
* image/bmp
* image/tiff
* image/x-jg

## URL components

Here is how the syntax of the URL works :

```json
https://[DOMAIN].amaging.net/[CID]/filter_1&filter_2&.../your_image.jpg
```

{% hint style="info" %}
In case of misusage of filters or if you miss the`'&'` delimiter, Amaging will fetch the default image.
{% endhint %}

