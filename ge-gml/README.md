# Conformance class: GML application schemas, Geology

Conformance class for the GML encoding of spatial objects specified in the INSPIRE GML application schema 'Geology'. This conformance class examines the data set against requirements associated with the GML application schema.

This conformance class is part of the [INSPIRE Data Specification on Geology](../README.md).

## Standardization target type

INSPIRE spatial data set encoded in GML, Geology features

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the GML documents, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [INSPIRE GML application schemas](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/schemas) | n/a |

### Indirect dependencies

n/a
 
## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-GE <a name="ref_TG_DS_GE"></a>   | [INSPIRE Data Specification on Geology – Technical Guidelines version 3.0](https://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_GE_v3.0.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-sd](#ref_TG_DS_GE)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Basic test](./basic.md)  | ready for review  | A.1.1, (A.6.1)  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
ge      	   | http://inspire.ec.europa.eu/schemas/ge-core/4.0
ge_gp   	   | http://inspire.ec.europa.eu/schemas/ge_gp/4.0
ge_hg   	   | http://inspire.ec.europa.eu/schemas/ge_hg/4.0
