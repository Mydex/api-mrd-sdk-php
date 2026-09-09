# Mydex\ApiMrdSdk\MedicinesApi

Operations for retrieving and searching NHS Medicines content.

All URIs are relative to https://api-mrd.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getMedicineLevelOne()**](MedicinesApi.md#getMedicineLevelOne) | **GET** /medicines/{param1} | Retrieve a Medicine page |
| [**getMedicineLevelThree()**](MedicinesApi.md#getMedicineLevelThree) | **GET** /medicines/{param1}/{param2}/{param3} | Retrieve a page within a nested Medicine |
| [**getMedicineLevelTwo()**](MedicinesApi.md#getMedicineLevelTwo) | **GET** /medicines/{param1}/{param2} | Retrieve a Medicine subpage or nested medicine |
| [**getMedicinesRoutes()**](MedicinesApi.md#getMedicinesRoutes) | **GET** /medicines | Retrieve available Medicines routes |
| [**searchMedicines()**](MedicinesApi.md#searchMedicines) | **GET** /medicines/search | Search Medicines content |


## `getMedicineLevelOne()`

```php
getMedicineLevelOne($x_mrd_scopes, $param1, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetMedicineLevelOne200Response
```

Retrieve a Medicine page

Returns a first-level Medicines page. HTML content is returned by default. no_html removes markup, while nhs_links rewrites eligible MRD links to NHS website links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MedicinesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = medicines; // string | MRD service scope required for Medicines endpoints.
$param1 = insulin; // string | First Medicines route segment, normally identifying a medicine, medicine category or medicine family.
$no_html = true; // string | When supplied, removes HTML markup from content text. The only accepted value is 'true'. Omit the parameter to leave HTML unchanged.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.

try {
    $result = $apiInstance->getMedicineLevelOne($x_mrd_scopes, $param1, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MedicinesApi->getMedicineLevelOne: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Medicines endpoints. | [default to &#39;medicines&#39;] |
| **param1** | **string**| First Medicines route segment, normally identifying a medicine, medicine category or medicine family. | |
| **no_html** | **string**| When supplied, removes HTML markup from content text. The only accepted value is &#39;true&#39;. Omit the parameter to leave HTML unchanged. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetMedicineLevelOne200Response**](../Model/GetMedicineLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMedicineLevelThree()`

```php
getMedicineLevelThree($x_mrd_scopes, $param1, $param2, $param3, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetMedicineLevelOne200Response
```

Retrieve a page within a nested Medicine

Returns a third-level Medicines route. These responses use the same flexible NHS page structure as other Medicines routes and may include nested question and answer content. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MedicinesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = medicines; // string | MRD service scope required for Medicines endpoints.
$param1 = insulin; // string | First Medicines route segment, normally identifying a medicine, medicine category or medicine family.
$param2 = rapid-acting-insulin; // string | Second Medicines route segment, normally identifying a medicine page or a medicine within a broader medicine family.
$param3 = common-questions-about-rapid-acting-insulin; // string | Third Medicines route segment identifying a page within a nested medicine, such as common questions, dosage, side effects or interactions.
$no_html = true; // string | When supplied, removes HTML markup from content text. The only accepted value is 'true'. Omit the parameter to leave HTML unchanged.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.

try {
    $result = $apiInstance->getMedicineLevelThree($x_mrd_scopes, $param1, $param2, $param3, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MedicinesApi->getMedicineLevelThree: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Medicines endpoints. | [default to &#39;medicines&#39;] |
| **param1** | **string**| First Medicines route segment, normally identifying a medicine, medicine category or medicine family. | |
| **param2** | **string**| Second Medicines route segment, normally identifying a medicine page or a medicine within a broader medicine family. | |
| **param3** | **string**| Third Medicines route segment identifying a page within a nested medicine, such as common questions, dosage, side effects or interactions. | |
| **no_html** | **string**| When supplied, removes HTML markup from content text. The only accepted value is &#39;true&#39;. Omit the parameter to leave HTML unchanged. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetMedicineLevelOne200Response**](../Model/GetMedicineLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMedicineLevelTwo()`

```php
getMedicineLevelTwo($x_mrd_scopes, $param1, $param2, $no_html, $nhs_links): \Mydex\ApiMrdSdk\Model\GetMedicineLevelOne200Response
```

Retrieve a Medicine subpage or nested medicine

Returns a specific page within a medicine, or a medicine nested within a broader medicine family. HTML and link behaviour can be controlled using no_html and nhs_links. A route that does not exist returns an application-level not-found object with HTTP 200.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MedicinesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = medicines; // string | MRD service scope required for Medicines endpoints.
$param1 = insulin; // string | First Medicines route segment, normally identifying a medicine, medicine category or medicine family.
$param2 = rapid-acting-insulin; // string | Second Medicines route segment, normally identifying a medicine page or a medicine within a broader medicine family.
$no_html = true; // string | When supplied, removes HTML markup from content text. The only accepted value is 'true'. Omit the parameter to leave HTML unchanged.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.

try {
    $result = $apiInstance->getMedicineLevelTwo($x_mrd_scopes, $param1, $param2, $no_html, $nhs_links);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MedicinesApi->getMedicineLevelTwo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Medicines endpoints. | [default to &#39;medicines&#39;] |
| **param1** | **string**| First Medicines route segment, normally identifying a medicine, medicine category or medicine family. | |
| **param2** | **string**| Second Medicines route segment, normally identifying a medicine page or a medicine within a broader medicine family. | |
| **no_html** | **string**| When supplied, removes HTML markup from content text. The only accepted value is &#39;true&#39;. Omit the parameter to leave HTML unchanged. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetMedicineLevelOne200Response**](../Model/GetMedicineLevelOne200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMedicinesRoutes()`

```php
getMedicinesRoutes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MedicinesRoutesResponse
```

Retrieve available Medicines routes

Returns the available routes within the NHS Medicines dataset.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MedicinesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = medicines; // string | MRD service scope required for Medicines endpoints.

try {
    $result = $apiInstance->getMedicinesRoutes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MedicinesApi->getMedicinesRoutes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Medicines endpoints. | [default to &#39;medicines&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MedicinesRoutesResponse**](../Model/MedicinesRoutesResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchMedicines()`

```php
searchMedicines($x_mrd_scopes, $filters, $no_html, $nhs_links, $search_all): \Mydex\ApiMrdSdk\Model\MedicineData[]
```

Search Medicines content

Searches the NHS Medicines dataset using structured filters. By default filters search medicine descriptions. When search_all is enabled, additional searchable page content is included. no_html and nhs_links control content and link formatting.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MedicinesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = medicines; // string | MRD service scope required for Medicines endpoints.
$filters = array(new \Mydex\ApiMrdSdk\Model\\Mydex\ApiMrdSdk\Model\MedicinesSearchFilter()); // \Mydex\ApiMrdSdk\Model\MedicinesSearchFilter[] | Structured Medicines search filters supplied using indexed bracket notation, for example filters[0][operator]=LIKE&filters[0][value]=rapid acting insulin&filters[0][condition]=AND&filters[1][operator]=LIKE&filters[1][value]=diabetes&filters[1][condition]=. Each filter must contain exactly value, operator and condition.
$no_html = true; // string | When supplied, removes HTML markup from content text. The only accepted value is 'true'. Omit the parameter to leave HTML unchanged.
$nhs_links = true; // string | When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is 'true'. Omit the parameter to leave links in their default form.
$search_all = true; // string | When supplied, the search also checks additional Medicines page content in addition to medicine descriptions. The only accepted value is 'true'. This parameter is only valid on the search endpoint.

try {
    $result = $apiInstance->searchMedicines($x_mrd_scopes, $filters, $no_html, $nhs_links, $search_all);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MedicinesApi->searchMedicines: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Medicines endpoints. | [default to &#39;medicines&#39;] |
| **filters** | [**\Mydex\ApiMrdSdk\Model\MedicinesSearchFilter[]**](../Model/\Mydex\ApiMrdSdk\Model\MedicinesSearchFilter.md)| Structured Medicines search filters supplied using indexed bracket notation, for example filters[0][operator]&#x3D;LIKE&amp;filters[0][value]&#x3D;rapid acting insulin&amp;filters[0][condition]&#x3D;AND&amp;filters[1][operator]&#x3D;LIKE&amp;filters[1][value]&#x3D;diabetes&amp;filters[1][condition]&#x3D;. Each filter must contain exactly value, operator and condition. | |
| **no_html** | **string**| When supplied, removes HTML markup from content text. The only accepted value is &#39;true&#39;. Omit the parameter to leave HTML unchanged. | [optional] |
| **nhs_links** | **string**| When supplied, eligible MRD API links are replaced with their equivalent NHS website links. The only accepted value is &#39;true&#39;. Omit the parameter to leave links in their default form. | [optional] |
| **search_all** | **string**| When supplied, the search also checks additional Medicines page content in addition to medicine descriptions. The only accepted value is &#39;true&#39;. This parameter is only valid on the search endpoint. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MedicineData[]**](../Model/MedicineData.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
