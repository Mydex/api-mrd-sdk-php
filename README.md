# OpenAPIClient-php

API for retrieving Master Reference Data


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiMrdSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiMrdSdk\Api\ALISSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_mrd_scopes = aliss; // string | MRD service scope required for ALISS endpoints.
$filters = new \Mydex\ApiMrdSdk\Model\\Mydex\ApiMrdSdk\Model\SearchAlissServicesFiltersParameter(); // \Mydex\ApiMrdSdk\Model\SearchAlissServicesFiltersParameter | Structured filters used to search ALISS services. Supported datasets are services, organisations, categories, service_areas, locations, accessibility_features and community_groups. Each filter requires field, value and operator. Every filter except the final filter must also contain condition.

try {
    $result = $apiInstance->countAlissServices($x_mrd_scopes, $filters);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ALISSApi->countAlissServices: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api-mrd.mydex.org*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ALISSApi* | [**countAlissServices**](docs/Api/ALISSApi.md#countalissservices) | **GET** /aliss/get-services/search/count | Count matching ALISS services
*ALISSApi* | [**getAlissAccessibilityFeatures**](docs/Api/ALISSApi.md#getalissaccessibilityfeatures) | **GET** /aliss/accessibility-features | Retrieve ALISS accessibility features
*ALISSApi* | [**getAlissCategories**](docs/Api/ALISSApi.md#getalisscategories) | **GET** /aliss/categories | Retrieve ALISS categories
*ALISSApi* | [**getAlissCommunityGroups**](docs/Api/ALISSApi.md#getalisscommunitygroups) | **GET** /aliss/community-groups | Retrieve ALISS community groups
*ALISSApi* | [**getAlissOrganisations**](docs/Api/ALISSApi.md#getalissorganisations) | **GET** /aliss/organisations | Retrieve ALISS organisations
*ALISSApi* | [**getAlissServiceAreas**](docs/Api/ALISSApi.md#getalissserviceareas) | **GET** /aliss/service-areas | Retrieve ALISS service areas
*ALISSApi* | [**getAlissServicesByIds**](docs/Api/ALISSApi.md#getalissservicesbyids) | **GET** /aliss/get-services/{service-ids} | Retrieve ALISS services by ID
*ALISSApi* | [**searchAlissServices**](docs/Api/ALISSApi.md#searchalissservices) | **GET** /aliss/get-services/search | Search ALISS services
*ConditionsApi* | [**getConditionLevelOne**](docs/Api/ConditionsApi.md#getconditionlevelone) | **GET** /conditions/{param1} | Retrieve a first-level Conditions page
*ConditionsApi* | [**getConditionLevelThree**](docs/Api/ConditionsApi.md#getconditionlevelthree) | **GET** /conditions/{param1}/{param2}/{param3} | Retrieve a third-level Conditions page
*ConditionsApi* | [**getConditionLevelTwo**](docs/Api/ConditionsApi.md#getconditionleveltwo) | **GET** /conditions/{param1}/{param2} | Retrieve a second-level Conditions page
*ConditionsApi* | [**getConditionRoutes**](docs/Api/ConditionsApi.md#getconditionroutes) | **GET** /conditions | Retrieve available Conditions routes
*ConditionsApi* | [**searchConditions**](docs/Api/ConditionsApi.md#searchconditions) | **GET** /conditions/search | Search Conditions content
*CountriesApi* | [**getAllCountries**](docs/Api/CountriesApi.md#getallcountries) | **GET** /countries | Retrieve all countries
*CountriesApi* | [**getCountryByCca2**](docs/Api/CountriesApi.md#getcountrybycca2) | **GET** /countries/{cca2} | Retrieve a country by CCA2 code
*LivewellApi* | [**getLivewellLevelOne**](docs/Api/LivewellApi.md#getlivewelllevelone) | **GET** /live-well/{param-1} | Retrieve a first-level Live Well page
*LivewellApi* | [**getLivewellLevelThree**](docs/Api/LivewellApi.md#getlivewelllevelthree) | **GET** /live-well/{param-1}/{param-2}/{param-3} | Retrieve a third-level Live Well page
*LivewellApi* | [**getLivewellLevelTwo**](docs/Api/LivewellApi.md#getlivewellleveltwo) | **GET** /live-well/{param-1}/{param-2} | Retrieve a second-level Live Well page
*LivewellApi* | [**getLivewellRoutes**](docs/Api/LivewellApi.md#getlivewellroutes) | **GET** /live-well | Retrieve available Live Well routes
*LivewellApi* | [**searchLivewell**](docs/Api/LivewellApi.md#searchlivewell) | **GET** /live-well/search | Search Live Well content
*MeasurementsApi* | [**getActivityType**](docs/Api/MeasurementsApi.md#getactivitytype) | **GET** /measurements/activity-type/{id} | Retrieve an activity type by ID
*MeasurementsApi* | [**getActivityTypes**](docs/Api/MeasurementsApi.md#getactivitytypes) | **GET** /measurements/activity-type | Retrieve all activity types
*MeasurementsApi* | [**getBloodPressureMeasurement**](docs/Api/MeasurementsApi.md#getbloodpressuremeasurement) | **GET** /measurements/blood-pressure-measurement/{id} | Retrieve a blood pressure measurement type by ID
*MeasurementsApi* | [**getBloodPressureMeasurements**](docs/Api/MeasurementsApi.md#getbloodpressuremeasurements) | **GET** /measurements/blood-pressure-measurement | Retrieve all blood pressure measurement types
*MeasurementsApi* | [**getBloodSpecimenSource**](docs/Api/MeasurementsApi.md#getbloodspecimensource) | **GET** /measurements/blood-specimen-source/{id} | Retrieve a blood specimen source by ID
*MeasurementsApi* | [**getBloodSpecimenSources**](docs/Api/MeasurementsApi.md#getbloodspecimensources) | **GET** /measurements/blood-specimen-source | Retrieve all blood specimen sources
*MeasurementsApi* | [**getBodyPosition**](docs/Api/MeasurementsApi.md#getbodyposition) | **GET** /measurements/body-position/{id} | Retrieve a body position by ID
*MeasurementsApi* | [**getBodyPositions**](docs/Api/MeasurementsApi.md#getbodypositions) | **GET** /measurements/body-position | Retrieve all body positions
*MeasurementsApi* | [**getBodyTemperatureLocation**](docs/Api/MeasurementsApi.md#getbodytemperaturelocation) | **GET** /measurements/body-temperature-location/{id} | Retrieve a body temperature location by ID
*MeasurementsApi* | [**getBodyTemperatureLocations**](docs/Api/MeasurementsApi.md#getbodytemperaturelocations) | **GET** /measurements/body-temperature-location | Retrieve all body temperature locations
*MeasurementsApi* | [**getCervicalDilation**](docs/Api/MeasurementsApi.md#getcervicaldilation) | **GET** /measurements/cervical-dilation/{id} | Retrieve a cervical dilation by ID
*MeasurementsApi* | [**getCervicalDilations**](docs/Api/MeasurementsApi.md#getcervicaldilations) | **GET** /measurements/cervical-dilation | Retrieve all cervical dilations
*MeasurementsApi* | [**getCervicalFirmness**](docs/Api/MeasurementsApi.md#getcervicalfirmness) | **GET** /measurements/cervical-firmness/{id} | Retrieve a cervical firmness value by ID
*MeasurementsApi* | [**getCervicalFirmnessValues**](docs/Api/MeasurementsApi.md#getcervicalfirmnessvalues) | **GET** /measurements/cervical-firmness | Retrieve all cervical firmness values
*MeasurementsApi* | [**getCervicalMucusAmount**](docs/Api/MeasurementsApi.md#getcervicalmucusamount) | **GET** /measurements/cervical-mucus-amount/{id} | Retrieve a cervical mucus amount by ID
*MeasurementsApi* | [**getCervicalMucusAmounts**](docs/Api/MeasurementsApi.md#getcervicalmucusamounts) | **GET** /measurements/cervical-mucus-amount | Retrieve all cervical mucus amounts
*MeasurementsApi* | [**getCervicalMucusTexture**](docs/Api/MeasurementsApi.md#getcervicalmucustexture) | **GET** /measurements/cervical-mucus-texture/{id} | Retrieve a cervical mucus texture by ID
*MeasurementsApi* | [**getCervicalMucusTextures**](docs/Api/MeasurementsApi.md#getcervicalmucustextures) | **GET** /measurements/cervical-mucus-texture | Retrieve all cervical mucus textures
*MeasurementsApi* | [**getCervicalPosition**](docs/Api/MeasurementsApi.md#getcervicalposition) | **GET** /measurements/cervical-position/{id} | Retrieve a cervical position by ID
*MeasurementsApi* | [**getCervicalPositions**](docs/Api/MeasurementsApi.md#getcervicalpositions) | **GET** /measurements/cervical-position | Retrieve all cervical positions
*MeasurementsApi* | [**getExerciseTypeByName**](docs/Api/MeasurementsApi.md#getexercisetypebyname) | **GET** /measurements/exercise-type/{exercise_type_name} | Retrieve an exercise type by name
*MeasurementsApi* | [**getExerciseTypes**](docs/Api/MeasurementsApi.md#getexercisetypes) | **GET** /measurements/exercise-type | Retrieve all exercise types
*MeasurementsApi* | [**getMealType**](docs/Api/MeasurementsApi.md#getmealtype) | **GET** /measurements/meal-type/{id} | Retrieve a meal type by ID
*MeasurementsApi* | [**getMealTypes**](docs/Api/MeasurementsApi.md#getmealtypes) | **GET** /measurements/meal-type | Retrieve all meal types
*MeasurementsApi* | [**getMeasurementGroup**](docs/Api/MeasurementsApi.md#getmeasurementgroup) | **GET** /measurements/groups/{id} | Retrieve a measurement group by ID
*MeasurementsApi* | [**getMeasurementGroups**](docs/Api/MeasurementsApi.md#getmeasurementgroups) | **GET** /measurements/groups | Retrieve all measurement groups
*MeasurementsApi* | [**getMeasurementType**](docs/Api/MeasurementsApi.md#getmeasurementtype) | **GET** /measurements/types/{id} | Retrieve a measurement type by ID
*MeasurementsApi* | [**getMeasurementTypes**](docs/Api/MeasurementsApi.md#getmeasurementtypes) | **GET** /measurements/types | Retrieve all measurement types
*MeasurementsApi* | [**getMeasurementUnit**](docs/Api/MeasurementsApi.md#getmeasurementunit) | **GET** /measurements/units/{id} | Retrieve a unit of measure by ID
*MeasurementsApi* | [**getMeasurementUnits**](docs/Api/MeasurementsApi.md#getmeasurementunits) | **GET** /measurements/units | Retrieve all units of measure
*MeasurementsApi* | [**getResistanceType**](docs/Api/MeasurementsApi.md#getresistancetype) | **GET** /measurements/resistance-type/{id} | Retrieve a resistance type by ID
*MeasurementsApi* | [**getResistanceTypes**](docs/Api/MeasurementsApi.md#getresistancetypes) | **GET** /measurements/resistance-type | Retrieve all resistance types
*MeasurementsApi* | [**getSleepSegmentType**](docs/Api/MeasurementsApi.md#getsleepsegmenttype) | **GET** /measurements/sleep-segment-type/{id} | Retrieve a sleep segment type by ID
*MeasurementsApi* | [**getSleepSegmentTypes**](docs/Api/MeasurementsApi.md#getsleepsegmenttypes) | **GET** /measurements/sleep-segment-type | Retrieve all sleep segment types
*MeasurementsApi* | [**getTemporalRelationToMeal**](docs/Api/MeasurementsApi.md#gettemporalrelationtomeal) | **GET** /measurements/temporal-relation-to-meal/{id} | Retrieve a temporal relation to meals by ID
*MeasurementsApi* | [**getTemporalRelationToSleep**](docs/Api/MeasurementsApi.md#gettemporalrelationtosleep) | **GET** /measurements/temporal-relation-to-sleep/{id} | Retrieve a temporal relation to sleep by ID
*MeasurementsApi* | [**getTemporalRelationsToMeal**](docs/Api/MeasurementsApi.md#gettemporalrelationstomeal) | **GET** /measurements/temporal-relation-to-meal | Retrieve all temporal relations to meals
*MeasurementsApi* | [**getTemporalRelationsToSleep**](docs/Api/MeasurementsApi.md#gettemporalrelationstosleep) | **GET** /measurements/temporal-relation-to-sleep | Retrieve all temporal relations to sleep
*MedicinesApi* | [**getMedicineLevelOne**](docs/Api/MedicinesApi.md#getmedicinelevelone) | **GET** /medicines/{param1} | Retrieve a Medicine page
*MedicinesApi* | [**getMedicineLevelThree**](docs/Api/MedicinesApi.md#getmedicinelevelthree) | **GET** /medicines/{param1}/{param2}/{param3} | Retrieve a page within a nested Medicine
*MedicinesApi* | [**getMedicineLevelTwo**](docs/Api/MedicinesApi.md#getmedicineleveltwo) | **GET** /medicines/{param1}/{param2} | Retrieve a Medicine subpage or nested medicine
*MedicinesApi* | [**getMedicinesRoutes**](docs/Api/MedicinesApi.md#getmedicinesroutes) | **GET** /medicines | Retrieve available Medicines routes
*MedicinesApi* | [**searchMedicines**](docs/Api/MedicinesApi.md#searchmedicines) | **GET** /medicines/search | Search Medicines content
*MentalHealthApi* | [**getMentalHealthLevelFour**](docs/Api/MentalHealthApi.md#getmentalhealthlevelfour) | **GET** /mental-health/{param1}/{param2}/{param3}/{param4} | Retrieve deeply nested Mental Health content
*MentalHealthApi* | [**getMentalHealthLevelOne**](docs/Api/MentalHealthApi.md#getmentalhealthlevelone) | **GET** /mental-health/{param1} | Retrieve a Mental Health page
*MentalHealthApi* | [**getMentalHealthLevelThree**](docs/Api/MentalHealthApi.md#getmentalhealthlevelthree) | **GET** /mental-health/{param1}/{param2}/{param3} | Retrieve nested Mental Health content
*MentalHealthApi* | [**getMentalHealthLevelTwo**](docs/Api/MentalHealthApi.md#getmentalhealthleveltwo) | **GET** /mental-health/{param1}/{param2} | Retrieve a Mental Health subcategory
*MentalHealthApi* | [**getMentalHealthRoutes**](docs/Api/MentalHealthApi.md#getmentalhealthroutes) | **GET** /mental-health | Retrieve available Mental Health routes
*MentalHealthApi* | [**searchMentalHealth**](docs/Api/MentalHealthApi.md#searchmentalhealth) | **GET** /mental-health/search | Search Mental Health content
*PregnancyApi* | [**getPregnancyLevelOne**](docs/Api/PregnancyApi.md#getpregnancylevelone) | **GET** /pregnancy/{param1} | Retrieve a Pregnancy page
*PregnancyApi* | [**getPregnancyLevelThree**](docs/Api/PregnancyApi.md#getpregnancylevelthree) | **GET** /pregnancy/{param1}/{param2}/{param3} | Retrieve deeply nested Pregnancy content
*PregnancyApi* | [**getPregnancyLevelTwo**](docs/Api/PregnancyApi.md#getpregnancyleveltwo) | **GET** /pregnancy/{param1}/{param2} | Retrieve a Pregnancy subpage
*PregnancyApi* | [**getPregnancyRoutes**](docs/Api/PregnancyApi.md#getpregnancyroutes) | **GET** /pregnancy | Retrieve available Pregnancy routes
*PregnancyApi* | [**searchPregnancy**](docs/Api/PregnancyApi.md#searchpregnancy) | **GET** /pregnancy/search | Search Pregnancy content
*SearchApi* | [**searchMrd**](docs/Api/SearchApi.md#searchmrd) | **GET** /search | Search MRD content
*ValidationsApi* | [**getValidationLookupValues**](docs/Api/ValidationsApi.md#getvalidationlookupvalues) | **GET** /validations/lookup/{field_name} | Retrieve allowed values for a lookup field
*ValidationsApi* | [**getValidationMdsAllDatasetsAndFields**](docs/Api/ValidationsApi.md#getvalidationmdsalldatasetsandfields) | **GET** /validations/mds/all-datasets-and-fields | Retrieve all MDS datasets with extended field information
*ValidationsApi* | [**getValidationMdsDatasetFieldTypes**](docs/Api/ValidationsApi.md#getvalidationmdsdatasetfieldtypes) | **GET** /validations/mds/dataset/{dataset}/fieldtypes | Retrieve field types for an MDS dataset
*ValidationsApi* | [**getValidationMdsDatasetFields**](docs/Api/ValidationsApi.md#getvalidationmdsdatasetfields) | **GET** /validations/mds/dataset/{dataset} | Retrieve full field definitions for an MDS dataset
*ValidationsApi* | [**getValidationMdsDatasets**](docs/Api/ValidationsApi.md#getvalidationmdsdatasets) | **GET** /validations/mds/datasets | Retrieve MDS datasets
*ValidationsApi* | [**getValidationMdsDatasetsAndFields**](docs/Api/ValidationsApi.md#getvalidationmdsdatasetsandfields) | **GET** /validations/mds/datasets-and-fields | Retrieve MDS datasets and basic field information
*ValidationsApi* | [**getValidationMdsDatasetsByOneStatus**](docs/Api/ValidationsApi.md#getvalidationmdsdatasetsbyonestatus) | **GET** /validations/mds/datasets/{status1} | Retrieve MDS datasets by one status
*ValidationsApi* | [**getValidationMdsDatasetsByThreeStatuses**](docs/Api/ValidationsApi.md#getvalidationmdsdatasetsbythreestatuses) | **GET** /validations/mds/datasets/{status1}/{status2}/{status3} | Retrieve MDS datasets by three statuses
*ValidationsApi* | [**getValidationMdsDatasetsByTwoStatuses**](docs/Api/ValidationsApi.md#getvalidationmdsdatasetsbytwostatuses) | **GET** /validations/mds/datasets/{status1}/{status2} | Retrieve MDS datasets by two statuses
*ValidationsApi* | [**getValidationMdsDatasetsByType**](docs/Api/ValidationsApi.md#getvalidationmdsdatasetsbytype) | **GET** /validations/mds/datasets/type/{type} | Retrieve MDS datasets by type
*ValidationsApi* | [**getValidationMdsFieldType**](docs/Api/ValidationsApi.md#getvalidationmdsfieldtype) | **GET** /validations/mds/field/type/{field} | Retrieve an MDS field&#39;s data type
*ValidationsApi* | [**getValidationMdsSummary**](docs/Api/ValidationsApi.md#getvalidationmdssummary) | **GET** /validations/mds/summary | Retrieve an MDS summary
*ValidationsApi* | [**getValidationMtsFeatureByName**](docs/Api/ValidationsApi.md#getvalidationmtsfeaturebyname) | **GET** /validations/mts/features/{feature} | Retrieve an MTS feature by name
*ValidationsApi* | [**getValidationMtsFeatures**](docs/Api/ValidationsApi.md#getvalidationmtsfeatures) | **GET** /validations/mts/features | Retrieve all MTS features
*ValidationsApi* | [**getValidationMtsFeaturesByGroup**](docs/Api/ValidationsApi.md#getvalidationmtsfeaturesbygroup) | **GET** /validations/mts/features/group/{group} | Retrieve MTS features by group
*ValidationsApi* | [**getValidationMtsTemplateByModule**](docs/Api/ValidationsApi.md#getvalidationmtstemplatebymodule) | **GET** /validations/mts/templates/{template}/{module} | Retrieve an MTS template module
*ValidationsApi* | [**getValidationMtsTemplateByName**](docs/Api/ValidationsApi.md#getvalidationmtstemplatebyname) | **GET** /validations/mts/templates/{template} | Retrieve MTS template records by template name
*ValidationsApi* | [**getValidationMtsTemplateBySubsection**](docs/Api/ValidationsApi.md#getvalidationmtstemplatebysubsection) | **GET** /validations/mts/templates/{template}/{module}/{subsection} | Retrieve an MTS template subsection
*ValidationsApi* | [**getValidationMtsTemplates**](docs/Api/ValidationsApi.md#getvalidationmtstemplates) | **GET** /validations/mts/templates | Retrieve all MTS template records
*ValidationsApi* | [**searchValidationMdsFields**](docs/Api/ValidationsApi.md#searchvalidationmdsfields) | **GET** /validations/mds/search/{search} | Search MDS field names
*ValidationsApi* | [**validateLookupValue**](docs/Api/ValidationsApi.md#validatelookupvalue) | **GET** /validations/lookup/{field_name}/{user_input} | Validate a value against a lookup field

## Models

- [AlissAccessibilityFeature](docs/Model/AlissAccessibilityFeature.md)
- [AlissAccessibilityFeaturesFilter](docs/Model/AlissAccessibilityFeaturesFilter.md)
- [AlissCategoriesFilter](docs/Model/AlissCategoriesFilter.md)
- [AlissCommunityGroup](docs/Model/AlissCommunityGroup.md)
- [AlissCommunityGroupsFilter](docs/Model/AlissCommunityGroupsFilter.md)
- [AlissLocation](docs/Model/AlissLocation.md)
- [AlissLocationsFilter](docs/Model/AlissLocationsFilter.md)
- [AlissNamedSlugItem](docs/Model/AlissNamedSlugItem.md)
- [AlissOrganisation](docs/Model/AlissOrganisation.md)
- [AlissOrganisationsFilter](docs/Model/AlissOrganisationsFilter.md)
- [AlissService](docs/Model/AlissService.md)
- [AlissServiceArea](docs/Model/AlissServiceArea.md)
- [AlissServiceAreaReference](docs/Model/AlissServiceAreaReference.md)
- [AlissServiceAreasFilter](docs/Model/AlissServiceAreasFilter.md)
- [AlissServiceCount](docs/Model/AlissServiceCount.md)
- [AlissServicesFilter](docs/Model/AlissServicesFilter.md)
- [AuthErrorResponse](docs/Model/AuthErrorResponse.md)
- [AuthErrorResponseError](docs/Model/AuthErrorResponseError.md)
- [ConditionAbout](docs/Model/ConditionAbout.md)
- [ConditionAlternateName](docs/Model/ConditionAlternateName.md)
- [ConditionBreadcrumb](docs/Model/ConditionBreadcrumb.md)
- [ConditionBreadcrumbItemData](docs/Model/ConditionBreadcrumbItemData.md)
- [ConditionBreadcrumbListItem](docs/Model/ConditionBreadcrumbListItem.md)
- [ConditionContentNode](docs/Model/ConditionContentNode.md)
- [ConditionErrorResponse](docs/Model/ConditionErrorResponse.md)
- [ConditionExternalLinkObject](docs/Model/ConditionExternalLinkObject.md)
- [ConditionHealthTopicContent](docs/Model/ConditionHealthTopicContent.md)
- [ConditionKeywords](docs/Model/ConditionKeywords.md)
- [ConditionLinkValue](docs/Model/ConditionLinkValue.md)
- [ConditionMrdLinkObject](docs/Model/ConditionMrdLinkObject.md)
- [ConditionOrganisation](docs/Model/ConditionOrganisation.md)
- [ConditionPage](docs/Model/ConditionPage.md)
- [ConditionPotentialAction](docs/Model/ConditionPotentialAction.md)
- [ConditionRelatedLink](docs/Model/ConditionRelatedLink.md)
- [ConditionResponse](docs/Model/ConditionResponse.md)
- [ConditionSearchFilter](docs/Model/ConditionSearchFilter.md)
- [ConditionVideoObject](docs/Model/ConditionVideoObject.md)
- [ConditionVideoObjectIdentifier](docs/Model/ConditionVideoObjectIdentifier.md)
- [ConditionWebPageElement](docs/Model/ConditionWebPageElement.md)
- [ConditionsRouteListResponse](docs/Model/ConditionsRouteListResponse.md)
- [ConditionsSearchResponse](docs/Model/ConditionsSearchResponse.md)
- [CountriesErrorDetails](docs/Model/CountriesErrorDetails.md)
- [CountriesErrorResponse](docs/Model/CountriesErrorResponse.md)
- [Country](docs/Model/Country.md)
- [CountryCapitalInfo](docs/Model/CountryCapitalInfo.md)
- [CountryCar](docs/Model/CountryCar.md)
- [CountryCoatOfArms](docs/Model/CountryCoatOfArms.md)
- [CountryCurrency](docs/Model/CountryCurrency.md)
- [CountryDemonym](docs/Model/CountryDemonym.md)
- [CountryFlags](docs/Model/CountryFlags.md)
- [CountryIdd](docs/Model/CountryIdd.md)
- [CountryMaps](docs/Model/CountryMaps.md)
- [CountryName](docs/Model/CountryName.md)
- [CountryPostalCode](docs/Model/CountryPostalCode.md)
- [CountryTranslation](docs/Model/CountryTranslation.md)
- [ErrorResponse](docs/Model/ErrorResponse.md)
- [GetAllCountries200Response](docs/Model/GetAllCountries200Response.md)
- [GetCountryByCca2200Response](docs/Model/GetCountryByCca2200Response.md)
- [GetLivewellLevelOne200Response](docs/Model/GetLivewellLevelOne200Response.md)
- [GetMedicineLevelOne200Response](docs/Model/GetMedicineLevelOne200Response.md)
- [GetMentalHealthLevelOne200Response](docs/Model/GetMentalHealthLevelOne200Response.md)
- [GetPregnancyLevelOne200Response](docs/Model/GetPregnancyLevelOne200Response.md)
- [LivewellAbout](docs/Model/LivewellAbout.md)
- [LivewellAboutAlternateName](docs/Model/LivewellAboutAlternateName.md)
- [LivewellAnswer](docs/Model/LivewellAnswer.md)
- [LivewellAnswerLinksInner](docs/Model/LivewellAnswerLinksInner.md)
- [LivewellAuthor](docs/Model/LivewellAuthor.md)
- [LivewellBreadcrumb](docs/Model/LivewellBreadcrumb.md)
- [LivewellBreadcrumbItemData](docs/Model/LivewellBreadcrumbItemData.md)
- [LivewellBreadcrumbListItem](docs/Model/LivewellBreadcrumbListItem.md)
- [LivewellContentElement](docs/Model/LivewellContentElement.md)
- [LivewellContentElementMainEntityInner](docs/Model/LivewellContentElementMainEntityInner.md)
- [LivewellCopyrightHolder](docs/Model/LivewellCopyrightHolder.md)
- [LivewellData](docs/Model/LivewellData.md)
- [LivewellDataHasPartInner](docs/Model/LivewellDataHasPartInner.md)
- [LivewellErrorResponse](docs/Model/LivewellErrorResponse.md)
- [LivewellExpanderGroup](docs/Model/LivewellExpanderGroup.md)
- [LivewellExpanderItem](docs/Model/LivewellExpanderItem.md)
- [LivewellHealthTopicContent](docs/Model/LivewellHealthTopicContent.md)
- [LivewellLinkObject](docs/Model/LivewellLinkObject.md)
- [LivewellNotFoundResponse](docs/Model/LivewellNotFoundResponse.md)
- [LivewellRelatedLink](docs/Model/LivewellRelatedLink.md)
- [LivewellRoutesResponse](docs/Model/LivewellRoutesResponse.md)
- [LivewellSearchFilter](docs/Model/LivewellSearchFilter.md)
- [LivewellVideoObject](docs/Model/LivewellVideoObject.md)
- [LookupAllowedValuesResponse](docs/Model/LookupAllowedValuesResponse.md)
- [LookupValidationResponse](docs/Model/LookupValidationResponse.md)
- [MdsAllDatasetWithFields](docs/Model/MdsAllDatasetWithFields.md)
- [MdsAllField](docs/Model/MdsAllField.md)
- [MdsDatasetSummary](docs/Model/MdsDatasetSummary.md)
- [MdsDatasetWithFields](docs/Model/MdsDatasetWithFields.md)
- [MdsFieldDetails](docs/Model/MdsFieldDetails.md)
- [MdsFieldSearchResponse](docs/Model/MdsFieldSearchResponse.md)
- [MdsFieldSearchResponseMatchingFields](docs/Model/MdsFieldSearchResponseMatchingFields.md)
- [MdsFieldType](docs/Model/MdsFieldType.md)
- [MdsFieldTypeResponse](docs/Model/MdsFieldTypeResponse.md)
- [MdsSummaryCounts](docs/Model/MdsSummaryCounts.md)
- [MdsSummaryResponse](docs/Model/MdsSummaryResponse.md)
- [MeasurementActivityType](docs/Model/MeasurementActivityType.md)
- [MeasurementActivityTypeResult](docs/Model/MeasurementActivityTypeResult.md)
- [MeasurementActivityTypesResult](docs/Model/MeasurementActivityTypesResult.md)
- [MeasurementBloodPressureMeasurement](docs/Model/MeasurementBloodPressureMeasurement.md)
- [MeasurementBloodPressureMeasurementResult](docs/Model/MeasurementBloodPressureMeasurementResult.md)
- [MeasurementBloodPressureMeasurementsResult](docs/Model/MeasurementBloodPressureMeasurementsResult.md)
- [MeasurementBloodSpecimenSource](docs/Model/MeasurementBloodSpecimenSource.md)
- [MeasurementBloodSpecimenSourceResult](docs/Model/MeasurementBloodSpecimenSourceResult.md)
- [MeasurementBloodSpecimenSourcesResult](docs/Model/MeasurementBloodSpecimenSourcesResult.md)
- [MeasurementBodyPosition](docs/Model/MeasurementBodyPosition.md)
- [MeasurementBodyPositionResult](docs/Model/MeasurementBodyPositionResult.md)
- [MeasurementBodyPositionsResult](docs/Model/MeasurementBodyPositionsResult.md)
- [MeasurementBodyTemperatureLocation](docs/Model/MeasurementBodyTemperatureLocation.md)
- [MeasurementBodyTemperatureLocationResult](docs/Model/MeasurementBodyTemperatureLocationResult.md)
- [MeasurementBodyTemperatureLocationsResult](docs/Model/MeasurementBodyTemperatureLocationsResult.md)
- [MeasurementCervicalDilation](docs/Model/MeasurementCervicalDilation.md)
- [MeasurementCervicalDilationResult](docs/Model/MeasurementCervicalDilationResult.md)
- [MeasurementCervicalDilationsResult](docs/Model/MeasurementCervicalDilationsResult.md)
- [MeasurementCervicalFirmness](docs/Model/MeasurementCervicalFirmness.md)
- [MeasurementCervicalFirmnessResult](docs/Model/MeasurementCervicalFirmnessResult.md)
- [MeasurementCervicalFirmnessValuesResult](docs/Model/MeasurementCervicalFirmnessValuesResult.md)
- [MeasurementCervicalMucusAmount](docs/Model/MeasurementCervicalMucusAmount.md)
- [MeasurementCervicalMucusAmountResult](docs/Model/MeasurementCervicalMucusAmountResult.md)
- [MeasurementCervicalMucusAmountsResult](docs/Model/MeasurementCervicalMucusAmountsResult.md)
- [MeasurementCervicalMucusTexture](docs/Model/MeasurementCervicalMucusTexture.md)
- [MeasurementCervicalMucusTextureResult](docs/Model/MeasurementCervicalMucusTextureResult.md)
- [MeasurementCervicalMucusTexturesResult](docs/Model/MeasurementCervicalMucusTexturesResult.md)
- [MeasurementCervicalPosition](docs/Model/MeasurementCervicalPosition.md)
- [MeasurementCervicalPositionResult](docs/Model/MeasurementCervicalPositionResult.md)
- [MeasurementCervicalPositionsResult](docs/Model/MeasurementCervicalPositionsResult.md)
- [MeasurementExerciseType](docs/Model/MeasurementExerciseType.md)
- [MeasurementExerciseTypeResult](docs/Model/MeasurementExerciseTypeResult.md)
- [MeasurementExerciseTypesResult](docs/Model/MeasurementExerciseTypesResult.md)
- [MeasurementGroup](docs/Model/MeasurementGroup.md)
- [MeasurementGroupResult](docs/Model/MeasurementGroupResult.md)
- [MeasurementGroupsResult](docs/Model/MeasurementGroupsResult.md)
- [MeasurementMealType](docs/Model/MeasurementMealType.md)
- [MeasurementMealTypeResult](docs/Model/MeasurementMealTypeResult.md)
- [MeasurementMealTypesResult](docs/Model/MeasurementMealTypesResult.md)
- [MeasurementResistanceType](docs/Model/MeasurementResistanceType.md)
- [MeasurementResistanceTypeResult](docs/Model/MeasurementResistanceTypeResult.md)
- [MeasurementResistanceTypesResult](docs/Model/MeasurementResistanceTypesResult.md)
- [MeasurementSleepSegmentType](docs/Model/MeasurementSleepSegmentType.md)
- [MeasurementSleepSegmentTypeResult](docs/Model/MeasurementSleepSegmentTypeResult.md)
- [MeasurementSleepSegmentTypesResult](docs/Model/MeasurementSleepSegmentTypesResult.md)
- [MeasurementTemporalRelationToMeal](docs/Model/MeasurementTemporalRelationToMeal.md)
- [MeasurementTemporalRelationToMealResult](docs/Model/MeasurementTemporalRelationToMealResult.md)
- [MeasurementTemporalRelationToSleep](docs/Model/MeasurementTemporalRelationToSleep.md)
- [MeasurementTemporalRelationToSleepResult](docs/Model/MeasurementTemporalRelationToSleepResult.md)
- [MeasurementTemporalRelationsToMealResult](docs/Model/MeasurementTemporalRelationsToMealResult.md)
- [MeasurementTemporalRelationsToSleepResult](docs/Model/MeasurementTemporalRelationsToSleepResult.md)
- [MeasurementType](docs/Model/MeasurementType.md)
- [MeasurementTypeResult](docs/Model/MeasurementTypeResult.md)
- [MeasurementTypesResult](docs/Model/MeasurementTypesResult.md)
- [MeasurementUnit](docs/Model/MeasurementUnit.md)
- [MeasurementUnitResult](docs/Model/MeasurementUnitResult.md)
- [MeasurementUnitsResult](docs/Model/MeasurementUnitsResult.md)
- [MeasurementsDatabaseErrorResponse](docs/Model/MeasurementsDatabaseErrorResponse.md)
- [MeasurementsErrorDetails](docs/Model/MeasurementsErrorDetails.md)
- [MeasurementsErrorResponse](docs/Model/MeasurementsErrorResponse.md)
- [MedicineAbout](docs/Model/MedicineAbout.md)
- [MedicineAnswer](docs/Model/MedicineAnswer.md)
- [MedicineAnswerLinksInner](docs/Model/MedicineAnswerLinksInner.md)
- [MedicineAuthor](docs/Model/MedicineAuthor.md)
- [MedicineBreadcrumb](docs/Model/MedicineBreadcrumb.md)
- [MedicineBreadcrumbItemData](docs/Model/MedicineBreadcrumbItemData.md)
- [MedicineBreadcrumbListItem](docs/Model/MedicineBreadcrumbListItem.md)
- [MedicineContentElement](docs/Model/MedicineContentElement.md)
- [MedicineContentElementMainEntity](docs/Model/MedicineContentElementMainEntity.md)
- [MedicineCopyrightHolder](docs/Model/MedicineCopyrightHolder.md)
- [MedicineData](docs/Model/MedicineData.md)
- [MedicineHealthTopicContent](docs/Model/MedicineHealthTopicContent.md)
- [MedicineLinkObject](docs/Model/MedicineLinkObject.md)
- [MedicineNestedEntity](docs/Model/MedicineNestedEntity.md)
- [MedicineRelatedLink](docs/Model/MedicineRelatedLink.md)
- [MedicinesErrorResponse](docs/Model/MedicinesErrorResponse.md)
- [MedicinesNotFoundResponse](docs/Model/MedicinesNotFoundResponse.md)
- [MedicinesRoutesResponse](docs/Model/MedicinesRoutesResponse.md)
- [MedicinesSearchFilter](docs/Model/MedicinesSearchFilter.md)
- [MentalHealthAbout](docs/Model/MentalHealthAbout.md)
- [MentalHealthAnswer](docs/Model/MentalHealthAnswer.md)
- [MentalHealthAnswerLinksInner](docs/Model/MentalHealthAnswerLinksInner.md)
- [MentalHealthAuthor](docs/Model/MentalHealthAuthor.md)
- [MentalHealthBreadcrumb](docs/Model/MentalHealthBreadcrumb.md)
- [MentalHealthBreadcrumbItemData](docs/Model/MentalHealthBreadcrumbItemData.md)
- [MentalHealthBreadcrumbListItem](docs/Model/MentalHealthBreadcrumbListItem.md)
- [MentalHealthContentElement](docs/Model/MentalHealthContentElement.md)
- [MentalHealthContentElementMainEntity](docs/Model/MentalHealthContentElementMainEntity.md)
- [MentalHealthContentElementMainEntityOfPageInner](docs/Model/MentalHealthContentElementMainEntityOfPageInner.md)
- [MentalHealthCopyrightHolder](docs/Model/MentalHealthCopyrightHolder.md)
- [MentalHealthData](docs/Model/MentalHealthData.md)
- [MentalHealthErrorResponse](docs/Model/MentalHealthErrorResponse.md)
- [MentalHealthExpanderGroup](docs/Model/MentalHealthExpanderGroup.md)
- [MentalHealthExpanderItem](docs/Model/MentalHealthExpanderItem.md)
- [MentalHealthHealthTopicContent](docs/Model/MentalHealthHealthTopicContent.md)
- [MentalHealthLinkObject](docs/Model/MentalHealthLinkObject.md)
- [MentalHealthMainEntityObject](docs/Model/MentalHealthMainEntityObject.md)
- [MentalHealthNotFoundResponse](docs/Model/MentalHealthNotFoundResponse.md)
- [MentalHealthRelatedLink](docs/Model/MentalHealthRelatedLink.md)
- [MentalHealthRoutesResponse](docs/Model/MentalHealthRoutesResponse.md)
- [MentalHealthSearchFilter](docs/Model/MentalHealthSearchFilter.md)
- [MentalHealthVideoObject](docs/Model/MentalHealthVideoObject.md)
- [MtsFeatureRecord](docs/Model/MtsFeatureRecord.md)
- [MtsTemplateRecord](docs/Model/MtsTemplateRecord.md)
- [PaginatedSearchResponse](docs/Model/PaginatedSearchResponse.md)
- [PregnancyAbout](docs/Model/PregnancyAbout.md)
- [PregnancyAnswer](docs/Model/PregnancyAnswer.md)
- [PregnancyAnswerLinksInner](docs/Model/PregnancyAnswerLinksInner.md)
- [PregnancyAuthor](docs/Model/PregnancyAuthor.md)
- [PregnancyBreadcrumb](docs/Model/PregnancyBreadcrumb.md)
- [PregnancyBreadcrumbItemData](docs/Model/PregnancyBreadcrumbItemData.md)
- [PregnancyBreadcrumbListItem](docs/Model/PregnancyBreadcrumbListItem.md)
- [PregnancyContentElement](docs/Model/PregnancyContentElement.md)
- [PregnancyContentElementMainEntity](docs/Model/PregnancyContentElementMainEntity.md)
- [PregnancyContentElementMainEntityOfPageInner](docs/Model/PregnancyContentElementMainEntityOfPageInner.md)
- [PregnancyCopyrightHolder](docs/Model/PregnancyCopyrightHolder.md)
- [PregnancyData](docs/Model/PregnancyData.md)
- [PregnancyErrorResponse](docs/Model/PregnancyErrorResponse.md)
- [PregnancyExpanderGroup](docs/Model/PregnancyExpanderGroup.md)
- [PregnancyExpanderItem](docs/Model/PregnancyExpanderItem.md)
- [PregnancyHealthTopicContent](docs/Model/PregnancyHealthTopicContent.md)
- [PregnancyLinkObject](docs/Model/PregnancyLinkObject.md)
- [PregnancyMainEntityObject](docs/Model/PregnancyMainEntityObject.md)
- [PregnancyNotFoundResponse](docs/Model/PregnancyNotFoundResponse.md)
- [PregnancyRelatedLink](docs/Model/PregnancyRelatedLink.md)
- [PregnancyRoutesResponse](docs/Model/PregnancyRoutesResponse.md)
- [PregnancySearchFilter](docs/Model/PregnancySearchFilter.md)
- [PregnancyVideoObject](docs/Model/PregnancyVideoObject.md)
- [SearchAlissServicesFiltersParameter](docs/Model/SearchAlissServicesFiltersParameter.md)
- [SearchErrorDetails](docs/Model/SearchErrorDetails.md)
- [SearchErrorResponse](docs/Model/SearchErrorResponse.md)
- [SearchFilter](docs/Model/SearchFilter.md)
- [SearchMrd200Response](docs/Model/SearchMrd200Response.md)
- [SearchPagination](docs/Model/SearchPagination.md)
- [SearchResultItem](docs/Model/SearchResultItem.md)
- [UnpaginatedSearchResponse](docs/Model/UnpaginatedSearchResponse.md)
- [ValidationsErrorDetails](docs/Model/ValidationsErrorDetails.md)
- [ValidationsErrorResponse](docs/Model/ValidationsErrorResponse.md)

## Authorization

Authentication schemes defined for the API:
### oauth2

- **Type**: `OAuth`
- **Flow**: `application`
- **Authorization URL**: ``
- **Scopes**: 
    - **aliss**: Access ALISS routes
    - **conditions**: Access Conditions routes
    - **live-well**: Access Live Well routes
    - **medicines**: Access Medicines routes
    - **mental-health**: Access Mental Health routes
    - **pregnancy**: Access Pregnancy routes
    - **councils**: Access Councils routes
    - **countries**: Access Countries routes
    - **listings**: Access Listings routes
    - **measurements**: Access Measurements routes
    - **frn**: Access Financial Register routes
    - **geo-ip**: Access Geo-IP routes
    - **paf**: Access PAF routes
    - **suppliers**: Access Suppliers routes
    - **citizen-directory**: Access Citizen Directory routes
    - **service-directory**: Access Service Directory routes

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
    - Package version: `1.0.0`
    - Generator version: `7.23.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
