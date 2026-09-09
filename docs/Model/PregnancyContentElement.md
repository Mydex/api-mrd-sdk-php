# PregnancyContentElement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**at_type** | **string** |  | [optional]
**name** | **string** |  | [optional]
**identifier** | [**\Mydex\ApiMrdSdk\Model\ConditionVideoObjectIdentifier**](ConditionVideoObjectIdentifier.md) |  | [optional]
**position** | **int** |  | [optional]
**headline** | **string** | Element heading. Empty strings are valid. | [optional]
**description** | **string** |  | [optional]
**url** | **string** | Element URL. MRD API URLs are normally returned by default and NHS URLs are returned when nhs_links is enabled. | [optional]
**text** | **string** | Element content. HTML is retained by default. When no_html is enabled, markup is removed and extracted links may be moved into links. | [optional]
**caption** | **string** | Caption content when supplied by the source. This content is processed using the selected content formatter. | [optional]
**credit** | **string** | Credit content when supplied by the source. This content is processed using the selected content formatter. | [optional]
**links** | [**\Mydex\ApiMrdSdk\Model\PregnancyAnswerLinksInner[]**](PregnancyAnswerLinksInner.md) | Links extracted while formatting text, caption, credit or nested content. | [optional]
**accepted_answer** | [**\Mydex\ApiMrdSdk\Model\PregnancyAnswer**](PregnancyAnswer.md) |  | [optional]
**main_entity** | [**\Mydex\ApiMrdSdk\Model\PregnancyContentElementMainEntity**](PregnancyContentElementMainEntity.md) |  | [optional]
**main_entity_of_page** | [**\Mydex\ApiMrdSdk\Model\PregnancyContentElementMainEntityOfPageInner[]**](PregnancyContentElementMainEntityOfPageInner.md) | Nested Pregnancy page content. | [optional]
**has_part** | [**\Mydex\ApiMrdSdk\Model\PregnancyContentElement[]**](PregnancyContentElement.md) | Nested Pregnancy content. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
