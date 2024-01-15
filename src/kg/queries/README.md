# Queries


### get_all_frameworks
|   topic                   | information                                                       |          
|---------------------------|-------------------------------------------------------------------|
| query name                  | get_all_frameworks              | 
| Use Case                  | get all available frameworks in the knowledge graph               | 
| additional explanations:  | no changes for the input/output from demo-search                                                                | 
| inputs                    | -                                                                 |   
| outputs                   | <ul><li>frameworkKey: iri</li><li>frameworkLabel: str </li></ul>  | 

### get_all_framework SP5

For SP5 use this query to query the framework.

|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_all_frameworks_SP5             | 
| Use Case                  | get all available frameworks in the knowledge graph   | 
| additional explanations:  | SP5 only needs a subset, query will be changed, but interface will stay the same                                                  | 
| inputs                    | -                                                     |   
| outputs                   | <ul><li>frameworkKey: iri</li><li>frameworkLabel: str </li></ul>      | 

### get_all_operational_boundaries
|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_all_operational_boundaries              | 
| Use Case                  | get all available operational boundaries in the knowledge graph   | 
| additional explanations:  | no changes for the input/output from demo-search                                                    | 
| inputs                    | -                                                     |   
| outputs                   | <ul><li>operationalBoundaryKey: iri</li><li>operationalBoundaryLabel: str </li></ul>               | 


### get_all_operational_boundaries_by_framework
|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_all_operational_boundaries_by_framework              | 
| Use Case                  | get all available operational boundaries in the knowledge graph given a certain framework   | 
| additional explanations:  | no changes for the input/output from demo-search, except the new parameter                                                   | 
| inputs                    | <ul><li>$frameworkKey: iri(e.g. \<https://purl.org/wiser#GHG_CP_LOC\>)</li></ul>                                                   |   
| outputs                   | <ul><li>operationalBoundaryKey: iri</li><li>operationalBoundaryLabel: str </li></ul>                | 


### get_all_categories
|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_all_categories              | 
| Use Case                  | get all available categories in the knowledge graph   | 
| additional explanations:  | no changes for the input/output from demo-search                                                 | 
| inputs                    | -                                                     |   
| outputs                   | <ul><li>categoryKey: iri</li><li>categoryLabel: str </li></ul>               | 

### get_all_categories_by_framework

<mark>Only valid for the prototype.<mark> 

A category can belong to a different operational boundary for another framework, that is why it is best to use the operational boundary as a filter as well. The suggested usage is listed as the next query.This use case is not covered in the prototype, so this query will always be correct for the prototype.

|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_all_categories_by_framework              | 
| Use Case                  | get all available categories in the knowledge graph given a certain framework   | 
| additional explanations:  | no changes for the input/output from demo-search, except the new parameter                                                 | 
| inputs                    | <ul><li>$frameworkKey: iri(e.g. \<https://purl.org/wiser#GHG_CP_LOC\>)</li></ul>                                                     |   
| outputs                   | <ul><li>categoryKey: iri</li><li>categoryLabel: str </li></ul>               | 

### get_all_categories_by_framework_and_operational_boundary 

|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_all_categories_by_framework_and_operational_boundary              | 
| Use Case                  | get all available categories in the knowledge graph given a certain framework and operational boundary  | 
| additional explanations:  | usage suggestion                                                 | 
| inputs                    | <ul><li>$frameworkKey: iri(e.g. \<https://purl.org/wiser#GHG_CP_LOC\>)</li></ul>                                                     |   
| outputs                   | <ul><li>categoryKey: iri</li><li>categoryLabel: str </li></ul>               | 


### get_classification_from_category 

A classification is uniquely mapped to the triple (framework - operational boundary - category), since depending on the category it can include more or less classification given a certain framework and operational boundary. The suggested usage is listed as the next query. This use case is not covered in the prototype, so this query will always be correct for the prototype.

|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_classification_from_category              | 
| Use Case                  | get all available classifications in the knowledge graph given a certain framework, operational boundary and category   | 
| additional explanations:  | no changes for the input/output from demo-search                                              | 
| inputs                    | <ul><li>$categoryKey: iri (e.g. \<https://purl.org/wiser#Category_TRANSPORTATION_AND_DISTRIBUTION\>)</li></ul>                       |   
| outputs                   | <ul><li>classificationKey: iri</li><li>categoryLabel: str </li></ul>                 | 


### get_classification_from_category_and_operational_boundary_and_framework 

|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_classification_from_category_and_operational_boundary_and_framework              | 
| Use Case                  |    | 
| additional explanations:  | usage suggestion                                                 | 
| inputs                    | <ul><li> $fwFilter: iri (e.g. \<https://purl.org/wiser#GHG_CP_LOC\>) </li><li> $catFilter: iri (e.g. \<https://purl.org/wiser#Category_TRANSPORTATION_AND_DISTRIBUTION\>)</li><li> $obFilter: iri (e.g. \<https://purl.org/wiser#OB_SCOPE_3_UPSTREAM\> )</li></ul>                                                   |   
| outputs                   | <ul><li>classificationKey: iri</li><li>categoryLabel: str </li></ul>               | 


### get_all_countries 

|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_all_countries              | 
| Use Case                  | get all available countries in the knowledge graph   | 
| additional explanations:  | changes in the language parameter          | 
| inputs                    | <ul><li> $language: str (in \"\", e.g. \"en\")</li></ul>                                                   |   
| outputs                   | <ul><li>country: iri</li><li>countryName: str </li><li>countryCode: str </li></ul>               | 


### get_rankings_for_geographies 

|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_rankings_for_geographies              | 
| Use Case                  | get all geographical search codes (e.g. CH, RER, etc.) for a given Geography-IRI retrieved with the geography  | 
| additional explanations:  | changes in the language parameter                   | 
| inputs                    | <ul><li> $filter: iri (e.g. \<https://sws.geonames.org/2658434/\>)</li></ul>  |   
| outputs                   | <ul><li>possibleCountryCode: str</li><li>ranking: number </li></ul>   | 


### get_ecospold01_data_by_geography_search_string


|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_ecospold01_data_by_geography_search_string              | 
| Use Case                  | get the Data from the UVEK-database (ecospold01-format) in the same fashion as the ecoinvent-database (hopefully :-D)   | 
| additional explanations:  | searchString (querying the name of the activity) and geographySearchString are mandatory, classificationString is optional. The geographySearchString is the countryCode from the geography-queries above (country or region does not matter). The return value returns an IRI for an activity with the information relevant for the SP5 screen (so far). SearchString must be in non-capital letters.                                            | 
| inputs                    | <ul><li> $searchString: str (e.g. "laptop")</li><li> $geographySearchString: str (e.g. "CH")</li><li> $classificationString: iri (e.g. "https://purl.org/wiser#WISER_Classification_2013_MANUFACTURE_OF_PLASTICS_AND_SYNTHETIC_RUBBER_IN_PRIMARY_FORMS")</li></ul>                                                   |   
| outputs                   | <ul><li>act: iri</li><li>referenceProduct: str </li><li>activity: str </li><li>location: str </li></ul>               | 


### get_ecospold01_data_by_geography_iri

|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_ecospold01_data_by_geography_iri             | 
| Use Case                  | get the Data from the UVEK-database (ecospold01-format) in the same fashion as the ecoinvent-database (hopefully :-D)   | 
| additional explanations:  | searchString (querying the name of the activity) and geographyIRI are mandatory, classificationString is optional. The geographyIRI is the countryCode from the geography-queries above (country or region does not matter). The return value returns an IRI for an activity with the information relevant for the SP5 screen (so far). SearchString must be in non-capital letters. In addition to the query above, this query includes the ranking of the selected dataset related to the given geographyIRI directly. The query itself is slower though                                           | 
| inputs                    | <ul><li> $searchString: str (e.g. "laptop")</li><li> $geographySearchString: str (e.g. "CH")</li><li> $classificationString: iri (e.g. "https://purl.org/wiser#WISER_Classification_2013_MANUFACTURE_OF_PLASTICS_AND_SYNTHETIC_RUBBER_IN_PRIMARY_FORMS")</li></ul>                                                   |   
| outputs                   | <ul><li>act: iri</li><li>referenceProduct: str </li><li>activity: str </li><li>location: str </li><li>ranking: number </li></ul>               | 

### get_ghg_emission_factor

|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | get_ghg_emission_factor              | 
| Use Case                  | get GHG-Emission-Factor (at the moment for any LCIA-Method) for the UVEK-dataset (Ecospold01)   | 
| additional explanations:  | lciaMethod is ignored, you can put there whatever you like, you will get the same number                                          | 
| inputs                    | <ul><li> $act: iri (e.g. \<http://www.EcoInvent.org/EcoSpold01#b1d8fafd-86d3-b2f0-0f31-8e10b0218d0c\>)</li><li> $lciaMethod: str (e.g. "iDontCare")</li></ul>                                                   |   
| outputs                   | <ul><li>act: iri</li><li>ghgEmissionFactor: decimal </li></ul>               | 


### change_framework_per_item

|   topic                   | information                                           |          
|---------------------------|-------------------------------------------------------|
| query name                  | change_framework_per_item              | 
| Use Case                  | switch from one framework to another   | 
| additional explanations:  | can return one entry, which is perfect, but can also return several entries, which then would lead to a user action to choose which new category/operational boundary combination is the most relevant                                         | 
| inputs                    | <ul><li> $newFW: iri (e.g. \<https://purl.org/wiser#ISO\>)</li><li> $oldFW: iri (e.g. \<https://purl.org/wiser#GHG_CP_LOC\>)</li><li> $oldCat: iri (e.g. \<https://purl.org/wiser#Category_END_OF_LIFE_TREATMENT_OF_SOLD_PRODUCTS\>)</li><li> $oldOB: iri (e.g. \<https://purl.org/wiser#OB_SCOPE_3_DOWNSTREAM\>)</li><li> $oldClassification: iri (e.g. \<https://purl.org/wiser#Classification_3900_REMEDIATION_ACTIVITIES_AND_OTHER_WASTE_MANAGEMENT_SERVICES\>)</li></ul>                                                  |   
| outputs                   | <ul><li>newOB: iri</li><li>obLabel: str </li><li>newCategory: iri</li><li>catLabel: str </li></ul>               | 