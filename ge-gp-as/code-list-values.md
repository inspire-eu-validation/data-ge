# Code list values

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II, III and IV of the Implementing Rule. To pass this test verify that any instance of an attribute:

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.
* takes only a value explicitly specified in the INSPIRE code list register or shall take a value that is narrower (i.e. more specific) than those explicitly specified in the application schema when the code list‘s extensibility is 'narrower'.
* takes values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'open' or if a value is not one of the values listed in the code list register check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements (This last check is a manual test).

The following check are performed for every feature in the dataset, for the 'open' codelists:

* Check that all the [campaignType](#campaignType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue1).
* Check that all the [surveyType](#surveyType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue2).
* Check that all the [relatedNetwork](#relatedNetwork) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue3).
* Check that all the [platformType](#platformType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue4).
* Check that all the [profileType](#profileType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue5).
* Check that all the [stationType](#stationType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue6).
* Check that all the [stationRank](#stationRank) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue7).
* Check that all the [swathType](#swathType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue8).

If the check fails a manual check will be required asking to review the code list definition in order to verify that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).


| <a name="preDefinedValue1"></a> Pre-defined values for xlink:href attribute of [campaignType](#campaignType) element are available in the INSPIRE Registry| 
| ---- | 
| CampaignTypeValue: http://inspire.ec.europa.eu/codelist/CampaignTypeValue |

| <a name="preDefinedValue2"></a> Pre-defined values for xlink:href attribute of [surveyType](#surveyType) element are available in the INSPIRE Registry| 
| ---- | 
| SurveyTypeValue: http://inspire.ec.europa.eu/codelist/SurveyTypeValue |

| <a name="preDefinedValue3"></a> Pre-defined values for xlink:href attribute of [relatedNetwork](#relatedNetwork) element are available in the INSPIRE Registry| 
| ---- | 
| NetworkNameValue: http://inspire.ec.europa.eu/codelist/NetworkNameValue |

| <a name="preDefinedValue4"></a> Pre-defined values for xlink:href attribute of [platformType](#platformType) element are available in the INSPIRE Registry| 
| ---- | 
| PlatformTypeValue: http://inspire.ec.europa.eu/codelist/PlatformTypeValue |

| <a name="preDefinedValue5"></a> Pre-defined values for xlink:href attribute of [profileType](#profileType) element are available in the INSPIRE Registry| 
| ---- | 
| ProfileTypeValue: http://inspire.ec.europa.eu/codelist/ProfileTypeValue |

| <a name="preDefinedValue6"></a> Pre-defined values for xlink:href attribute of [stationType](#stationType) element are available in the INSPIRE Registry| 
| ---- | 
| StationTypeValue: http://inspire.ec.europa.eu/codelist/StationTypeValue |

| <a name="preDefinedValue7"></a> Pre-defined values for xlink:href attribute of [stationRank](#stationRank) element are available in the INSPIRE Registry| 
| ---- | 
| StationRankValue: http://inspire.ec.europa.eu/codelist/StationRankValue |

| <a name="preDefinedValue8"></a> Pre-defined values for xlink:href attribute of [swathType](#swathType) element are available in the INSPIRE Registry| 
| ---- | 
| SwathTypeValue: http://inspire.ec.europa.eu/codelist/SwathTypeValue |


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
campaignType <a name="campaignType"></a> | //schema-element(ge_gp:Campaign)/ge_gp:campaignType/@xlink:href | 1 | No
surveyType <a name="surveyType"></a> | //schema-element(ge_gp:Campaign)/ge_gp:surveyType/@xlink:href | 1 | No
relatedNetwork <a name="relatedNetwork"></a> | //schema-element(ge_gp:GeophStation)/ge_gp:relatedNetwork/@xlink:href <br> //schema-element(ge_gp:GeophProfile)/ge_gp:relatedNetwork/@xlink:href <br> //schema-element(ge_gp:GeophSwath)/ge_gp:relatedNetwork/@xlink:href | 1..\* | Yes
platformType <a name="platformType"></a> | //schema-element(ge_gp:GeophStation)/ge_gp:platformType/@xlink:href <br> //schema-element(ge_gp:GeophProfile)/ge_gp:platformType/@xlink:href <br> //schema-element(ge_gp:GeophSwath)/ge_gp:platformType/@xlink:href | 1 | No
profileType <a name="profileType"></a> | //schema-element(ge_gp:GeophProfile)/ge_gp:profileType/@xlink:href | 1 | No 
stationType <a name="stationType"></a> | //schema-element(ge_gp:GeophStation)/ge_gp:stationType/@xlink:href | 1 | No 
stationRank <a name="stationRank"></a> | //schema-element(ge_gp:GeophStation)/ge_gp:stationRank/@xlink:href | 1..\* | Yes 
swathType <a name="swathType"></a> | //schema-element(ge_gp:GeophSwath)/ge_gp:swathType/@xlink:href | 1 | No