# Conformance class: Information accessibility, Geology

Conformance class for the requirements related to the accessibility of referenced information, for example, information stored in registries (code lists, coordinate reference systems).

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Geology".

This conformance class is part of the [INSPIRE Data Specification on Geology](../README.md).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [Information accessibility](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/information-accessibility) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-GE](#ref_TG_DS_GE) | [GML application schemas, Geology](../ge-gml/README.md) | INSPIRE spatial data set encoded in GML, Geology features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types are:

* Anthropogenic Geomorphologic Feature
* Borehole
* Fold
* Geologic Collection
* Geologic Event
* Geologic Unit
* Mapped Feature
* Mapped Interval
* Natural Geomorphologic Feature
* Shear Displacement Structure

* Campaign
* Geophysical Object Set
* Geophysical Profile
* Geophysical Station
* Geophysical Swath

* Active Well
* Aquiclude
* Aquifer
* Aquifer System
* Aquitard
* Groundwater Body
* Natural Hydrogeological Object

*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers only to instances of feature types of this application schema, not to any types specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-GE <a name="ref_TG_DS_GE"></a>   | [INSPIRE Data Specification on Geology – Technical Guidelines version 3.0](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_GE_v3.0.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-GE](#ref_TG_DS_GE)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Code lists](./code-list.md)  | ready for review  | A.5.1 |
| [Feature references](./features.md)  | ready for review  | A.1.4 |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gml            | http://www.opengis.net/gml/3.2
ge             | http://inspire.ec.europa.eu/schemas/ge-core/4.0

The following variables are used to refer to the corresponding Xpath expressions in all test descriptions:

Variable       | Value
-------------- | -------------------------------------------------
features <a name="features"></a>   |  //schema-element(ge-core:AnthropogenicGeomorphologicFeature) \| //schema-element(ge-core:Borehole) \| //schema-element(ge-core:Fold) \| //schema-element(ge-core:GeologicCollection) \| //schema-element(ge-core:GeologicEvent) \| //schema-element(ge-core:NaturalGeomorphologicFeature) \| //schema-element(ge-core:GeologicUnit) \| //schema-element(ge-core:MappedFeature) \| //schema-element(ge-core:MappedInterval)) \| //schema-element(ge-core:ShearDisplacementStructure) \| //schema-element(ge-core:Campaign)) \| //schema-element(ge-core:GeophObjectSet) \|  //schema-element(ge-core:GeophProfile) \| //schema-element(ge-core:GeophStation) \| //schema-element(ge-core:GeophSwath) \| //schema-element(ge-core:ActiveWell) \| //schema-element(ge-core:Aquifer) \| //schema-element(ge-core:AquiferSystem) \| //schema-element(ge-core:Aquitard) \| //schema-element(ge-core:GroundWaterBody) \| //schema-element(ge-core:HydrogeologicalObjectNatural) \| //schema-element(ge-core:Aquiclude)