# PregnancyData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**at_context** | **string** |  | [optional]
**at_type** | **string** |  | [optional]
**name** | **string** |  | [optional]
**copyright_holder** | [**\Mydex\ApiMrdSdk\Model\PregnancyCopyrightHolder**](PregnancyCopyrightHolder.md) |  | [optional]
**license** | **string** |  | [optional]
**author** | [**\Mydex\ApiMrdSdk\Model\PregnancyAuthor**](PregnancyAuthor.md) |  | [optional]
**about** | [**\Mydex\ApiMrdSdk\Model\PregnancyAbout**](PregnancyAbout.md) |  | [optional]
**description** | **string** |  | [optional]
**url** | **string** | Canonical content URL. An MRD API URL is normally returned by default and is rewritten where applicable when nhs_links is enabled. | [optional]
**genre** | **string[]** | Page genres. Pregnancy pages may return an empty array. | [optional]
**keywords** | [**\Mydex\ApiMrdSdk\Model\LivewellAboutAlternateName**](LivewellAboutAlternateName.md) |  | [optional]
**date_modified** | **\DateTime** |  | [optional]
**last_reviewed** | **string[]** | Review date and review-due date when supplied by the source. | [optional]
**has_part** | [**\Mydex\ApiMrdSdk\Model\PregnancyHealthTopicContent[]**](PregnancyHealthTopicContent.md) | Structured health-topic sections. Some category pages may return an empty array. | [optional]
**breadcrumb** | [**\Mydex\ApiMrdSdk\Model\PregnancyBreadcrumb**](PregnancyBreadcrumb.md) |  | [optional]
**related_link** | [**\Mydex\ApiMrdSdk\Model\PregnancyRelatedLink[]**](PregnancyRelatedLink.md) | Navigation links associated with the page when supplied by the source. | [optional]
**headline** | **string** | Page headline. Empty strings are valid. | [optional]
**content_sub_types** | **string[]** |  | [optional]
**main_entity_of_page** | [**\Mydex\ApiMrdSdk\Model\PregnancyContentElement[]**](PregnancyContentElement.md) | Top-level Pregnancy page content. The exact elements depend on the requested NHS page. | [optional]
**expander_groups** | [**\Mydex\ApiMrdSdk\Model\PregnancyExpanderGroup[]**](PregnancyExpanderGroup.md) | Expandable content groups when supplied by the Pregnancy source data. | [optional]
**webpage** | **string** | Original NHS webpage URL. | [optional]
**id** | **int** |  | [optional]
**route_mapping** | **string** |  | [optional]
**redirect** | **string** | Redirect value from the source dataset. Empty strings are valid. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
