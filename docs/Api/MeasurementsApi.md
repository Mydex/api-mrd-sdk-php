# Mydex\ApiMrdSdk\MeasurementsApi

Operations for retrieving measurement types, units and supporting health lookup values.

All URIs are relative to https://api-mrd.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getActivityType()**](MeasurementsApi.md#getActivityType) | **GET** /measurements/activity-type/{id} | Retrieve an activity type by ID |
| [**getActivityTypes()**](MeasurementsApi.md#getActivityTypes) | **GET** /measurements/activity-type | Retrieve all activity types |
| [**getBloodPressureMeasurement()**](MeasurementsApi.md#getBloodPressureMeasurement) | **GET** /measurements/blood-pressure-measurement/{id} | Retrieve a blood pressure measurement type by ID |
| [**getBloodPressureMeasurements()**](MeasurementsApi.md#getBloodPressureMeasurements) | **GET** /measurements/blood-pressure-measurement | Retrieve all blood pressure measurement types |
| [**getBloodSpecimenSource()**](MeasurementsApi.md#getBloodSpecimenSource) | **GET** /measurements/blood-specimen-source/{id} | Retrieve a blood specimen source by ID |
| [**getBloodSpecimenSources()**](MeasurementsApi.md#getBloodSpecimenSources) | **GET** /measurements/blood-specimen-source | Retrieve all blood specimen sources |
| [**getBodyPosition()**](MeasurementsApi.md#getBodyPosition) | **GET** /measurements/body-position/{id} | Retrieve a body position by ID |
| [**getBodyPositions()**](MeasurementsApi.md#getBodyPositions) | **GET** /measurements/body-position | Retrieve all body positions |
| [**getBodyTemperatureLocation()**](MeasurementsApi.md#getBodyTemperatureLocation) | **GET** /measurements/body-temperature-location/{id} | Retrieve a body temperature location by ID |
| [**getBodyTemperatureLocations()**](MeasurementsApi.md#getBodyTemperatureLocations) | **GET** /measurements/body-temperature-location | Retrieve all body temperature locations |
| [**getCervicalDilation()**](MeasurementsApi.md#getCervicalDilation) | **GET** /measurements/cervical-dilation/{id} | Retrieve a cervical dilation by ID |
| [**getCervicalDilations()**](MeasurementsApi.md#getCervicalDilations) | **GET** /measurements/cervical-dilation | Retrieve all cervical dilations |
| [**getCervicalFirmness()**](MeasurementsApi.md#getCervicalFirmness) | **GET** /measurements/cervical-firmness/{id} | Retrieve a cervical firmness value by ID |
| [**getCervicalFirmnessValues()**](MeasurementsApi.md#getCervicalFirmnessValues) | **GET** /measurements/cervical-firmness | Retrieve all cervical firmness values |
| [**getCervicalMucusAmount()**](MeasurementsApi.md#getCervicalMucusAmount) | **GET** /measurements/cervical-mucus-amount/{id} | Retrieve a cervical mucus amount by ID |
| [**getCervicalMucusAmounts()**](MeasurementsApi.md#getCervicalMucusAmounts) | **GET** /measurements/cervical-mucus-amount | Retrieve all cervical mucus amounts |
| [**getCervicalMucusTexture()**](MeasurementsApi.md#getCervicalMucusTexture) | **GET** /measurements/cervical-mucus-texture/{id} | Retrieve a cervical mucus texture by ID |
| [**getCervicalMucusTextures()**](MeasurementsApi.md#getCervicalMucusTextures) | **GET** /measurements/cervical-mucus-texture | Retrieve all cervical mucus textures |
| [**getCervicalPosition()**](MeasurementsApi.md#getCervicalPosition) | **GET** /measurements/cervical-position/{id} | Retrieve a cervical position by ID |
| [**getCervicalPositions()**](MeasurementsApi.md#getCervicalPositions) | **GET** /measurements/cervical-position | Retrieve all cervical positions |
| [**getExerciseTypeByName()**](MeasurementsApi.md#getExerciseTypeByName) | **GET** /measurements/exercise-type/{exercise_type_name} | Retrieve an exercise type by name |
| [**getExerciseTypes()**](MeasurementsApi.md#getExerciseTypes) | **GET** /measurements/exercise-type | Retrieve all exercise types |
| [**getMealType()**](MeasurementsApi.md#getMealType) | **GET** /measurements/meal-type/{id} | Retrieve a meal type by ID |
| [**getMealTypes()**](MeasurementsApi.md#getMealTypes) | **GET** /measurements/meal-type | Retrieve all meal types |
| [**getMeasurementGroup()**](MeasurementsApi.md#getMeasurementGroup) | **GET** /measurements/groups/{id} | Retrieve a measurement group by ID |
| [**getMeasurementGroups()**](MeasurementsApi.md#getMeasurementGroups) | **GET** /measurements/groups | Retrieve all measurement groups |
| [**getMeasurementType()**](MeasurementsApi.md#getMeasurementType) | **GET** /measurements/types/{id} | Retrieve a measurement type by ID |
| [**getMeasurementTypes()**](MeasurementsApi.md#getMeasurementTypes) | **GET** /measurements/types | Retrieve all measurement types |
| [**getMeasurementUnit()**](MeasurementsApi.md#getMeasurementUnit) | **GET** /measurements/units/{id} | Retrieve a unit of measure by ID |
| [**getMeasurementUnits()**](MeasurementsApi.md#getMeasurementUnits) | **GET** /measurements/units | Retrieve all units of measure |
| [**getResistanceType()**](MeasurementsApi.md#getResistanceType) | **GET** /measurements/resistance-type/{id} | Retrieve a resistance type by ID |
| [**getResistanceTypes()**](MeasurementsApi.md#getResistanceTypes) | **GET** /measurements/resistance-type | Retrieve all resistance types |
| [**getSleepSegmentType()**](MeasurementsApi.md#getSleepSegmentType) | **GET** /measurements/sleep-segment-type/{id} | Retrieve a sleep segment type by ID |
| [**getSleepSegmentTypes()**](MeasurementsApi.md#getSleepSegmentTypes) | **GET** /measurements/sleep-segment-type | Retrieve all sleep segment types |
| [**getTemporalRelationToMeal()**](MeasurementsApi.md#getTemporalRelationToMeal) | **GET** /measurements/temporal-relation-to-meal/{id} | Retrieve a temporal relation to meals by ID |
| [**getTemporalRelationToSleep()**](MeasurementsApi.md#getTemporalRelationToSleep) | **GET** /measurements/temporal-relation-to-sleep/{id} | Retrieve a temporal relation to sleep by ID |
| [**getTemporalRelationsToMeal()**](MeasurementsApi.md#getTemporalRelationsToMeal) | **GET** /measurements/temporal-relation-to-meal | Retrieve all temporal relations to meals |
| [**getTemporalRelationsToSleep()**](MeasurementsApi.md#getTemporalRelationsToSleep) | **GET** /measurements/temporal-relation-to-sleep | Retrieve all temporal relations to sleep |


## `getActivityType()`

```php
getActivityType($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementActivityTypeResult
```

Retrieve an activity type by ID

Returns the activity type matching the supplied activity_type_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getActivityType($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getActivityType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementActivityTypeResult**](../Model/MeasurementActivityTypeResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getActivityTypes()`

```php
getActivityTypes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementActivityTypesResult
```

Retrieve all activity types

Returns activity types including the database record ID, activity type ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getActivityTypes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getActivityTypes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementActivityTypesResult**](../Model/MeasurementActivityTypesResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBloodPressureMeasurement()`

```php
getBloodPressureMeasurement($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementBloodPressureMeasurementResult
```

Retrieve a blood pressure measurement type by ID

Returns the blood pressure measurement type matching the supplied blood_pressure_measurement_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getBloodPressureMeasurement($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getBloodPressureMeasurement: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementBloodPressureMeasurementResult**](../Model/MeasurementBloodPressureMeasurementResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBloodPressureMeasurements()`

```php
getBloodPressureMeasurements($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementBloodPressureMeasurementsResult
```

Retrieve all blood pressure measurement types

Returns blood pressure measurement types including the database record ID, blood pressure measurement ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getBloodPressureMeasurements($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getBloodPressureMeasurements: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementBloodPressureMeasurementsResult**](../Model/MeasurementBloodPressureMeasurementsResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBloodSpecimenSource()`

```php
getBloodSpecimenSource($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementBloodSpecimenSourceResult
```

Retrieve a blood specimen source by ID

Returns the blood specimen source matching the supplied blood_specimen_source_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getBloodSpecimenSource($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getBloodSpecimenSource: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementBloodSpecimenSourceResult**](../Model/MeasurementBloodSpecimenSourceResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBloodSpecimenSources()`

```php
getBloodSpecimenSources($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementBloodSpecimenSourcesResult
```

Retrieve all blood specimen sources

Returns blood specimen sources including the database record ID, blood specimen source ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getBloodSpecimenSources($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getBloodSpecimenSources: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementBloodSpecimenSourcesResult**](../Model/MeasurementBloodSpecimenSourcesResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBodyPosition()`

```php
getBodyPosition($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementBodyPositionResult
```

Retrieve a body position by ID

Returns the body position matching the supplied body_position_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getBodyPosition($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getBodyPosition: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementBodyPositionResult**](../Model/MeasurementBodyPositionResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBodyPositions()`

```php
getBodyPositions($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementBodyPositionsResult
```

Retrieve all body positions

Returns body positions including the database record ID, body position ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getBodyPositions($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getBodyPositions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementBodyPositionsResult**](../Model/MeasurementBodyPositionsResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBodyTemperatureLocation()`

```php
getBodyTemperatureLocation($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementBodyTemperatureLocationResult
```

Retrieve a body temperature location by ID

Returns the body temperature location matching the supplied body_temperature_location_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getBodyTemperatureLocation($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getBodyTemperatureLocation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementBodyTemperatureLocationResult**](../Model/MeasurementBodyTemperatureLocationResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBodyTemperatureLocations()`

```php
getBodyTemperatureLocations($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementBodyTemperatureLocationsResult
```

Retrieve all body temperature locations

Returns body temperature locations including the database record ID, body temperature location ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getBodyTemperatureLocations($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getBodyTemperatureLocations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementBodyTemperatureLocationsResult**](../Model/MeasurementBodyTemperatureLocationsResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCervicalDilation()`

```php
getCervicalDilation($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementCervicalDilationResult
```

Retrieve a cervical dilation by ID

Returns the cervical dilation matching the supplied cervical_dilation_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getCervicalDilation($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getCervicalDilation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementCervicalDilationResult**](../Model/MeasurementCervicalDilationResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCervicalDilations()`

```php
getCervicalDilations($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementCervicalDilationsResult
```

Retrieve all cervical dilations

Returns cervical dilations including the database record ID, cervical dilation ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getCervicalDilations($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getCervicalDilations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementCervicalDilationsResult**](../Model/MeasurementCervicalDilationsResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCervicalFirmness()`

```php
getCervicalFirmness($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementCervicalFirmnessResult
```

Retrieve a cervical firmness value by ID

Returns the cervical firmness value matching the supplied cervical_firmness_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getCervicalFirmness($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getCervicalFirmness: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementCervicalFirmnessResult**](../Model/MeasurementCervicalFirmnessResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCervicalFirmnessValues()`

```php
getCervicalFirmnessValues($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementCervicalFirmnessValuesResult
```

Retrieve all cervical firmness values

Returns cervical firmness values including the database record ID, cervical firmness ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getCervicalFirmnessValues($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getCervicalFirmnessValues: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementCervicalFirmnessValuesResult**](../Model/MeasurementCervicalFirmnessValuesResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCervicalMucusAmount()`

```php
getCervicalMucusAmount($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementCervicalMucusAmountResult
```

Retrieve a cervical mucus amount by ID

Returns the cervical mucus amount matching the supplied cervical_mucus_amount_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getCervicalMucusAmount($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getCervicalMucusAmount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementCervicalMucusAmountResult**](../Model/MeasurementCervicalMucusAmountResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCervicalMucusAmounts()`

```php
getCervicalMucusAmounts($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementCervicalMucusAmountsResult
```

Retrieve all cervical mucus amounts

Returns cervical mucus amounts including the database record ID, cervical mucus amount ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getCervicalMucusAmounts($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getCervicalMucusAmounts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementCervicalMucusAmountsResult**](../Model/MeasurementCervicalMucusAmountsResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCervicalMucusTexture()`

```php
getCervicalMucusTexture($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementCervicalMucusTextureResult
```

Retrieve a cervical mucus texture by ID

Returns the cervical mucus texture matching the supplied cervical_mucus_texture_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getCervicalMucusTexture($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getCervicalMucusTexture: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementCervicalMucusTextureResult**](../Model/MeasurementCervicalMucusTextureResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCervicalMucusTextures()`

```php
getCervicalMucusTextures($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementCervicalMucusTexturesResult
```

Retrieve all cervical mucus textures

Returns cervical mucus textures including the database record ID, cervical mucus texture ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getCervicalMucusTextures($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getCervicalMucusTextures: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementCervicalMucusTexturesResult**](../Model/MeasurementCervicalMucusTexturesResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCervicalPosition()`

```php
getCervicalPosition($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementCervicalPositionResult
```

Retrieve a cervical position by ID

Returns the cervical position matching the supplied cervical_position_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getCervicalPosition($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getCervicalPosition: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementCervicalPositionResult**](../Model/MeasurementCervicalPositionResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCervicalPositions()`

```php
getCervicalPositions($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementCervicalPositionsResult
```

Retrieve all cervical positions

Returns cervical positions including the database record ID, cervical position ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getCervicalPositions($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getCervicalPositions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementCervicalPositionsResult**](../Model/MeasurementCervicalPositionsResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getExerciseTypeByName()`

```php
getExerciseTypeByName($x_mrd_scopes, $exercise_type_name): \Mydex\ApiMrdSdk\Model\MeasurementExerciseTypeResult
```

Retrieve an exercise type by name

Returns the exercise type matching the supplied exercise_type_name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$exercise_type_name = Running; // string | Exercise type name used to retrieve a specific exercise-type record.

try {
    $result = $apiInstance->getExerciseTypeByName($x_mrd_scopes, $exercise_type_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getExerciseTypeByName: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **exercise_type_name** | **string**| Exercise type name used to retrieve a specific exercise-type record. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementExerciseTypeResult**](../Model/MeasurementExerciseTypeResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getExerciseTypes()`

```php
getExerciseTypes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementExerciseTypesResult
```

Retrieve all exercise types

Returns exercise types including the database record ID, exercise type name and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getExerciseTypes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getExerciseTypes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementExerciseTypesResult**](../Model/MeasurementExerciseTypesResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMealType()`

```php
getMealType($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementMealTypeResult
```

Retrieve a meal type by ID

Returns the meal type matching the supplied meal_type_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getMealType($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getMealType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementMealTypeResult**](../Model/MeasurementMealTypeResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMealTypes()`

```php
getMealTypes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementMealTypesResult
```

Retrieve all meal types

Returns meal types including the database record ID, meal type ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getMealTypes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getMealTypes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementMealTypesResult**](../Model/MeasurementMealTypesResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMeasurementGroup()`

```php
getMeasurementGroup($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementGroupResult
```

Retrieve a measurement group by ID

Returns the measurement group matching the supplied database record ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getMeasurementGroup($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getMeasurementGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementGroupResult**](../Model/MeasurementGroupResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMeasurementGroups()`

```php
getMeasurementGroups($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementGroupsResult
```

Retrieve all measurement groups

Returns the available measurement groups and their definitions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getMeasurementGroups($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getMeasurementGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementGroupsResult**](../Model/MeasurementGroupsResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMeasurementType()`

```php
getMeasurementType($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementTypeResult
```

Retrieve a measurement type by ID

Returns the measurement definition matching the supplied measurement ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getMeasurementType($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getMeasurementType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementTypeResult**](../Model/MeasurementTypeResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMeasurementTypes()`

```php
getMeasurementTypes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementTypesResult
```

Retrieve all measurement types

Returns measurement definitions including the measurement name, group and unit.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getMeasurementTypes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getMeasurementTypes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementTypesResult**](../Model/MeasurementTypesResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMeasurementUnit()`

```php
getMeasurementUnit($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementUnitResult
```

Retrieve a unit of measure by ID

Returns the unit of measure matching the supplied database record ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getMeasurementUnit($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getMeasurementUnit: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementUnitResult**](../Model/MeasurementUnitResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMeasurementUnits()`

```php
getMeasurementUnits($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementUnitsResult
```

Retrieve all units of measure

Returns available measurement units and their definitions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getMeasurementUnits($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getMeasurementUnits: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementUnitsResult**](../Model/MeasurementUnitsResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResistanceType()`

```php
getResistanceType($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementResistanceTypeResult
```

Retrieve a resistance type by ID

Returns the resistance type matching the supplied resistance_type_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getResistanceType($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getResistanceType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementResistanceTypeResult**](../Model/MeasurementResistanceTypeResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResistanceTypes()`

```php
getResistanceTypes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementResistanceTypesResult
```

Retrieve all resistance types

Returns resistance types including the database record ID, resistance type ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getResistanceTypes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getResistanceTypes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementResistanceTypesResult**](../Model/MeasurementResistanceTypesResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSleepSegmentType()`

```php
getSleepSegmentType($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementSleepSegmentTypeResult
```

Retrieve a sleep segment type by ID

Returns the sleep segment type matching the supplied sleep_segment_type_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getSleepSegmentType($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getSleepSegmentType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementSleepSegmentTypeResult**](../Model/MeasurementSleepSegmentTypeResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSleepSegmentTypes()`

```php
getSleepSegmentTypes($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementSleepSegmentTypesResult
```

Retrieve all sleep segment types

Returns sleep segment types including the database record ID, sleep segment type ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getSleepSegmentTypes($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getSleepSegmentTypes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementSleepSegmentTypesResult**](../Model/MeasurementSleepSegmentTypesResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTemporalRelationToMeal()`

```php
getTemporalRelationToMeal($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementTemporalRelationToMealResult
```

Retrieve a temporal relation to meals by ID

Returns the temporal relation to meal matching the supplied temporal_relation_to_meal_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getTemporalRelationToMeal($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getTemporalRelationToMeal: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementTemporalRelationToMealResult**](../Model/MeasurementTemporalRelationToMealResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTemporalRelationToSleep()`

```php
getTemporalRelationToSleep($x_mrd_scopes, $id): \Mydex\ApiMrdSdk\Model\MeasurementTemporalRelationToSleepResult
```

Retrieve a temporal relation to sleep by ID

Returns the temporal relation to sleep matching the supplied temporal_relation_to_sleep_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.
$id = 1; // int | Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings.

try {
    $result = $apiInstance->getTemporalRelationToSleep($x_mrd_scopes, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getTemporalRelationToSleep: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |
| **id** | **int**| Numeric lookup identifier used by the requested Measurements endpoint. The response may serialize identifiers as strings. | |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementTemporalRelationToSleepResult**](../Model/MeasurementTemporalRelationToSleepResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTemporalRelationsToMeal()`

```php
getTemporalRelationsToMeal($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementTemporalRelationsToMealResult
```

Retrieve all temporal relations to meals

Returns temporal relations to meals including the database record ID, relation ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getTemporalRelationsToMeal($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getTemporalRelationsToMeal: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementTemporalRelationsToMealResult**](../Model/MeasurementTemporalRelationsToMealResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTemporalRelationsToSleep()`

```php
getTemporalRelationsToSleep($x_mrd_scopes): \Mydex\ApiMrdSdk\Model\MeasurementTemporalRelationsToSleepResult
```

Retrieve all temporal relations to sleep

Returns temporal relations to sleep including the database record ID, relation ID and description.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\MeasurementsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = measurements; // string | MRD service scope required for Measurements endpoints.

try {
    $result = $apiInstance->getTemporalRelationsToSleep($x_mrd_scopes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MeasurementsApi->getTemporalRelationsToSleep: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope required for Measurements endpoints. | [default to &#39;measurements&#39;] |

### Return type

[**\Mydex\ApiMrdSdk\Model\MeasurementTemporalRelationsToSleepResult**](../Model/MeasurementTemporalRelationsToSleepResult.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
