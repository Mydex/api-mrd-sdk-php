# Mydex\ApiMrdSdk\SearchApi

Operations for searching indexed MRD content.

All URIs are relative to https://api-mrd.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**searchMrd()**](SearchApi.md#searchMrd) | **GET** /search | Search MRD content |


## `searchMrd()`

```php
searchMrd($x_mrd_scopes, $filters, $page, $all, $limit): \Mydex\ApiMrdSdk\Model\SearchMrd200Response
```

Search MRD content

Searches indexed MRD content using structured filters. Filter 0 must contain a keyword. Searchable fields are keyword and page description, using either = or LIKE. Indexed filters can be connected using AND, OR, NOT or AND NOT, with NOT converted internally to AND NOT. Results are restricted according to the MRD scopes authorised for the request. By default results are paginated. Supplying the all query parameter disables pagination regardless of the parameter value.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = aliss,conditions; // string | MRD service scope or scopes to include in global search. Supply one or more OAuth-authorised MRD service scopes, comma-delimited or space-delimited.
$filters = array(new \Mydex\ApiMrdSdk\Model\\Mydex\ApiMrdSdk\Model\SearchFilter()); // \Mydex\ApiMrdSdk\Model\SearchFilter[] | Structured Search filters supplied using indexed bracket notation. Filter 0 must contain keyword, operator and condition. Additional filters must contain operator and condition and may contain keyword, description or both. For example: filters[0][operator]=LIKE&filters[0][keyword]=smoking&filters[0][condition]=AND&filters[1][operator]=LIKE&filters[1][description]=electronic cigarette&filters[1][condition]=. The final filter should normally use an empty condition.
$page = 1; // int | Page number used when pagination is enabled. The value is cast to an integer by the current implementation. If the resulting value is below 1, page 1 is used. The default is 1.
$all = true; // string | Disables pagination when this query parameter is present. The current implementation checks only whether the parameter exists; its value is ignored. all=true, all=false and an empty all parameter all enable unpaginated results. Omit the parameter to use pagination.
$limit = 50; // int | Requested number of results per page when pagination is enabled. The value is cast to an integer. Values above 100 are reduced to 100. The default is 50.

try {
    $result = $apiInstance->searchMrd($x_mrd_scopes, $filters, $page, $all, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchMrd: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_mrd_scopes** | **string**| MRD service scope or scopes to include in global search. Supply one or more OAuth-authorised MRD service scopes, comma-delimited or space-delimited. | [default to &#39;aliss&#39;] |
| **filters** | [**\Mydex\ApiMrdSdk\Model\SearchFilter[]**](../Model/\Mydex\ApiMrdSdk\Model\SearchFilter.md)| Structured Search filters supplied using indexed bracket notation. Filter 0 must contain keyword, operator and condition. Additional filters must contain operator and condition and may contain keyword, description or both. For example: filters[0][operator]&#x3D;LIKE&amp;filters[0][keyword]&#x3D;smoking&amp;filters[0][condition]&#x3D;AND&amp;filters[1][operator]&#x3D;LIKE&amp;filters[1][description]&#x3D;electronic cigarette&amp;filters[1][condition]&#x3D;. The final filter should normally use an empty condition. | |
| **page** | **int**| Page number used when pagination is enabled. The value is cast to an integer by the current implementation. If the resulting value is below 1, page 1 is used. The default is 1. | [optional] [default to 1] |
| **all** | **string**| Disables pagination when this query parameter is present. The current implementation checks only whether the parameter exists; its value is ignored. all&#x3D;true, all&#x3D;false and an empty all parameter all enable unpaginated results. Omit the parameter to use pagination. | [optional] |
| **limit** | **int**| Requested number of results per page when pagination is enabled. The value is cast to an integer. Values above 100 are reduced to 100. The default is 50. | [optional] [default to 50] |

### Return type

[**\Mydex\ApiMrdSdk\Model\SearchMrd200Response**](../Model/SearchMrd200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
