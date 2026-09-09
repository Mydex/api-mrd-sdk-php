# Mydex\ApiMrdSdk\LivewellApi

Operations for retrieving and searching NHS Live Well content.

All URIs are relative to https://api-mrd.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getLivewellLevelOne()**](LivewellApi.md#getLivewellLevelOne) | **GET** /live-well/{param-1} | Retrieve a first-level Live Well page |
| [**getLivewellLevelThree()**](LivewellApi.md#getLivewellLevelThree) | **GET** /live-well/{param-1}/{param-2}/{param-3} | Retrieve a third-level Live Well page |
| [**getLivewellLevelTwo()**](LivewellApi.md#getLivewellLevelTwo) | **GET** /live-well/{param-1}/{param-2} | Retrieve a second-level Live Well page |
| [**getLivewellRoutes()**](LivewellApi.md#getLivewellRoutes) | **GET** /live-well | Retrieve available Live Well routes |
| [**searchLivewell()**](LivewellApi.md#searchLivewell) | **GET** /live-well/search | Search Live Well content |


## `getLivewellLevelOne()`

```php
getLivewellLevelOne($x_mrd_scopes, $param1, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetLivewellLevelOne200Response
```

Retrieve a first-level Live Well page

Returns a first-level Live Well route. no_html removes HTML markup and nhs_links rewrites eligible MRD links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\LivewellApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = live-well; // string | MRD service scope required for Live Well endpoints.
$param1 = eat-well; // string | First Live Well route segment, normally identifying a top-level topic or category.
$no_html = true; // string | Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to 'true'.
$nhs_links = true; // string | Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to 'true'.

try {
    $result = $apiInstance->getLivewellLevelOne($x_mrd_scopes, $param1, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LivewellApi->getLivewellLevelOne: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Live Well endpoints. | [default to &#39;live-well&#39;] |
| **param1** | **string**| First Live Well route segment, normally identifying a top-level topic or category. | |
| **no_html** | **string**| Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |
| **nhs_links** | **string**| Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetLivewellLevelOne200Response**](../Model/GetLivewellLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLivewellLevelThree()`

```php
getLivewellLevelThree($x_mrd_scopes, $param1, $param2, $param3, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetLivewellLevelOne200Response
```

Retrieve a third-level Live Well page

Returns deeply nested Live Well content. The response uses the same flexible NHS page structure as first-level and second-level routes. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\LivewellApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = live-well; // string | MRD service scope required for Live Well endpoints.
$param1 = eat-well; // string | First Live Well route segment, normally identifying a top-level topic or category.
$param2 = food-types; // string | Second Live Well route segment, normally identifying a category or page within a top-level topic.
$param3 = milk-and-dairy-nutrition; // string | Third Live Well route segment, normally identifying a deeply nested page within a Live Well category.
$no_html = true; // string | Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to 'true'.
$nhs_links = true; // string | Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to 'true'.

try {
    $result = $apiInstance->getLivewellLevelThree($x_mrd_scopes, $param1, $param2, $param3, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LivewellApi->getLivewellLevelThree: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Live Well endpoints. | [default to &#39;live-well&#39;] |
| **param1** | **string**| First Live Well route segment, normally identifying a top-level topic or category. | |
| **param2** | **string**| Second Live Well route segment, normally identifying a category or page within a top-level topic. | |
| **param3** | **string**| Third Live Well route segment, normally identifying a deeply nested page within a Live Well category. | |
| **no_html** | **string**| Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |
| **nhs_links** | **string**| Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetLivewellLevelOne200Response**](../Model/GetLivewellLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLivewellLevelTwo()`

```php
getLivewellLevelTwo($x_mrd_scopes, $param1, $param2, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetLivewellLevelOne200Response
```

Retrieve a second-level Live Well page

Returns a second-level page or category within a Live Well topic. HTML and link behaviour can be controlled using no_html and nhs_links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\LivewellApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = live-well; // string | MRD service scope required for Live Well endpoints.
$param1 = eat-well; // string | First Live Well route segment, normally identifying a top-level topic or category.
$param2 = food-types; // string | Second Live Well route segment, normally identifying a category or page within a top-level topic.
$no_html = true; // string | Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to 'true'.
$nhs_links = true; // string | Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to 'true'.

try {
    $result = $apiInstance->getLivewellLevelTwo($x_mrd_scopes, $param1, $param2, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LivewellApi->getLivewellLevelTwo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Live Well endpoints. | [default to &#39;live-well&#39;] |
| **param1** | **string**| First Live Well route segment, normally identifying a top-level topic or category. | |
| **param2** | **string**| Second Live Well route segment, normally identifying a category or page within a top-level topic. | |
| **no_html** | **string**| Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |
| **nhs_links** | **string**| Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetLivewellLevelOne200Response**](../Model/GetLivewellLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLivewellRoutes()`

```php
getLivewellRoutes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\LivewellRoutesResponse
```

Retrieve available Live Well routes

Returns the available routes within the NHS Live Well dataset.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\LivewellApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = live-well; // string | MRD service scope required for Live Well endpoints.

try {
    $result = $apiInstance->getLivewellRoutes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LivewellApi->getLivewellRoutes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Live Well endpoints. | [default to &#39;live-well&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\LivewellRoutesResponse**](../Model/LivewellRoutesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchLivewell()`

```php
searchLivewell($x_mrd_scopes, $filters, $no_html, $nhs_links, $search_all): \Mydex\ApiMrdSdk\Model\LivewellData[]
```

Search Live Well content

Searches the NHS Live Well dataset using structured filters. By default filters search page descriptions. When search_all is enabled, page-content text is also searched.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\LivewellApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = live-well; // string | MRD service scope required for Live Well endpoints.
$filters = array(new \Mydex\ApiMrdSdk\Model\\Mydex\ApiMrdSdk\Model\LivewellSearchFilter()); // \Mydex\ApiMrdSdk\Model\LivewellSearchFilter[] | Structured Live Well search filters supplied using indexed bracket notation, for example filters[0][operator]=LIKE&filters[0][value]=healthy eating&filters[0][condition]=AND&filters[1][operator]=LIKE&filters[1][value]=diet&filters[1][condition]=. Each filter must contain exactly value, operator and condition.
$no_html = true; // string | Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to 'true'.
$nhs_links = true; // string | Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to 'true'.
$search_all = true; // string | Extends Live Well search to page-content text in addition to the default page description. When supplied, this parameter must be set to 'true'. This parameter is only valid on the search endpoint.

try {
    $result = $apiInstance->searchLivewell($x_mrd_scopes, $filters, $no_html, $nhs_links, $search_all);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LivewellApi->searchLivewell: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Live Well endpoints. | [default to &#39;live-well&#39;] |
| **filters** | [**\Mydex\ApiMrdSdk\Model\LivewellSearchFilter[]**](../Model/\Mydex\ApiMrdSdk\Model\LivewellSearchFilter.md)| Structured Live Well search filters supplied using indexed bracket notation, for example filters[0][operator]&#x3D;LIKE&amp;filters[0][value]&#x3D;healthy eating&amp;filters[0][condition]&#x3D;AND&amp;filters[1][operator]&#x3D;LIKE&amp;filters[1][value]&#x3D;diet&amp;filters[1][condition]&#x3D;. Each filter must contain exactly value, operator and condition. | |
| **no_html** | **string**| Removes HTML markup from returned Live Well content. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |
| **nhs_links** | **string**| Replaces eligible MRD API links with their NHS website equivalents. When supplied, this parameter must be set to &#39;true&#39;. | [optional] |
| **search_all** | **string**| Extends Live Well search to page-content text in addition to the default page description. When supplied, this parameter must be set to &#39;true&#39;. This parameter is only valid on the search endpoint. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\LivewellData[]**](../Model/LivewellData.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
