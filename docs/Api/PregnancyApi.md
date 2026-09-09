# Mydex\ApiMrdSdk\PregnancyApi

Operations for retrieving and searching NHS Pregnancy content.

All URIs are relative to https://api-mrd.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getPregnancyLevelOne()**](PregnancyApi.md#getPregnancyLevelOne) | **GET** /pregnancy/{param1} | Retrieve a Pregnancy page |
| [**getPregnancyLevelThree()**](PregnancyApi.md#getPregnancyLevelThree) | **GET** /pregnancy/{param1}/{param2}/{param3} | Retrieve deeply nested Pregnancy content |
| [**getPregnancyLevelTwo()**](PregnancyApi.md#getPregnancyLevelTwo) | **GET** /pregnancy/{param1}/{param2} | Retrieve a Pregnancy subpage |
| [**getPregnancyRoutes()**](PregnancyApi.md#getPregnancyRoutes) | **GET** /pregnancy | Retrieve available Pregnancy routes |
| [**searchPregnancy()**](PregnancyApi.md#searchPregnancy) | **GET** /pregnancy/search | Search Pregnancy content |


## `getPregnancyLevelOne()`

```php
getPregnancyLevelOne($x_mrd_scopes, $param1, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetPregnancyLevelOne200Response
```

Retrieve a Pregnancy page

Returns a first-level Pregnancy route. no_html=true removes HTML markup, while nhs_links=true rewrites eligible MRD API URLs to NHS website URLs. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\PregnancyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = pregnancy; // string | MRD service scope required for Pregnancy endpoints.
$param1 = keeping-well; // string | First Pregnancy route segment, normally identifying a Pregnancy topic, category or section.
$no_html = true; // string | When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is 'true'. Omit the parameter to retain HTML.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.

try {
    $result = $apiInstance->getPregnancyLevelOne($x_mrd_scopes, $param1, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PregnancyApi->getPregnancyLevelOne: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Pregnancy endpoints. | [default to &#39;pregnancy&#39;] |
| **param1** | **string**| First Pregnancy route segment, normally identifying a Pregnancy topic, category or section. | |
| **no_html** | **string**| When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetPregnancyLevelOne200Response**](../Model/GetPregnancyLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPregnancyLevelThree()`

```php
getPregnancyLevelThree($x_mrd_scopes, $param1, $param2, $param3, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetPregnancyLevelOne200Response
```

Retrieve deeply nested Pregnancy content

Returns a third-level Pregnancy route. no_html=true removes HTML markup, while nhs_links=true rewrites eligible MRD API URLs to NHS website URLs. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\PregnancyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = pregnancy; // string | MRD service scope required for Pregnancy endpoints.
$param1 = keeping-well; // string | First Pregnancy route segment, normally identifying a Pregnancy topic, category or section.
$param2 = pregnancy-and-covid-19; // string | Second Pregnancy route segment, normally identifying a page within a Pregnancy topic.
$param3 = 4-weeks; // string | Third Pregnancy route segment identifying a deeply nested Pregnancy page, such as a specific pregnancy week or page within a nested category.
$no_html = true; // string | When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is 'true'. Omit the parameter to retain HTML.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.

try {
    $result = $apiInstance->getPregnancyLevelThree($x_mrd_scopes, $param1, $param2, $param3, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PregnancyApi->getPregnancyLevelThree: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Pregnancy endpoints. | [default to &#39;pregnancy&#39;] |
| **param1** | **string**| First Pregnancy route segment, normally identifying a Pregnancy topic, category or section. | |
| **param2** | **string**| Second Pregnancy route segment, normally identifying a page within a Pregnancy topic. | |
| **param3** | **string**| Third Pregnancy route segment identifying a deeply nested Pregnancy page, such as a specific pregnancy week or page within a nested category. | |
| **no_html** | **string**| When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetPregnancyLevelOne200Response**](../Model/GetPregnancyLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPregnancyLevelTwo()`

```php
getPregnancyLevelTwo($x_mrd_scopes, $param1, $param2, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetPregnancyLevelOne200Response
```

Retrieve a Pregnancy subpage

Returns a second-level page within a Pregnancy topic. no_html=true removes HTML markup, while nhs_links=true rewrites eligible MRD API URLs to NHS website URLs. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\PregnancyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = pregnancy; // string | MRD service scope required for Pregnancy endpoints.
$param1 = keeping-well; // string | First Pregnancy route segment, normally identifying a Pregnancy topic, category or section.
$param2 = pregnancy-and-covid-19; // string | Second Pregnancy route segment, normally identifying a page within a Pregnancy topic.
$no_html = true; // string | When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is 'true'. Omit the parameter to retain HTML.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.

try {
    $result = $apiInstance->getPregnancyLevelTwo($x_mrd_scopes, $param1, $param2, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PregnancyApi->getPregnancyLevelTwo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Pregnancy endpoints. | [default to &#39;pregnancy&#39;] |
| **param1** | **string**| First Pregnancy route segment, normally identifying a Pregnancy topic, category or section. | |
| **param2** | **string**| Second Pregnancy route segment, normally identifying a page within a Pregnancy topic. | |
| **no_html** | **string**| When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetPregnancyLevelOne200Response**](../Model/GetPregnancyLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPregnancyRoutes()`

```php
getPregnancyRoutes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\PregnancyRoutesResponse
```

Retrieve available Pregnancy routes

Returns the available routes within the NHS Pregnancy dataset.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\PregnancyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = pregnancy; // string | MRD service scope required for Pregnancy endpoints.

try {
    $result = $apiInstance->getPregnancyRoutes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PregnancyApi->getPregnancyRoutes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Pregnancy endpoints. | [default to &#39;pregnancy&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\PregnancyRoutesResponse**](../Model/PregnancyRoutesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchPregnancy()`

```php
searchPregnancy($x_mrd_scopes, $filters, $no_html, $nhs_links, $search_all): \Mydex\ApiMrdSdk\Model\PregnancyData[]
```

Search Pregnancy content

Searches the NHS Pregnancy dataset using structured filters. By default each filter searches the page description. When search_all=true, the search additionally checks page-content text and expander-group content. no_html removes HTML markup from returned content and nhs_links rewrites eligible MRD API links to NHS website links.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\PregnancyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = pregnancy; // string | MRD service scope required for Pregnancy endpoints.
$filters = array(new \Mydex\ApiMrdSdk\Model\\Mydex\ApiMrdSdk\Model\PregnancySearchFilter()); // \Mydex\ApiMrdSdk\Model\PregnancySearchFilter[] | Structured Pregnancy search filters supplied using indexed bracket notation, for example filters[0][value]=antenatal appointments&filters[0][operator]=LIKE&filters[0][condition]=. Each filter must contain exactly value, operator and condition.
$no_html = true; // string | When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is 'true'. Omit the parameter to retain HTML.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
$search_all = true; // string | When supplied, the search also checks Pregnancy page-content text and expander-group content in addition to the page description. The only accepted value is 'true'. This parameter is only valid on the search endpoint.

try {
    $result = $apiInstance->searchPregnancy($x_mrd_scopes, $filters, $no_html, $nhs_links, $search_all);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PregnancyApi->searchPregnancy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Pregnancy endpoints. | [default to &#39;pregnancy&#39;] |
| **filters** | [**\Mydex\ApiMrdSdk\Model\PregnancySearchFilter[]**](../Model/\Mydex\ApiMrdSdk\Model\PregnancySearchFilter.md)| Structured Pregnancy search filters supplied using indexed bracket notation, for example filters[0][value]&#x3D;antenatal appointments&amp;filters[0][operator]&#x3D;LIKE&amp;filters[0][condition]&#x3D;. Each filter must contain exactly value, operator and condition. | |
| **no_html** | **string**| When supplied, removes HTML markup from returned Pregnancy content. The only accepted value is &#39;true&#39;. Omit the parameter to retain HTML. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |
| **search_all** | **string**| When supplied, the search also checks Pregnancy page-content text and expander-group content in addition to the page description. The only accepted value is &#39;true&#39;. This parameter is only valid on the search endpoint. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\PregnancyData[]**](../Model/PregnancyData.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
