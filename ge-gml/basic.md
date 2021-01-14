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
features <a name="features"></a>   |  //schema-element(ge:AnthropogenicGeomorphologicFeature) \| //schema-element(ge:Borehole) \| //schema-element(ge:Fold) \| //schema-element(ge:GeologicCollection) \| //schema-element(ge:GeologicEvent) \| //schema-element(ge:NaturalGeomorphologicFeature) \| //schema-element(ge:GeologicUnit) \| //schema-element(ge:MappedFeature) \| //schema-element(ge:MappedInterval)) \| //schema-element(ge:ShearDisplacementStructure) \| //schema-element(ge-gp:Campaign)) \| //schema-element(ge-gp:GeophObjectSet) \|  //schema-element(ge-gp:GeophProfile) \| //schema-element(ge-gp:GeophStation) \| //schema-element(ge-gp:GeophSwath) \| //schema-element(ge-hg:ActiveWell) \| //schema-element(ge-hg:Aquifer) \| //schema-element(ge-hg:AquiferSystem) \| //schema-element(ge-hg:Aquitard) \| //schema-element(ge-hg:GroundWaterBody) \| //schema-element(ge-hg:HydrogeologicalObjectNatural) \| //schema-element(ge-hg:Aquiclude)
