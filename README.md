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


##### Search Shodan

```php
$shodan = new Shodan('apikey');
$host_info = $shodan->host('127.0.0.1');
```


##### Return the total number of results that match the query and any facet information.

```php
$shodan = new Shodan('apikey');
$count = $shodan->host_count('127.0.0.1');
```


##### Determine which filters are being used by the query string and what parameters were provided to the filters.

```php
$shodan = new Shodan('apikey');
$search = token_search('xxx');
```


##### Return an object containing all the services that the Shodan crawlers look at.

```php
$shodan = new Shodan('apikey');
$services = $shodan->services();
```


##### Look up the IP address for the provided list of hostnames.

```php
$shodan = new Shodan('apikey');
$resolve = $shodan->dns_resolve('shodanhq.com');
```

##### Look up the hostnames that have been defined for the given list of IP addresses.

```php
$shodan = new Shodan('apikey');
$reverse = $shodan->dns_reverse('shodanhq.com');
```

##### Returns your current IP address as seen from the Internet.

```php
$shodan = new Shodan('apikey');
$ip = $shodan->myip();
```


##### Returns information about the API plan belonging to the given API key.

```php
$shodan = new Shodan('apikey');
$info = $shodan->api_info();
```


##### Return all of the data that Shodan collects.

```php
$shodan = new Shodan('apikey');
$banners = $shodan->banners();
```


##### Return geolocation data for all of the collected data by Shodan
