# Mydex\ApiMrdSdk\ConditionsApi

Operations for retrieving and searching NHS Conditions content.

All URIs are relative to https://api-mrd.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getConditionLevelOne()**](ConditionsApi.md#getConditionLevelOne) | **GET** /conditions/{param1} | Retrieve a first-level Conditions page |
| [**getConditionLevelThree()**](ConditionsApi.md#getConditionLevelThree) | **GET** /conditions/{param1}/{param2}/{param3} | Retrieve a third-level Conditions page |
| [**getConditionLevelTwo()**](ConditionsApi.md#getConditionLevelTwo) | **GET** /conditions/{param1}/{param2} | Retrieve a second-level Conditions page |
| [**getConditionRoutes()**](ConditionsApi.md#getConditionRoutes) | **GET** /conditions | Retrieve available Conditions routes |
| [**searchConditions()**](ConditionsApi.md#searchConditions) | **GET** /conditions/search | Search Conditions content |


## `getConditionLevelOne()`

```php
getConditionLevelOne($x_mrd_scopes, $param1, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\ConditionResponse
```

Retrieve a first-level Conditions page

Returns a Conditions page identified by one route segment. The response may contain HTML by default. Use no_html to return processed plain text and nhs_links to return eligible original NHS URLs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ConditionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = conditions; // string | MRD service scope required for Conditions endpoints.
$param1 = adhd-adults; // string | First Conditions route segment.
$no_html = true; // string | Removes HTML markup from returned content. When supplied, this parameter must be set to 'true'.
$nhs_links = true; // string | Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to 'true'.

try {
    $result = $apiInstance->getConditionLevelOne($x_mrd_scopes, $param1, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConditionsApi->getConditionLevelOne: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Conditions endpoints. | [default to &#39;conditions&#39;] |
| **param1** | **string**| First Conditions route segment. | |
| **no_html** | **string**| Removes HTML markup from returned content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |
| **nhs_links** | **string**| Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\ConditionResponse**](../Model/ConditionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConditionLevelThree()`

```php
getConditionLevelThree($x_mrd_scopes, $param1, $param2, $param3, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\ConditionResponse
```

Retrieve a third-level Conditions page

Returns a Conditions page identified by three route segments. Responses may contain recursively nested web-page elements and video objects.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ConditionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = conditions; // string | MRD service scope required for Conditions endpoints.
$param1 = adhd-adults; // string | First Conditions route segment.
$param2 = help-and-support; // string | Second Conditions route segment.
$param3 = help-for-families; // string | Third Conditions route segment.
$no_html = true; // string | Removes HTML markup from returned content. When supplied, this parameter must be set to 'true'.
$nhs_links = true; // string | Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to 'true'.

try {
    $result = $apiInstance->getConditionLevelThree($x_mrd_scopes, $param1, $param2, $param3, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConditionsApi->getConditionLevelThree: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Conditions endpoints. | [default to &#39;conditions&#39;] |
| **param1** | **string**| First Conditions route segment. | |
| **param2** | **string**| Second Conditions route segment. | |
| **param3** | **string**| Third Conditions route segment. | |
| **no_html** | **string**| Removes HTML markup from returned content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |
| **nhs_links** | **string**| Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\ConditionResponse**](../Model/ConditionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConditionLevelTwo()`

```php
getConditionLevelTwo($x_mrd_scopes, $param1, $param2, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\ConditionResponse
```

Retrieve a second-level Conditions page

Returns a Conditions page identified by two route segments. The no_html and nhs_links parameters can be used separately or together.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ConditionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = conditions; // string | MRD service scope required for Conditions endpoints.
$param1 = adhd-adults; // string | First Conditions route segment.
$param2 = help-and-support; // string | Second Conditions route segment.
$no_html = true; // string | Removes HTML markup from returned content. When supplied, this parameter must be set to 'true'.
$nhs_links = true; // string | Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to 'true'.

try {
    $result = $apiInstance->getConditionLevelTwo($x_mrd_scopes, $param1, $param2, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConditionsApi->getConditionLevelTwo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Conditions endpoints. | [default to &#39;conditions&#39;] |
| **param1** | **string**| First Conditions route segment. | |
| **param2** | **string**| Second Conditions route segment. | |
| **no_html** | **string**| Removes HTML markup from returned content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |
| **nhs_links** | **string**| Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\ConditionResponse**](../Model/ConditionResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConditionRoutes()`

```php
getConditionRoutes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\ConditionsRouteListResponse
```

Retrieve available Conditions routes

Returns absolute URLs for the routes available in the NHS Conditions dataset.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ConditionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = conditions; // string | MRD service scope required for Conditions endpoints.

try {
    $result = $apiInstance->getConditionRoutes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConditionsApi->getConditionRoutes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Conditions endpoints. | [default to &#39;conditions&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\ConditionsRouteListResponse**](../Model/ConditionsRouteListResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchConditions()`

```php
searchConditions($x_mrd_scopes, $filters, $no_html, $nhs_links, $search_all): \Mydex\ApiMrdSdk\Model\ConditionsSearchResponse
```

Search Conditions content

Searches the NHS Conditions dataset. By default the search is performed against page descriptions. When search_all is enabled, page text and expander content are also searched. The no_html option removes HTML from textual content and nhs_links changes eligible MRD URLs to original NHS URLs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ConditionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = conditions; // string | MRD service scope required for Conditions endpoints.
$filters = array(new \Mydex\ApiMrdSdk\Model\\Mydex\ApiMrdSdk\Model\ConditionSearchFilter()); // \Mydex\ApiMrdSdk\Model\ConditionSearchFilter[] | Structured Conditions search filters supplied using indexed bracket notation, for example filters[0][operator]=LIKE&filters[0][value]=cancer&filters[0][condition]=AND&filters[1][operator]=LIKE&filters[1][value]=treatment&filters[1][condition]=. Each filter must contain exactly value, operator and condition.
$no_html = true; // string | Removes HTML markup from returned content. When supplied, this parameter must be set to 'true'.
$nhs_links = true; // string | Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to 'true'.
$search_all = true; // string | Extends Conditions search to page-content text and expander content in addition to the default page description. When supplied, this parameter must be set to 'true'. This parameter is only valid on the search endpoint.

try {
    $result = $apiInstance->searchConditions($x_mrd_scopes, $filters, $no_html, $nhs_links, $search_all);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConditionsApi->searchConditions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Conditions endpoints. | [default to &#39;conditions&#39;] |
| **filters** | [**\Mydex\ApiMrdSdk\Model\ConditionSearchFilter[]**](../Model/\Mydex\ApiMrdSdk\Model\ConditionSearchFilter.md)| Structured Conditions search filters supplied using indexed bracket notation, for example filters[0][operator]&#x3D;LIKE&amp;filters[0][value]&#x3D;cancer&amp;filters[0][condition]&#x3D;AND&amp;filters[1][operator]&#x3D;LIKE&amp;filters[1][value]&#x3D;treatment&amp;filters[1][condition]&#x3D;. Each filter must contain exactly value, operator and condition. | |
| **no_html** | **string**| Removes HTML markup from returned content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |
| **nhs_links** | **string**| Replaces eligible MRD URLs with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |
| **search_all** | **string**| Extends Conditions search to page-content text and expander content in addition to the default page description. When supplied, this parameter must be set to &#39;true&#39;. This parameter is only valid on the search endpoint. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\ConditionsSearchResponse**](../Model/ConditionsSearchResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
