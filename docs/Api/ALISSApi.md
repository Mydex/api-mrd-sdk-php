# Mydex\ApiMrdSdk\ALISSApi

Operations for searching ALISS services and retrieving ALISS reference data.

All URIs are relative to https://api-mrd.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**countAlissServices()**](ALISSApi.md#countAlissServices) | **GET** /aliss/get-services/search/count | Count matching ALISS services |
| [**getAlissAccessibilityFeatures()**](ALISSApi.md#getAlissAccessibilityFeatures) | **GET** /aliss/accessibility-features | Retrieve ALISS accessibility features |
| [**getAlissCategories()**](ALISSApi.md#getAlissCategories) | **GET** /aliss/categories | Retrieve ALISS categories |
| [**getAlissCommunityGroups()**](ALISSApi.md#getAlissCommunityGroups) | **GET** /aliss/community-groups | Retrieve ALISS community groups |
| [**getAlissOrganisations()**](ALISSApi.md#getAlissOrganisations) | **GET** /aliss/organisations | Retrieve ALISS organisations |
| [**getAlissServiceAreas()**](ALISSApi.md#getAlissServiceAreas) | **GET** /aliss/service-areas | Retrieve ALISS service areas |
| [**getAlissServicesByIds()**](ALISSApi.md#getAlissServicesByIds) | **GET** /aliss/get-services/{service-ids} | Retrieve ALISS services by ID |
| [**searchAlissServices()**](ALISSApi.md#searchAlissServices) | **GET** /aliss/get-services/search | Search ALISS services |


## `countAlissServices()`

```php
countAlissServices($x_mrd_scopes, $filters): \Mydex\ApiMrdSdk\Model\AlissServiceCount[]
```

Count matching ALISS services

Returns the number of distinct ALISS services matching the supplied structured filters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ALISSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = aliss; // string | MRD service scope required for ALISS endpoints.
$filters = new \Mydex\ApiMrdSdk\Model\\Mydex\ApiMrdSdk\Model\SearchAlissServicesFiltersParameter(); // \Mydex\ApiMrdSdk\Model\SearchAlissServicesFiltersParameter | Structured filters used to search ALISS services. Supported datasets are services, organisations, categories, service_areas, locations, accessibility_features and community_groups. Each filter requires field, value and operator. Every filter except the final filter must also contain condition.

try {
    $result = $apiInstance->countAlissServices($x_mrd_scopes, $filters);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ALISSApi->countAlissServices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;] |
| **filters** | [**\Mydex\ApiMrdSdk\Model\SearchAlissServicesFiltersParameter**](../Model/.md)| Structured filters used to search ALISS services. Supported datasets are services, organisations, categories, service_areas, locations, accessibility_features and community_groups. Each filter requires field, value and operator. Every filter except the final filter must also contain condition. | [optional] |

### Return type

[**\Mydex\ApiMrdSdk\Model\AlissServiceCount[]**](../Model/AlissServiceCount.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAlissAccessibilityFeatures()`

```php
getAlissAccessibilityFeatures($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\AlissNamedSlugItem[]
```

Retrieve ALISS accessibility features

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ALISSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = aliss; // string | MRD service scope required for ALISS endpoints.

try {
    $result = $apiInstance->getAlissAccessibilityFeatures($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ALISSApi->getAlissAccessibilityFeatures: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\AlissNamedSlugItem[]**](../Model/AlissNamedSlugItem.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAlissCategories()`

```php
getAlissCategories($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\AlissNamedSlugItem[]
```

Retrieve ALISS categories

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ALISSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = aliss; // string | MRD service scope required for ALISS endpoints.

try {
    $result = $apiInstance->getAlissCategories($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ALISSApi->getAlissCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\AlissNamedSlugItem[]**](../Model/AlissNamedSlugItem.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAlissCommunityGroups()`

```php
getAlissCommunityGroups($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\AlissNamedSlugItem[]
```

Retrieve ALISS community groups

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ALISSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = aliss; // string | MRD service scope required for ALISS endpoints.

try {
    $result = $apiInstance->getAlissCommunityGroups($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ALISSApi->getAlissCommunityGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\AlissNamedSlugItem[]**](../Model/AlissNamedSlugItem.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAlissOrganisations()`

```php
getAlissOrganisations($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\AlissNamedSlugItem[]
```

Retrieve ALISS organisations

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ALISSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = aliss; // string | MRD service scope required for ALISS endpoints.

try {
    $result = $apiInstance->getAlissOrganisations($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ALISSApi->getAlissOrganisations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\AlissNamedSlugItem[]**](../Model/AlissNamedSlugItem.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAlissServiceAreas()`

```php
getAlissServiceAreas($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\AlissServiceAreaReference[]
```

Retrieve ALISS service areas

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ALISSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = aliss; // string | MRD service scope required for ALISS endpoints.

try {
    $result = $apiInstance->getAlissServiceAreas($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ALISSApi->getAlissServiceAreas: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\AlissServiceAreaReference[]**](../Model/AlissServiceAreaReference.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAlissServicesByIds()`

```php
getAlissServicesByIds($x_mrd_scopes, $service_ids, $order_by, $order, $geojson, $format): \Mydex\ApiMrdSdk\Model\AlissService[]
```

Retrieve ALISS services by ID

Retrieves one or more services using a comma-separated list of service IDs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ALISSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = aliss; // string | MRD service scope required for ALISS endpoints.
$service_ids = 123,456; // string | One or more comma-separated ALISS service IDs.
$order_by = services.name; // string | Field used to order matching services.
$order = ASC; // string | Direction used to order matching services.
$geojson = false; // bool | Controls whether GeoJSON is included with service-area data. The API accepts true or false case-insensitively.
$format = JSON; // string | Response format.

try {
    $result = $apiInstance->getAlissServicesByIds($x_mrd_scopes, $service_ids, $order_by, $order, $geojson, $format);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ALISSApi->getAlissServicesByIds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;] |
| **service_ids** | **string**| One or more comma-separated ALISS service IDs. | |
| **order_by** | **string**| Field used to order matching services. | [optional] [default to &#39;services.id&#39;] |
| **order** | **string**| Direction used to order matching services. | [optional] [default to &#39;ASC&#39;] |
| **geojson** | **bool**| Controls whether GeoJSON is included with service-area data. The API accepts true or false case-insensitively. | [optional] [default to false] |
| **format** | **string**| Response format. | [optional] [default to &#39;JSON&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\AlissService[]**](../Model/AlissService.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/xml`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchAlissServices()`

```php
searchAlissServices($x_mrd_scopes, $filters, $order_by, $order, $limit, $after, $before, $geojson, $format): \Mydex\ApiMrdSdk\Model\AlissService[]
```

Search ALISS services

Searches ALISS services using structured filters, ordering and keyset pagination.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ALISSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = aliss; // string | MRD service scope required for ALISS endpoints.
$filters = new \Mydex\ApiMrdSdk\Model\\Mydex\ApiMrdSdk\Model\SearchAlissServicesFiltersParameter(); // \Mydex\ApiMrdSdk\Model\SearchAlissServicesFiltersParameter | Structured filters used to search ALISS services. Supported datasets are services, organisations, categories, service_areas, locations, accessibility_features and community_groups. Each filter requires field, value and operator. Every filter except the final filter must also contain condition.
$order_by = services.name; // string | Field used to order matching services.
$order = ASC; // string | Direction used to order matching services.
$limit = 20; // int | Maximum number of services to return. The API defaults to 20 and rejects values greater than 100.
$after = 123; // string | Keyset pagination value used to retrieve records after the supplied position. Only alphanumeric characters, commas, hyphens, underscores and spaces are accepted.
$before = 456; // string | Keyset pagination value used to retrieve records before the supplied position. Only alphanumeric characters, commas, hyphens, underscores and spaces are accepted.
$geojson = false; // bool | Controls whether GeoJSON is included with service-area data. The API accepts true or false case-insensitively.
$format = JSON; // string | Response format.

try {
    $result = $apiInstance->searchAlissServices($x_mrd_scopes, $filters, $order_by, $order, $limit, $after, $before, $geojson, $format);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ALISSApi->searchAlissServices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for ALISS endpoints. | [default to &#39;aliss&#39;] |
| **filters** | [**\Mydex\ApiMrdSdk\Model\SearchAlissServicesFiltersParameter**](../Model/.md)| Structured filters used to search ALISS services. Supported datasets are services, organisations, categories, service_areas, locations, accessibility_features and community_groups. Each filter requires field, value and operator. Every filter except the final filter must also contain condition. | [optional] |
| **order_by** | **string**| Field used to order matching services. | [optional] [default to &#39;services.id&#39;] |
| **order** | **string**| Direction used to order matching services. | [optional] [default to &#39;ASC&#39;] |
| **limit** | **int**| Maximum number of services to return. The API defaults to 20 and rejects values greater than 100. | [optional] [default to 20] |
| **after** | **string**| Keyset pagination value used to retrieve records after the supplied position. Only alphanumeric characters, commas, hyphens, underscores and spaces are accepted. | [optional] |
| **before** | **string**| Keyset pagination value used to retrieve records before the supplied position. Only alphanumeric characters, commas, hyphens, underscores and spaces are accepted. | [optional] |
| **geojson** | **bool**| Controls whether GeoJSON is included with service-area data. The API accepts true or false case-insensitively. | [optional] [default to false] |
| **format** | **string**| Response format. | [optional] [default to &#39;JSON&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\AlissService[]**](../Model/AlissService.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/xml`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
