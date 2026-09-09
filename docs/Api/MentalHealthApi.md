# Mydex\ApiMrdSdk\MentalHealthApi



All URIs are relative to https://api-mrd.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getMentalHealthLevelFour()**](MentalHealthApi.md#getMentalHealthLevelFour) | **GET** /mental-health/{param1}/{param2}/{param3}/{param4} | Retrieve deeply nested Mental Health content |
| [**getMentalHealthLevelOne()**](MentalHealthApi.md#getMentalHealthLevelOne) | **GET** /mental-health/{param1} | Retrieve a Mental Health page |
| [**getMentalHealthLevelThree()**](MentalHealthApi.md#getMentalHealthLevelThree) | **GET** /mental-health/{param1}/{param2}/{param3} | Retrieve nested Mental Health content |
| [**getMentalHealthLevelTwo()**](MentalHealthApi.md#getMentalHealthLevelTwo) | **GET** /mental-health/{param1}/{param2} | Retrieve a Mental Health subcategory |
| [**getMentalHealthRoutes()**](MentalHealthApi.md#getMentalHealthRoutes) | **GET** /mental-health | Retrieve available Mental Health routes |
| [**searchMentalHealth()**](MentalHealthApi.md#searchMentalHealth) | **GET** /mental-health/search | Search Mental Health content |


## `getMentalHealthLevelFour()`

```php
getMentalHealthLevelFour($x_mrd_scopes, $param1, $param2, $param3, $param4, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetMentalHealthLevelOne200Response
```

Retrieve deeply nested Mental Health content

Returns a fourth-level Mental Health route. no_html=true removes HTML markup and nhs_links=true rewrites eligible MRD API links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MentalHealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = mental-health; // string | MRD service scope required for Mental Health endpoints.
$param1 = feelings-symptoms-behaviours; // string | First Mental Health route segment, normally identifying a Mental Health topic, category or section.
$param2 = feelings-and-symptoms; // string | Second Mental Health route segment, normally identifying a category or page within a Mental Health topic.
$param3 = stress; // string | Third Mental Health route segment identifying a nested Mental Health page.
$param4 = getting-help; // string | Fourth Mental Health route segment identifying deeply nested Mental Health content.
$no_html = true; // string | When supplied, removes HTML markup from returned Mental Health content. The only accepted value is 'true'. Omit the parameter to retain HTML.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.

try {
    $result = $apiInstance->getMentalHealthLevelFour($x_mrd_scopes, $param1, $param2, $param3, $param4, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MentalHealthApi->getMentalHealthLevelFour: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;] |
| **param1** | **string**| First Mental Health route segment, normally identifying a Mental Health topic, category or section. | |
| **param2** | **string**| Second Mental Health route segment, normally identifying a category or page within a Mental Health topic. | |
| **param3** | **string**| Third Mental Health route segment identifying a nested Mental Health page. | |
| **param4** | **string**| Fourth Mental Health route segment identifying deeply nested Mental Health content. | |
| **no_html** | **string**| When supplied, removes HTML markup from returned Mental Health content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetMentalHealthLevelOne200Response**](../Model/GetMentalHealthLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMentalHealthLevelOne()`

```php
getMentalHealthLevelOne($x_mrd_scopes, $param1, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetMentalHealthLevelOne200Response
```

Retrieve a Mental Health page

Returns a first-level Mental Health route. no_html=true removes HTML markup and nhs_links=true rewrites eligible MRD API links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MentalHealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = mental-health; // string | MRD service scope required for Mental Health endpoints.
$param1 = feelings-symptoms-behaviours; // string | First Mental Health route segment, normally identifying a Mental Health topic, category or section.
$no_html = true; // string | When supplied, removes HTML markup from returned Mental Health content. The only accepted value is 'true'. Omit the parameter to retain HTML.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.

try {
    $result = $apiInstance->getMentalHealthLevelOne($x_mrd_scopes, $param1, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MentalHealthApi->getMentalHealthLevelOne: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;] |
| **param1** | **string**| First Mental Health route segment, normally identifying a Mental Health topic, category or section. | |
| **no_html** | **string**| When supplied, removes HTML markup from returned Mental Health content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetMentalHealthLevelOne200Response**](../Model/GetMentalHealthLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMentalHealthLevelThree()`

```php
getMentalHealthLevelThree($x_mrd_scopes, $param1, $param2, $param3, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetMentalHealthLevelOne200Response
```

Retrieve nested Mental Health content

Returns a third-level Mental Health page. no_html=true removes HTML markup and nhs_links=true rewrites eligible MRD API links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MentalHealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = mental-health; // string | MRD service scope required for Mental Health endpoints.
$param1 = feelings-symptoms-behaviours; // string | First Mental Health route segment, normally identifying a Mental Health topic, category or section.
$param2 = feelings-and-symptoms; // string | Second Mental Health route segment, normally identifying a category or page within a Mental Health topic.
$param3 = stress; // string | Third Mental Health route segment identifying a nested Mental Health page.
$no_html = true; // string | When supplied, removes HTML markup from returned Mental Health content. The only accepted value is 'true'. Omit the parameter to retain HTML.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.

try {
    $result = $apiInstance->getMentalHealthLevelThree($x_mrd_scopes, $param1, $param2, $param3, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MentalHealthApi->getMentalHealthLevelThree: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;] |
| **param1** | **string**| First Mental Health route segment, normally identifying a Mental Health topic, category or section. | |
| **param2** | **string**| Second Mental Health route segment, normally identifying a category or page within a Mental Health topic. | |
| **param3** | **string**| Third Mental Health route segment identifying a nested Mental Health page. | |
| **no_html** | **string**| When supplied, removes HTML markup from returned Mental Health content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetMentalHealthLevelOne200Response**](../Model/GetMentalHealthLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMentalHealthLevelTwo()`

```php
getMentalHealthLevelTwo($x_mrd_scopes, $param1, $param2, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetMentalHealthLevelOne200Response
```

Retrieve a Mental Health subcategory

Returns a second-level Mental Health route. no_html=true removes HTML markup and nhs_links=true rewrites eligible MRD API links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MentalHealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = mental-health; // string | MRD service scope required for Mental Health endpoints.
$param1 = feelings-symptoms-behaviours; // string | First Mental Health route segment, normally identifying a Mental Health topic, category or section.
$param2 = feelings-and-symptoms; // string | Second Mental Health route segment, normally identifying a category or page within a Mental Health topic.
$no_html = true; // string | When supplied, removes HTML markup from returned Mental Health content. The only accepted value is 'true'. Omit the parameter to retain HTML.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.

try {
    $result = $apiInstance->getMentalHealthLevelTwo($x_mrd_scopes, $param1, $param2, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MentalHealthApi->getMentalHealthLevelTwo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;] |
| **param1** | **string**| First Mental Health route segment, normally identifying a Mental Health topic, category or section. | |
| **param2** | **string**| Second Mental Health route segment, normally identifying a category or page within a Mental Health topic. | |
| **no_html** | **string**| When supplied, removes HTML markup from returned Mental Health content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetMentalHealthLevelOne200Response**](../Model/GetMentalHealthLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMentalHealthRoutes()`

```php
getMentalHealthRoutes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MentalHealthRoutesResponse
```

Retrieve available Mental Health routes

Returns the available routes within the NHS Mental Health dataset.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MentalHealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = mental-health; // string | MRD service scope required for Mental Health endpoints.

try {
    $result = $apiInstance->getMentalHealthRoutes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MentalHealthApi->getMentalHealthRoutes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MentalHealthRoutesResponse**](../Model/MentalHealthRoutesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchMentalHealth()`

```php
searchMentalHealth($x_mrd_scopes, $filters, $no_html, $nhs_links, $search_all): \Mydex\ApiMrdSdk\Model\MentalHealthData[]
```

Search Mental Health content

Searches the NHS Mental Health dataset using structured filters. By default filters search the page description. search_all=true additionally searches page-content text and expander-group content.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MentalHealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = mental-health; // string | MRD service scope required for Mental Health endpoints.
$filters = array(new \Mydex\ApiMrdSdk\Model\\Mydex\ApiMrdSdk\Model\MentalHealthSearchFilter()); // \Mydex\ApiMrdSdk\Model\MentalHealthSearchFilter[] | Structured Mental Health search filters supplied using indexed bracket notation, for example filters[0][value]=depression&filters[0][operator]=LIKE&filters[0][condition]=. Each filter must contain value, operator and condition. By default the search checks the page description. search_all=true additionally searches page-content text and expander-group content.
$no_html = true; // string | When supplied, removes HTML markup from returned Mental Health content. The only accepted value is 'true'. Omit the parameter to retain HTML.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
$search_all = true; // string | When supplied, the search also checks page-content text and expander-group content in addition to the page description. The only accepted value is 'true'. This parameter is only valid on the search endpoint.

try {
    $result = $apiInstance->searchMentalHealth($x_mrd_scopes, $filters, $no_html, $nhs_links, $search_all);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MentalHealthApi->searchMentalHealth: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Mental Health endpoints. | [default to &#39;mental-health&#39;] |
| **filters** | [**\Mydex\ApiMrdSdk\Model\MentalHealthSearchFilter[]**](../Model/\Mydex\ApiMrdSdk\Model\MentalHealthSearchFilter.md)| Structured Mental Health search filters supplied using indexed bracket notation, for example filters[0][value]&#x3D;depression&amp;filters[0][operator]&#x3D;LIKE&amp;filters[0][condition]&#x3D;. Each filter must contain value, operator and condition. By default the search checks the page description. search_all&#x3D;true additionally searches page-content text and expander-group content. | |
| **no_html** | **string**| When supplied, removes HTML markup from returned Mental Health content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |
| **search_all** | **string**| When supplied, the search also checks page-content text and expander-group content in addition to the page description. The only accepted value is &#39;true&#39;. This parameter is only valid on the search endpoint. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MentalHealthData[]**](../Model/MentalHealthData.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
