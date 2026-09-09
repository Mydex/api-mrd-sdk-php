# MentalHealthContentElement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**at_type** | **string** | Schema.org element type. | [optional]
**name** | **string** |  | [optional]
**identifier** | [**\Mydex\ApiMrdSdk\Model\ConditionVideoObjectIdentifier**](ConditionVideoObjectIdentifier.md) |  | [optional]
**position** | **int** |  | [optional]
**headline** | **string** |  | [optional]
**description** | **string** |  | [optional]
**url** | **string** |  | [optional]
**text** | **string** | Element content. HTML is retained by default and removed when no_html is enabled. | [optional]
**caption** | **string** | Caption content when supplied by the source. This is processed by the content formatter. | [optional]
**credit** | **string** | Credit content when supplied by the source. This is processed by the content formatter. | [optional]
**links** | [**\Mydex\ApiMrdSdk\Model\MentalHealthAnswerLinksInner[]**](MentalHealthAnswerLinksInner.md) |  | [optional]
**accepted_answer** | [**\Mydex\ApiMrdSdk\Model\MentalHealthAnswer**](MentalHealthAnswer.md) |  | [optional]
**main_entity** | [**\Mydex\ApiMrdSdk\Model\MentalHealthContentElementMainEntity**](MentalHealthContentElementMainEntity.md) |  | [optional]
**main_entity_of_page** | [**\Mydex\ApiMrdSdk\Model\MentalHealthContentElementMainEntityOfPageInner[]**](MentalHealthContentElementMainEntityOfPageInner.md) |  | [optional]
**has_part** | [**\Mydex\ApiMrdSdk\Model\MentalHealthContentElementMainEntityOfPageInner[]**](MentalHealthContentElementMainEntityOfPageInner.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
