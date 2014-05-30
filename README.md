shodan-rest-api-wrapper
=======================

Up-to-date Shodan REST API wrapper.


### Notes

* Each function's return type can be changed by defining RETURN_TYPE to your liking (true = object; false = array)
* Each function is appropriately documented with php-documentor formatting.
* If you're in search of better and more thorough documentation, please refer to Shodan's REST API documentation (https://developer.shodan.io/api).
* For the functions that require subscriptions (banners(), geo() and ports()), refer to Shodan's STREAM API documentation (https://developer.shodan.io/api/stream)


### Usage

##### Search hosts

```php
$shodan = new Shodan('apikey');
$search = $shodan->host_search('NASA');
$search = $shodan->host_search('NASA', 2); // Retrieves results from page 2.
```

##### Retrieve host information

```php
$shodan = new Shodan('apikey');
$host_info = $shodan->host('127.0.0.1');
```
