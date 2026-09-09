# SearchFilter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**keyword** | **string** | Optional keyword value to search. A non-empty value may contain letters, numbers, commas, spaces and hyphens and cannot consist only of whitespace. | [optional]
**description** | **string** | Optional page-description value to search. A non-empty value may contain letters, numbers, commas, spaces and hyphens and cannot consist only of whitespace. | [optional]
**operator** | **string** | Comparison operator used for searchable fields in this filter. |
**condition** | **string** | Logical condition connecting this filter to another indexed filter. NOT is converted internally to AND NOT. The final filter should normally use an empty condition. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
