# Code list values

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II, III and IV of the Implementing Rule. To pass this test verify that any instance of an attribute:

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.
* takes only a value explicitly specified in the INSPIRE code list register or shall take a value that is narrower (i.e. more specific) than those explicitly specified in the application schema when the code list‘s extensibility is 'narrower'.
* takes values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'open' or if a value is not one of the values listed in the code list register check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements (This last check is a manual test).

The following checks are performed for every feature in the dataset, for the 'open' codelists:

* Check that all the [anthropogenicGeomorphologicFeatureType](#anthropogenicGeomorphologicFeatureType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue1).
* Check that all the [purpose](#purpose) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue2).
* Check that all the [collectionType](#collectionType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue3).
* Check that all the [role](#role) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue4).
* Check that all the [material](#material) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue5).
* Check that all the [eventEnvironment](#eventEnvironment) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue6).
* Check that all the [eventProcess](#eventProcess) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue7).
* Check that all the [olderNamedAge](#olderNamedAge) elements and all the [youngerNamedAge](#youngerNamedAge) elements have a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue8).
* Check that all the [faultType](#faultType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue9).
* Check that all the [profileType](#profileType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue10).
* Check that all the [geologicUnitType](#geologicUnitType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue11).
* Check that all the [activity](#activity) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue12).
* Check that all the [naturalGeomorphologicFeatureType](#naturalGeomorphologicFeatureType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue13).
* Check that all the [mappingFrame](#mappingFrame) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue14).

If the check fails a manual check will be required asking to review the code list definition in order to verify that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).


| <a name="preDefinedValue1"></a> Pre-defined values for xlink:href attribute of [anthropogenicGeomorphologicFeatureType](#anthropogenicGeomorphologicFeatureType) element are available in the INSPIRE Registry| 
| ---- | 
| AnthropogenicGeomorphologicFeatureTypeValue: http://inspire.ec.europa.eu/codelist/AnthropogenicGeomorphologicFeatureTypeValue |

| <a name="preDefinedValue2"></a> Pre-defined values for xlink:href attribute of [purpose](#purpose) element are available in the INSPIRE Registry| 
| ---- | 
| BoreholePurposeValue: http://inspire.ec.europa.eu/codelist/BoreholePurposeValue |

| <a name="preDefinedValue3"></a> Pre-defined values for xlink:href attribute of [collectionType](#collectionType) element are available in the INSPIRE Registry| 
| ---- | 
| CollectionTypeValue: http://inspire.ec.europa.eu/codelist/CollectionTypeValue |

| <a name="preDefinedValue4"></a> Pre-defined values for xlink:href attribute of [role](#role) element are available in the INSPIRE Registry| 
| ---- | 
| CompositionPartRoleValue: http://inspire.ec.europa.eu/codelist/CompositionPartRoleValue |

| <a name="preDefinedValue5"></a> Pre-defined values for xlink:href attribute of [material](#material) element are available in the INSPIRE Registry| 
| ---- | 
| LithologyValue: http://inspire.ec.europa.eu/codelist/LithologyValue |

| <a name="preDefinedValue6"></a> Pre-defined values for xlink:href attribute of [eventEnvironment](#eventEnvironment) element are available in the INSPIRE Registry| 
| ---- | 
| EventEnvironmentValue: http://inspire.ec.europa.eu/codelist/EventEnvironmentValue |

| <a name="preDefinedValue7"></a> Pre-defined values for xlink:href attribute of [eventProcess](#eventProcess) element are available in the INSPIRE Registry| 
| ---- | 
| EventProcessValue: http://inspire.ec.europa.eu/codelist/EventProcessValue |

| <a name="preDefinedValue8"></a> Pre-defined values for xlink:href attribute of [olderNamedAge](#olderNamedAge) element and of [youngerNamedAge](#youngerNamedAge) element are available in the INSPIRE Registry| 
| ---- | 
| GeochronologicEraValue: http://inspire.ec.europa.eu/codelist/GeochronologicEraValue |

| <a name="preDefinedValue9"></a> Pre-defined values for xlink:href attribute of [faultType](#faultType) element are available in the INSPIRE Registry| 
| ---- | 
| FaultTypeValue: http://inspire.ec.europa.eu/codelist/FaultTypeValue |

| <a name="preDefinedValue10"></a> Pre-defined values for xlink:href attribute of [profileType](#profileType) element are available in the INSPIRE Registry| 
| ---- | 
| FoldProfileTypeValue: http://inspire.ec.europa.eu/codelist/FoldProfileTypeValue |

| <a name="preDefinedValue11"></a> Pre-defined values for xlink:href attribute of [geologicUnitType](#geologicUnitType) element are available in the INSPIRE Registry| 
| ---- | 
| GeologicUnitTypeValue: http://inspire.ec.europa.eu/codelist/GeologicUnitTypeValue |

| <a name="preDefinedValue12"></a> Pre-defined values for xlink:href attribute of [activity](#activity) element are available in the INSPIRE Registry| 
| ---- | 
| GeomorphologicActivityValue: http://inspire.ec.europa.eu/codelist/GeomorphologicActivityValue |

| <a name="preDefinedValue13"></a> Pre-defined values for xlink:href attribute of [naturalGeomorphologicFeatureType](#naturalGeomorphologicFeatureType) element are available in the INSPIRE Registry| 
| ---- | 
| NaturalGeomorphologicFeatureTypeValue: http://inspire.ec.europa.eu/codelist/NaturalGeomorphologicFeatureTypeValue |

| <a name="preDefinedValue14"></a> Pre-defined values for xlink:href attribute of [mappingFrame](#mappingFrame) element are available in the INSPIRE Registry| 
| ---- | 
| MappingFrameValue: http://inspire.ec.europa.eu/codelist/MappingFrameValue |

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
anthropogenicGeomorphologicFeatureType <a name="anthropogenicGeomorphologicFeatureType"></a> | //schema-element(ge:AnthropogenicGeomorphologicFeature)/ge:anthropogenicGeomorphologicFeatureType/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:AnthropogenicGeomorphologicFeature/ge:anthropogenicGeomorphologicFeatureType/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:AnthropogenicGeomorphologicFeature/ge:anthropogenicGeomorphologicFeatureType/@xlink:href | 1 | No
purpose <a name="purpose"></a> | //schema-element(ge:Borehole)/ge:purpose/@xlink:href | 1..\* | No
collectionType <a name="collectionType"></a> | //schema-element(ge:GeologicCollection)/ge:collectionType/@xlink:href | 1 | No
role <a name="role"></a> | //schema-element(ge:GeologicUnit)/ge:composition/ge:CompositionPart/ge:role/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:GeologicUnit/ge:composition/ge:CompositionPart/ge:role/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:GeologicUnit/ge:composition/ge:CompositionPart/ge:role/@xlink:href | 1 (1..\* for the parent data type) |Yes
material <a name="material"></a> | //schema-element(ge:GeologicUnit)/ge:composition/ge:CompositionPart/ge:material/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:GeologicUnit/ge:composition/ge:CompositionPart/ge:material/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:GeologicUnit/ge:composition/ge:CompositionPart/ge:material/@xlink:href | 1 (1..\* for the parent data type) |No
eventEnvironment <a name="eventEnvironment"></a> | //schema-element(ge:GeologicEvent)/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:GeologicUnit)/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:ShearDisplacementStructure)/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:Fold)/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:AnthropogenicGeomorphologicFeature)/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:NaturalGeomorphologicFeature)/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:GeologicUnit/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:ShearDisplacementStructure/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:Fold/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:AnthropogenicGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:NaturalGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:GeologicUnit/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:ShearDisplacementStructure/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:Fold/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:AnthropogenicGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:NaturalGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:eventEnvironment/@xlink:href | 1 | Yes
eventProcess <a name="eventProcess"></a> | //schema-element(ge:GeologicEvent)/ge:eventProcess/@xlink:href <br> //schema-element(ge:GeologicUnit)/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:ShearDisplacementStructure)/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:Fold)/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:AnthropogenicGeomorphologicFeature)/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:NaturalGeomorphologicFeature)/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:GeologicUnit/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:ShearDisplacementStructure/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:Fold/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:AnthropogenicGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:NaturalGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:GeologicUnit/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:ShearDisplacementStructure/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:Fold/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:AnthropogenicGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:NaturalGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:eventProcess/@xlink:href | 1..\* | Yes
olderNamedAge <a name="olderNamedAge"></a> | //schema-element(ge:GeologicEvent)/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:GeologicUnit)/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:ShearDisplacementStructure)/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:Fold)/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:AnthropogenicGeomorphologicFeature)/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:NaturalGeomorphologicFeature)/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:GeologicUnit/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:ShearDisplacementStructure/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:Fold/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:AnthropogenicGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:NaturalGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:GeologicUnit/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:ShearDisplacementStructure/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:Fold/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:AnthropogenicGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:NaturalGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:olderNamedAge/@xlink:href | 1 | Yes
youngerNamedAge <a name="youngerNamedAge"></a> | //schema-element(ge:GeologicEvent)/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:GeologicUnit)/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:ShearDisplacementStructure)/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:Fold)/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:AnthropogenicGeomorphologicFeature)/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:NaturalGeomorphologicFeature)/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:GeologicUnit/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:ShearDisplacementStructure/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:Fold/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:AnthropogenicGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:NaturalGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:GeologicUnit/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:ShearDisplacementStructure/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:Fold/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:AnthropogenicGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:NaturalGeomorphologicFeature/ge:geologicHistory/ge:GeologicEvent/ge:youngerNamedAge/@xlink:href | 1 | Yes
faultType <a name="faultType"></a> | //schema-element(ge:ShearDisplacementStructure)/ge:faultType/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:ShearDisplacementStructure/ge:faultType/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:ShearDisplacementStructure/ge:faultType/@xlink:href | 1 | No
profileType <a name="profileType"></a> | //schema-element(ge:Fold)/ge:profileType/@xlink:href  <br> //schema-element(ge:MappedFeature)/ge:specification/ge:Fold/ge:profileType/@xlink:href  <br> //schema-element(ge:MappedInterval)/ge:specification/ge:Fold/ge:profileType/@xlink:href | 1 | Yes
geologicUnitType <a name="geologicUnitType"></a> | //schema-element(ge:GeologicUnit)/ge:geologicUnitType/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:GeologicUnit/ge:geologicUnitType/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:GeologicUnit/ge:geologicUnitType/@xlink:href | 1 | No
activity <a name="activity"></a> | //schema-element(ge:NaturalGeomorphologicFeature)/ge:activity/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:NaturalGeomorphologicFeature/ge:activity/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:NaturalGeomorphologicFeature/ge:activity/@xlink:href | 0..1 | No
naturalGeomorphologicFeatureType <a name="naturalGeomorphologicFeatureType"></a> | //schema-element(ge:NaturalGeomorphologicFeature)/ge:naturalGeomorphologicFeatureType/@xlink:href <br> //schema-element(ge:MappedFeature)/ge:specification/ge:NaturalGeomorphologicFeature/ge:naturalGeomorphologicFeatureType/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/ge:NaturalGeomorphologicFeature/ge:naturalGeomorphologicFeatureType/@xlink:href | 1 | No
mappingFrame <a name="mappingFrame"></a> | //schema-element(ge:MappedFeature)/ge:mappingFrame/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:mappingFrame/@xlink:href| 1 | No
