# Basic test

**Purpose**: Verify that the spatial data set contains at least one Geology feature.

**Prerequisites**

**Test method**

* Check that the set of [features](#features) in the spatial data set is not empty. Otherwise report [noFeature](#noFeature)

**Reference(s)**: 

* [TG DS-GE](./README.md#ref_TG_DS_GE) 5.4, 5.5

**Test type**: Automated

**Notes**

There is no requirement that we could reference in the Technical Guidelines. Maybe such a requirement should be added in the future revision?

## Messages

Identifier  |  Message text (parameters start with '$')
----------- | -------------------------------------------------------------------------
noFeature <a name="noFeature"/>  |  	The XML documents representing the spatial data set do not contain a feature of any of the spatial object types in the 'Geology' application schemas. Therefore, the spatial data set cannot conform to this conformance class. If you have expected to find spatial objects from the application schema in the data set, please consult the statistics information to see the spatial object types that have been found.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                          |  XPath expression
----------------------------------------------------- | ------------------------------------------------------------------
features <a name="features"></a>   |  //schema-element(ge-core:AnthropogenicGeomorphologicFeature) \| //schema-element(ge-core:Borehole) \| //schema-element(ge-core:Fold) \| //schema-element(ge-core:GeologicCollection) \| //schema-element(ge-core:GeologicEvent) \| //schema-element(ge-core:NaturalGeomorphologicFeature) \| //schema-element(ge-core:GeologicUnit) \| //schema-element(ge-core:MappedFeature) \| //schema-element(ge-core:MappedInterval)) \| //schema-element(ge-core:ShearDisplacementStructure) \| //schema-element(ge-core:Campaign)) \| //schema-element(ge-core:GeophObjectSet) \|  //schema-element(ge-core:GeophProfile) \| //schema-element(ge-core:GeophStation) \| //schema-element(ge-core:GeophSwath) \| //schema-element(ge-core:ActiveWell) \| //schema-element(ge-core:Aquifer) \| //schema-element(ge-core:AquiferSystem) \| //schema-element(ge-core:Aquitard) \| //schema-element(ge-core:GroundWaterBody) \| //schema-element(ge-core:HydrogeologicalObjectNatural) \| //schema-element(ge-core:Aquiclude)