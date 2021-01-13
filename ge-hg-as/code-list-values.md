# Code list values

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II, III and IV of the Implementing Rule. To pass this test verify that any instance of an attribute:

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.
* takes only a value explicitly specified in the INSPIRE code list register or shall take a value that is narrower (i.e. more specific) than those explicitly specified in the application schema when the code list‘s extensibility is 'narrower'.
* takes values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'open' or if a value is not one of the values listed in the code list register check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements (This last check is a manual test).

The following checks are performed for every feature in the dataset, for the not extensible codelists:

* Check that all the [aquiferType](#aquiferType) elements has a xlink:href attribute pointing to a [valid value](#validValue1). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

* Check that all the [conditionOfGroundWaterBody](#conditionOfGroundWaterBody) elements has a xlink:href attribute pointing to a [valid value](#validValue2). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue1"></a> Valid values for xlink:href attribute of [aquiferType](#aquiferType) element are available in the INSPIRE Registry| 
| ---- | 
| AquiferTypeValue: http://inspire.ec.europa.eu/codelist/AquiferTypeValue | 

| <a name="validValue2"></a> Valid values for xlink:href attribute of [conditionOfGroundWaterBody](#conditionOfGroundWaterBody) element are available in the INSPIRE Registry| 
| ---- | 
| ConditionOfGroundwaterValue: http://inspire.ec.europa.eu/codelist/ConditionOfGroundwaterValue | 


The following checks are performed for every feature in the dataset, for the 'open' codelists:

* Check that all the [activityType](#activityType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue1).
* Check that all the [mediaType](#mediaType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue2).
* Check that all the [hydroGeochemicalRockType](#hydroGeochemicalRockType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue3).
* Check that all the [naturalObjectType](#naturalObjectType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue4).
* Check that all the [waterPersistence](#waterPersistence) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue5).
* Check that all the [statusCode](#statusCode) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue6).
* Check that all the [mineralization](#mineralization) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue7).


If the check fails a manual check will be required asking to review the code list definition in order to verify that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).


| <a name="preDefinedValue1"></a> Pre-defined values for xlink:href attribute of [activityType](#activityType) element are available in the INSPIRE Registry| 
| ---- | 
| ActiveWellTypeValue: http://inspire.ec.europa.eu/codelist/ActiveWellTypeValue |

| <a name="preDefinedValue2"></a> Pre-defined values for xlink:href attribute of [mediaType](#mediaType) element are available in the INSPIRE Registry| 
| ---- | 
| AquiferMediaTypeValue: http://inspire.ec.europa.eu/codelist/AquiferMediaTypeValue |

| <a name="preDefinedValue3"></a> Pre-defined values for xlink:href attribute of [hydroGeochemicalRockType](#hydroGeochemicalRockType) element are available in the INSPIRE Registry| 
| ---- | 
| HydroGeochemicalRockTypeValue: http://inspire.ec.europa.eu/codelist/HydroGeochemicalRockTypeValue |

| <a name="preDefinedValue4"></a> Pre-defined values for xlink:href attribute of [naturalObjectType](#naturalObjectType) element are available in the INSPIRE Registry| 
| ---- | 
| NaturalObjectTypeValue: http://inspire.ec.europa.eu/codelist/NaturalObjectTypeValue |

| <a name="preDefinedValue5"></a> Pre-defined values for xlink:href attribute of [waterPersistence](#waterPersistence) element are available in the INSPIRE Registry| 
| ---- | 
| WaterPersistenceValue: http://inspire.ec.europa.eu/codelist/WaterPersistenceValue |

| <a name="preDefinedValue6"></a> Pre-defined values for xlink:href attribute of [statusCode](#statusCode) element are available in the INSPIRE Registry| 
| ---- | 
| StatusCodeTypeValue: http://inspire.ec.europa.eu/codelist/StatusCodeTypeValue |

| <a name="preDefinedValue7"></a> Pre-defined values for xlink:href attribute of [mineralization](#mineralization) element are available in the INSPIRE Registry| 
| ---- | 
| WaterSalinityValue: http://inspire.ec.europa.eu/codelist/WaterSalinityValue |


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Automated + Manual check (if required)

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/> | XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. Please note that the URIs of all code list values from the INSPIRE Registry shall be referenced using the http protocol. 
reviewCodeListValue <a name="reviewCodeListValue"/> | XML document '{filename}', {featureType} '{gmlid}': The property '{property}' has a value '{value}' that is not one of the pre-defined values in the INSPIRE data specification. The same value is used by {count} other features in the dataset, too. Extensions to the pre-defined values are allowed, but must not overlap with one of the pre-defined values and be consistent with the specification of the property. Please review the definition of the value. Please note that the URIs of all code list values from the INSPIRE Registry shall be referenced using the http protocol. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression				|Multiplicity       |Voidable
---------------------------------------------------------- | -------------------------------|-------------------|---------
aquiferType <a name="aquiferType"></a> | //schema-element(ge_hg:Aquifer)/ge_hg:aquiferType/@xlink:href  | 1 | No
conditionOfGroundWaterBody <a name="conditionOfGroundWaterBody"></a> | //schema-element(ge_hg:GroundWaterBody)/ge_hg:conditionOfGroundWaterBody/@xlink:href  | 1 | No
activityType <a name="activityType"></a> | //schema-element(ge_hg:ActiveWell)/ge_hg:activityType/@xlink:href  | 1..\* | No
mediaType <a name="mediaType"></a> | //schema-element(ge_hg:Aquifer)/ge_hg:mediaType/@xlink:href  | 1 | No
hydroGeochemicalRockType <a name="hydroGeochemicalRockType"></a> | //schema-element(ge_hg:Aquifer)/ge_hg:hydroGeochemicalRockType/@xlink:href  | 1 | Yes
naturalObjectType <a name="naturalObjectType"></a> | //schema-element(ge_hg:HydrogeologicalObjectNatural)/ge_hg:naturalObjectType/@xlink:href  | 1 | No
waterPersistence <a name="waterPersistence"></a> | //schema-element(ge_hg:HydrogeologicalObjectNatural)/ge_hg:waterPersistence/@xlink:href  | 1 | Yes
statusCode <a name="statusCode"></a> | //schema-element(ge_hg:ActiveWell)/ge_hg:statusCode/@xlink:href  | 1 | Yes
mineralization <a name="mineralization"></a> | //schema-element(ge_hg:GroundWaterBody)/ge_hg:mineralization/@xlink:href  | 1 | Yes