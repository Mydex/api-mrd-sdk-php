# Mydex\ApiMrdSdk\CountriesApi

Operations for retrieving country reference information.

All URIs are relative to https://api-mrd.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllCountries()**](CountriesApi.md#getAllCountries) | **GET** /countries | Retrieve all countries |
| [**getCountryByCca2()**](CountriesApi.md#getCountryByCca2) | **GET** /countries/{cca2} | Retrieve a country by CCA2 code |


## `getAllCountries()`

```php
getAllCountries($x_mrd_scopes, $filters): \Mydex\ApiMrdSdk\Model\GetAllCountries200Response
```

Retrieve all countries

Returns all available countries. Without filters, the model returns the complete country list inside an additional outer array. When filters are supplied, the response is the filtered country list directly.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\CountriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = countries; // string | MRD service scope required for Countries endpoints.
$filters = ["region","subregion","idd"]; // string[] | Country fields to include in the response. The API accepts comma-separated values such as filters=region,subregion,idd and PHP-style array values such as filters[]=capital&filters[]=maps. Duplicate filters are removed.

try {
    $result = $apiInstance->getAllCountries($x_mrd_scopes, $filters);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CountriesApi->getAllCountries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Countries endpoints. | [default to &#39;countries&#39;] |
| **filters** | [**string[]**](../Model/string.md)| Country fields to include in the response. The API accepts comma-separated values such as filters&#x3D;region,subregion,idd and PHP-style array values such as filters[]&#x3D;capital&amp;filters[]&#x3D;maps. Duplicate filters are removed. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetAllCountries200Response**](../Model/GetAllCountries200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCountryByCca2()`

```php
getCountryByCca2($x_mrd_scopes, $cca2, $filters): \Mydex\ApiMrdSdk\Model\GetCountryByCca2200Response
```

Retrieve a country by CCA2 code

Returns the country matching the supplied lookup value. The value is converted to uppercase before lookup. Without filters, a matching country is returned inside an array. With filters, the filtered country object is returned directly. An unknown value returns an empty array.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\CountriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = countries; // string | MRD service scope required for Countries endpoints.
$cca2 = ad; // string | Country CCA2 lookup value. The supplied value is converted to uppercase before the database lookup. For example, ad is looked up as AD.
$filters = ["region","subregion","idd"]; // string[] | Country fields to include in the response. The API accepts comma-separated values such as filters=region,subregion,idd and PHP-style array values such as filters[]=capital&filters[]=maps. Duplicate filters are removed.

try {
    $result = $apiInstance->getCountryByCca2($x_mrd_scopes, $cca2, $filters);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CountriesApi->getCountryByCca2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Countries endpoints. | [default to &#39;countries&#39;] |
| **cca2** | **string**| Country CCA2 lookup value. The supplied value is converted to uppercase before the database lookup. For example, ad is looked up as AD. | |
| **filters** | [**string[]**](../Model/string.md)| Country fields to include in the response. The API accepts comma-separated values such as filters&#x3D;region,subregion,idd and PHP-style array values such as filters[]&#x3D;capital&amp;filters[]&#x3D;maps. Duplicate filters are removed. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\GetCountryByCca2200Response**](../Model/GetCountryByCca2200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
