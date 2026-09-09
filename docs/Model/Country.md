# Country

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | [**\Mydex\ApiMrdSdk\Model\CountryName**](CountryName.md) |  |
**cca2** | **string** |  |
**cca3** | **string** |  |
**ccn3** | **string** |  |
**independent** | **int** | Whether the country is independent. The current database response serializes this as 0 or 1. |
**status** | **string** |  |
**un_member** | **int** | Whether the country is a United Nations member. The current database response serializes this as 0 or 1. |
**capital** | **string[]** |  |
**alt_spellings** | **string[]** |  |
**region** | **string** |  |
**subregion** | **string** |  |
**languages** | **array<string,string>** | Language codes mapped to language names. |
**landlocked** | **int** | Whether the country is landlocked. The current database response serializes this as 0 or 1. |
**area** | **float** |  |
**demonyms** | [**array<string,\Mydex\ApiMrdSdk\Model\CountryDemonym>**](CountryDemonym.md) |  |
**translations** | [**array<string,\Mydex\ApiMrdSdk\Model\CountryTranslation>**](CountryTranslation.md) |  |
**flag** | **string** |  |
**maps** | [**\Mydex\ApiMrdSdk\Model\CountryMaps**](CountryMaps.md) |  |
**population** | **int** |  |
**gini** | **array<string,float>** | Gini coefficient values keyed by year. Countries without Gini data return an empty object. |
**fifa** | **string** | FIFA country code. The source may also return an empty string. |
**car** | [**\Mydex\ApiMrdSdk\Model\CountryCar**](CountryCar.md) |  |
**timezones** | **string[]** |  |
**continents** | **string[]** |  |
**flags** | [**\Mydex\ApiMrdSdk\Model\CountryFlags**](CountryFlags.md) |  |
**coat_of_arms** | [**\Mydex\ApiMrdSdk\Model\CountryCoatOfArms**](CountryCoatOfArms.md) |  |
**start_of_week** | **string** |  |
**capital_info** | [**\Mydex\ApiMrdSdk\Model\CountryCapitalInfo**](CountryCapitalInfo.md) |  |
**postal_code** | [**\Mydex\ApiMrdSdk\Model\CountryPostalCode**](CountryPostalCode.md) |  |
**currencies** | [**array<string,\Mydex\ApiMrdSdk\Model\CountryCurrency>**](CountryCurrency.md) |  |
**idd** | [**\Mydex\ApiMrdSdk\Model\CountryIdd**](CountryIdd.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
