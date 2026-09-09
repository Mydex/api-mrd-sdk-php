# Mydex\ApiMrdSdk\ValidationsApi

Operations for lookup validation, PDS Master Schema metadata and Mydex Template System data.

All URIs are relative to https://api-mrd.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getValidationLookupValues()**](ValidationsApi.md#getValidationLookupValues) | **GET** /validations/lookup/{field_name} | Retrieve allowed values for a lookup field |
| [**getValidationMdsAllDatasetsAndFields()**](ValidationsApi.md#getValidationMdsAllDatasetsAndFields) | **GET** /validations/mds/all-datasets-and-fields | Retrieve all MDS datasets with extended field information |
| [**getValidationMdsDatasetFieldTypes()**](ValidationsApi.md#getValidationMdsDatasetFieldTypes) | **GET** /validations/mds/dataset/{dataset}/fieldtypes | Retrieve field types for an MDS dataset |
| [**getValidationMdsDatasetFields()**](ValidationsApi.md#getValidationMdsDatasetFields) | **GET** /validations/mds/dataset/{dataset} | Retrieve full field definitions for an MDS dataset |
| [**getValidationMdsDatasets()**](ValidationsApi.md#getValidationMdsDatasets) | **GET** /validations/mds/datasets | Retrieve MDS datasets |
| [**getValidationMdsDatasetsAndFields()**](ValidationsApi.md#getValidationMdsDatasetsAndFields) | **GET** /validations/mds/datasets-and-fields | Retrieve MDS datasets and basic field information |
| [**getValidationMdsDatasetsByOneStatus()**](ValidationsApi.md#getValidationMdsDatasetsByOneStatus) | **GET** /validations/mds/datasets/{status1} | Retrieve MDS datasets by one status |
| [**getValidationMdsDatasetsByThreeStatuses()**](ValidationsApi.md#getValidationMdsDatasetsByThreeStatuses) | **GET** /validations/mds/datasets/{status1}/{status2}/{status3} | Retrieve MDS datasets by three statuses |
| [**getValidationMdsDatasetsByTwoStatuses()**](ValidationsApi.md#getValidationMdsDatasetsByTwoStatuses) | **GET** /validations/mds/datasets/{status1}/{status2} | Retrieve MDS datasets by two statuses |
| [**getValidationMdsDatasetsByType()**](ValidationsApi.md#getValidationMdsDatasetsByType) | **GET** /validations/mds/datasets/type/{type} | Retrieve MDS datasets by type |
| [**getValidationMdsFieldType()**](ValidationsApi.md#getValidationMdsFieldType) | **GET** /validations/mds/field/type/{field} | Retrieve an MDS field&#39;s data type |
| [**getValidationMdsSummary()**](ValidationsApi.md#getValidationMdsSummary) | **GET** /validations/mds/summary | Retrieve an MDS summary |
| [**getValidationMtsFeatureByName()**](ValidationsApi.md#getValidationMtsFeatureByName) | **GET** /validations/mts/features/{feature} | Retrieve an MTS feature by name |
| [**getValidationMtsFeatures()**](ValidationsApi.md#getValidationMtsFeatures) | **GET** /validations/mts/features | Retrieve all MTS features |
| [**getValidationMtsFeaturesByGroup()**](ValidationsApi.md#getValidationMtsFeaturesByGroup) | **GET** /validations/mts/features/group/{group} | Retrieve MTS features by group |
| [**getValidationMtsTemplateByModule()**](ValidationsApi.md#getValidationMtsTemplateByModule) | **GET** /validations/mts/templates/{template}/{module} | Retrieve an MTS template module |
| [**getValidationMtsTemplateByName()**](ValidationsApi.md#getValidationMtsTemplateByName) | **GET** /validations/mts/templates/{template} | Retrieve MTS template records by template name |
| [**getValidationMtsTemplateBySubsection()**](ValidationsApi.md#getValidationMtsTemplateBySubsection) | **GET** /validations/mts/templates/{template}/{module}/{subsection} | Retrieve an MTS template subsection |
| [**getValidationMtsTemplates()**](ValidationsApi.md#getValidationMtsTemplates) | **GET** /validations/mts/templates | Retrieve all MTS template records |
| [**searchValidationMdsFields()**](ValidationsApi.md#searchValidationMdsFields) | **GET** /validations/mds/search/{search} | Search MDS field names |
| [**validateLookupValue()**](ValidationsApi.md#validateLookupValue) | **GET** /validations/lookup/{field_name}/{user_input} | Validate a value against a lookup field |


## `getValidationLookupValues()`

```php
getValidationLookupValues($field_name): \Mydex\ApiMrdSdk\Model\LookupAllowedValuesResponse
```

Retrieve allowed values for a lookup field

Returns allowed values from the requested validation lookup. Most lookup tables return an array of strings. Structured lookup tables such as race_ethnicity return an array of objects. The field name must map to a supported lu_<field_name> lookup table; country is additionally supported from the Countries database.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$field_name = gender; // string | Supported validation lookup field. Only lookup datasets currently intended to provide useful values through the Validations API are exposed here.

try {
    $result = $apiInstance->getValidationLookupValues($field_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationLookupValues: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **field_name** | **string**| Supported validation lookup field. Only lookup datasets currently intended to provide useful values through the Validations API are exposed here. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\LookupAllowedValuesResponse**](../Model/LookupAllowedValuesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsAllDatasetsAndFields()`

```php
getValidationMdsAllDatasetsAndFields(): array<string,array>
```

Retrieve all MDS datasets with extended field information

Returns all published datasets grouped dynamically by dataset status. Each dataset includes its PDS file type, derived deployment environment and extended information for its published fields.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getValidationMdsAllDatasetsAndFields();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsAllDatasetsAndFields: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**array<string,array>**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsDatasetFieldTypes()`

```php
getValidationMdsDatasetFieldTypes($dataset): array<string,\Mydex\ApiMrdSdk\Model\MdsFieldType>
```

Retrieve field types for an MDS dataset

Returns an object keyed by field machine name containing the field name, display name and data type for fields belonging to the requested dataset.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$dataset = ds_employment; // string | MDS dataset machine name.

try {
    $result = $apiInstance->getValidationMdsDatasetFieldTypes($dataset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsDatasetFieldTypes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dataset** | **string**| MDS dataset machine name. | |

### Return type

[**array<string,\Mydex\ApiMrdSdk\Model\MdsFieldType>**](../Model/MdsFieldType.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsDatasetFields()`

```php
getValidationMdsDatasetFields($dataset): array<string,\Mydex\ApiMrdSdk\Model\MdsFieldDetails>
```

Retrieve full field definitions for an MDS dataset

Returns an object keyed by field machine name containing extended definitions for published fields belonging to the requested dataset.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$dataset = ds_employment; // string | MDS dataset machine name.

try {
    $result = $apiInstance->getValidationMdsDatasetFields($dataset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsDatasetFields: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **dataset** | **string**| MDS dataset machine name. | |

### Return type

[**array<string,\Mydex\ApiMrdSdk\Model\MdsFieldDetails>**](../Model/MdsFieldDetails.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsDatasets()`

```php
getValidationMdsDatasets(): \Mydex\ApiMrdSdk\Model\MdsDatasetSummary[]
```

Retrieve MDS datasets

Returns published MDS datasets including their machine name, display name and status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getValidationMdsDatasets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsDatasets: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Mydex\ApiMrdSdk\Model\MdsDatasetSummary[]**](../Model/MdsDatasetSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsDatasetsAndFields()`

```php
getValidationMdsDatasetsAndFields(): array<string,array>
```

Retrieve MDS datasets and basic field information

Returns published datasets grouped dynamically by dataset status. Each dataset contains its machine name, display name, status, PDS file type and a map of published fields containing field name, display name and data type.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getValidationMdsDatasetsAndFields();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsDatasetsAndFields: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**array<string,array>**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsDatasetsByOneStatus()`

```php
getValidationMdsDatasetsByOneStatus($status1): \Mydex\ApiMrdSdk\Model\MdsDatasetSummary[]
```

Retrieve MDS datasets by one status

Returns published datasets matching the supplied dataset status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$status1 = Live; // string | First MDS dataset status to include.

try {
    $result = $apiInstance->getValidationMdsDatasetsByOneStatus($status1);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsDatasetsByOneStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status1** | **string**| First MDS dataset status to include. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MdsDatasetSummary[]**](../Model/MdsDatasetSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsDatasetsByThreeStatuses()`

```php
getValidationMdsDatasetsByThreeStatuses($status1, $status2, $status3): \Mydex\ApiMrdSdk\Model\MdsDatasetSummary[]
```

Retrieve MDS datasets by three statuses

Returns published datasets matching any of the supplied dataset statuses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$status1 = Live; // string | First MDS dataset status to include.
$status2 = Implement; // string | Second MDS dataset status to include.
$status3 = Hold; // string | Third MDS dataset status to include.

try {
    $result = $apiInstance->getValidationMdsDatasetsByThreeStatuses($status1, $status2, $status3);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsDatasetsByThreeStatuses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status1** | **string**| First MDS dataset status to include. | |
| **status2** | **string**| Second MDS dataset status to include. | |
| **status3** | **string**| Third MDS dataset status to include. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MdsDatasetSummary[]**](../Model/MdsDatasetSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsDatasetsByTwoStatuses()`

```php
getValidationMdsDatasetsByTwoStatuses($status1, $status2): \Mydex\ApiMrdSdk\Model\MdsDatasetSummary[]
```

Retrieve MDS datasets by two statuses

Returns published datasets matching either of the supplied dataset statuses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$status1 = Live; // string | First MDS dataset status to include.
$status2 = Implement; // string | Second MDS dataset status to include.

try {
    $result = $apiInstance->getValidationMdsDatasetsByTwoStatuses($status1, $status2);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsDatasetsByTwoStatuses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status1** | **string**| First MDS dataset status to include. | |
| **status2** | **string**| Second MDS dataset status to include. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MdsDatasetSummary[]**](../Model/MdsDatasetSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsDatasetsByType()`

```php
getValidationMdsDatasetsByType($type): \Mydex\ApiMrdSdk\Model\MdsDatasetSummary[]
```

Retrieve MDS datasets by type

Returns published datasets belonging to the requested public dataset type. metadata is mapped internally to JSON and transactional is mapped internally to SQLite.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$type = transactional; // string | Public dataset type. metadata maps to JSON-backed datasets and transactional maps to SQLite-backed datasets.

try {
    $result = $apiInstance->getValidationMdsDatasetsByType($type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsDatasetsByType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **type** | **string**| Public dataset type. metadata maps to JSON-backed datasets and transactional maps to SQLite-backed datasets. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MdsDatasetSummary[]**](../Model/MdsDatasetSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsFieldType()`

```php
getValidationMdsFieldType($field): \Mydex\ApiMrdSdk\Model\MdsFieldTypeResponse
```

Retrieve an MDS field's data type

Returns the field machine name, display name and data type for the requested MDS field.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$field = field_country; // string | MDS field machine name.

try {
    $result = $apiInstance->getValidationMdsFieldType($field);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsFieldType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **field** | **string**| MDS field machine name. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MdsFieldTypeResponse**](../Model/MdsFieldTypeResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMdsSummary()`

```php
getValidationMdsSummary(): \Mydex\ApiMrdSdk\Model\MdsSummaryResponse
```

Retrieve an MDS summary

Returns counts of published datasets, published live datasets and published fields. The current API serializes these database count values as strings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getValidationMdsSummary();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMdsSummary: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Mydex\ApiMrdSdk\Model\MdsSummaryResponse**](../Model/MdsSummaryResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMtsFeatureByName()`

```php
getValidationMtsFeatureByName($feature): \Mydex\ApiMrdSdk\Model\MtsFeatureRecord[]
```

Retrieve an MTS feature by name

Returns records whose feature_name matches the supplied feature name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$feature = View Measurements; // string | Mydex Template System feature name. The endpoint matches this value against feature_name.

try {
    $result = $apiInstance->getValidationMtsFeatureByName($feature);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMtsFeatureByName: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **feature** | **string**| Mydex Template System feature name. The endpoint matches this value against feature_name. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MtsFeatureRecord[]**](../Model/MtsFeatureRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMtsFeatures()`

```php
getValidationMtsFeatures(): \Mydex\ApiMrdSdk\Model\MtsFeatureRecord[]
```

Retrieve all MTS features

Returns all Mydex Template System feature records.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getValidationMtsFeatures();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMtsFeatures: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Mydex\ApiMrdSdk\Model\MtsFeatureRecord[]**](../Model/MtsFeatureRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMtsFeaturesByGroup()`

```php
getValidationMtsFeaturesByGroup($group): \Mydex\ApiMrdSdk\Model\MtsFeatureRecord[]
```

Retrieve MTS features by group

Returns records whose feature_group matches the supplied feature group name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$group = Measurements; // string | Mydex Template System feature group name. The endpoint matches this value against feature_group.

try {
    $result = $apiInstance->getValidationMtsFeaturesByGroup($group);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMtsFeaturesByGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group** | **string**| Mydex Template System feature group name. The endpoint matches this value against feature_group. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MtsFeatureRecord[]**](../Model/MtsFeatureRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMtsTemplateByModule()`

```php
getValidationMtsTemplateByModule($template, $module): \Mydex\ApiMrdSdk\Model\MtsTemplateRecord[]
```

Retrieve an MTS template module

Returns records whose template_name and module_name match the supplied values.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$template = About Me; // string | Mydex Template System template name. The endpoint matches this value against template_name.
$module = This is Me; // string | Mydex Template System module name. The endpoint matches this value against module_name.

try {
    $result = $apiInstance->getValidationMtsTemplateByModule($template, $module);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMtsTemplateByModule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template** | **string**| Mydex Template System template name. The endpoint matches this value against template_name. | |
| **module** | **string**| Mydex Template System module name. The endpoint matches this value against module_name. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MtsTemplateRecord[]**](../Model/MtsTemplateRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMtsTemplateByName()`

```php
getValidationMtsTemplateByName($template): \Mydex\ApiMrdSdk\Model\MtsTemplateRecord[]
```

Retrieve MTS template records by template name

Returns records whose template_name matches the supplied template name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$template = About Me; // string | Mydex Template System template name. The endpoint matches this value against template_name.

try {
    $result = $apiInstance->getValidationMtsTemplateByName($template);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMtsTemplateByName: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template** | **string**| Mydex Template System template name. The endpoint matches this value against template_name. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MtsTemplateRecord[]**](../Model/MtsTemplateRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMtsTemplateBySubsection()`

```php
getValidationMtsTemplateBySubsection($template, $module, $subsection): \Mydex\ApiMrdSdk\Model\MtsTemplateRecord[]
```

Retrieve an MTS template subsection

Returns records whose template_name, module_name and module_subsection match the supplied values.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$template = About Me; // string | Mydex Template System template name. The endpoint matches this value against template_name.
$module = This is Me; // string | Mydex Template System module name. The endpoint matches this value against module_name.
$subsection = Personal Details; // string | Mydex Template System module subsection name. The endpoint matches this value against module_subsection.

try {
    $result = $apiInstance->getValidationMtsTemplateBySubsection($template, $module, $subsection);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMtsTemplateBySubsection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template** | **string**| Mydex Template System template name. The endpoint matches this value against template_name. | |
| **module** | **string**| Mydex Template System module name. The endpoint matches this value against module_name. | |
| **subsection** | **string**| Mydex Template System module subsection name. The endpoint matches this value against module_subsection. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MtsTemplateRecord[]**](../Model/MtsTemplateRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getValidationMtsTemplates()`

```php
getValidationMtsTemplates(): \Mydex\ApiMrdSdk\Model\MtsTemplateRecord[]
```

Retrieve all MTS template records

Returns all records from the Mydex Template System templates_features table, including template, module, subsection and route information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getValidationMtsTemplates();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->getValidationMtsTemplates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Mydex\ApiMrdSdk\Model\MtsTemplateRecord[]**](../Model/MtsTemplateRecord.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `searchValidationMdsFields()`

```php
searchValidationMdsFields($search): \Mydex\ApiMrdSdk\Model\MdsFieldSearchResponse
```

Search MDS field names

Searches published MDS field machine names for values containing the supplied search term.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$search = birth; // string | Partial field machine name used to search published MDS fields.

try {
    $result = $apiInstance->searchValidationMdsFields($search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->searchValidationMdsFields: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **search** | **string**| Partial field machine name used to search published MDS fields. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MdsFieldSearchResponse**](../Model/MdsFieldSearchResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `validateLookupValue()`

```php
validateLookupValue($field_name, $user_input): \Mydex\ApiMrdSdk\Model\LookupValidationResponse
```

Validate a value against a lookup field

Checks whether the supplied value matches an allowed value associated with the requested lookup. Matching is case-insensitive because the endpoint converts both stored values and the supplied value to uppercase. The result is returned as the string true or false.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mydex\ApiMrdSdk\Api\ValidationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$field_name = gender; // string | Supported validation lookup field. Only lookup datasets currently intended to provide useful values through the Validations API are exposed here.
$user_input = Female; // string | Value to validate against the allowed values associated with the requested lookup.

try {
    $result = $apiInstance->validateLookupValue($field_name, $user_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ValidationsApi->validateLookupValue: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **field_name** | **string**| Supported validation lookup field. Only lookup datasets currently intended to provide useful values through the Validations API are exposed here. | |
| **user_input** | **string**| Value to validate against the allowed values associated with the requested lookup. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\LookupValidationResponse**](../Model/LookupValidationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
