# MentalHealthSearchFilter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **string** | Text to search for. The value must not be empty and may contain only letters, numbers and whitespace. |
**operator** | **string** | Comparison operator accepted by the Mental Health search validator. |
**condition** | **string** | Logical condition accepted by the shared search validator. The property is required but may be empty. The Mental Health search implementation currently combines generated search clauses using AND. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
