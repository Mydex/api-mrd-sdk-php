# MedicineContentElement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**at_type** | **string** |  | [optional]
**name** | **string** |  | [optional]
**identifier** | [**\Mydex\ApiMrdSdk\Model\ConditionVideoObjectIdentifier**](ConditionVideoObjectIdentifier.md) |  | [optional]
**position** | **int** |  | [optional]
**headline** | **string** |  | [optional]
**description** | **string** |  | [optional]
**url** | **string** |  | [optional]
**text** | **string** | Content or question text. HTML is retained by default and removed when no_html is enabled. | [optional]
**caption** | **string** | Caption content when supplied by the source. This is processed by the same content formatter as text. | [optional]
**credit** | **string** | Credit content when supplied by the source. This is processed by the same content formatter as text. | [optional]
**links** | [**\Mydex\ApiMrdSdk\Model\MedicineAnswerLinksInner[]**](MedicineAnswerLinksInner.md) |  | [optional]
**accepted_answer** | [**\Mydex\ApiMrdSdk\Model\MedicineAnswer**](MedicineAnswer.md) |  | [optional]
**main_entity** | [**\Mydex\ApiMrdSdk\Model\MedicineContentElementMainEntity**](MedicineContentElementMainEntity.md) |  | [optional]
**main_entity_of_page** | [**\Mydex\ApiMrdSdk\Model\MedicineContentElement[]**](MedicineContentElement.md) | Nested page elements. | [optional]
**has_part** | [**\Mydex\ApiMrdSdk\Model\MedicineContentElement[]**](MedicineContentElement.md) | Nested content elements duplicated or grouped under hasPart by the source data. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
