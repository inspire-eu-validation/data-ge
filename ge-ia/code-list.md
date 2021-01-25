# Code lists

**Purpose**: Verify that code lists extensions can be accessed.

**Prerequisites**

**Test method**

* Verify that any code list extensions are publicly accessible via HTTP, i.e. inspect extensible code list values property elements. If a reference (@xlink:href) has a value that does not start with http://inspire.ec.europa.eu/codelist/, verify that a HTTP GET request to the URI retrieves a document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following empty code lists:

* [ThematicClassValue](#ThematicClassValue) for the [themeClass](#themeClass) element: http://inspire.ec.europa.eu/codelist/ThematicClassValue
* [ThematicClassificationValue](#ThematicClassificationValue) for the [themeClassification](#themeClassification) element: http://inspire.ec.europa.eu/codelist/ThematicClassificationValue


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression      |Multiplicity   |Voidable
---------------------------------------------------------- | -----------------------|---------------|---------------------------------
themeClass <a name="themeClass"></a> | //schema-element(ge:GeologicUnit)/ge:themeClass/ge:ThematicClass/ge:themeClass/@xlink:href <br> //schema-element(ge:ShearDisplacementStructure)/ge:themeClass/ge:ThematicClass/ge:themeClass/@xlink:href <br> //schema-element(ge:Fold)/ge:themeClass/ge:ThematicClass/ge:themeClass/@xlink:href <br> //schema-element(ge:AnthropogenicGeomorphologicFeature)/ge:themeClass/ge:ThematicClass/ge:themeClass/@xlink:href <br>//schema-element(ge:NaturalGeomorphologicFeature)/ge:themeClass/ge:ThematicClass/ge:themeClass/@xlink:href <br> | 1 (0..\* for the parent) | No
themeClassification <a name="themeClassification"></a> | //schema-element(ge:GeologicUnit)/ge:themeClass/ge:ThematicClass/ge:themeClassification/@xlink:href <br> //schema-element(ge:ShearDisplacementStructure)/ge:themeClass/ge:ThematicClass/ge:themeClassification/@xlink:href <br> //schema-element(ge:Fold)/ge:themeClass/ge:ThematicClass/ge:themeClassification/@xlink:href <br> //schema-element(ge:AnthropogenicGeomorphologicFeature)/ge:themeClass/ge:ThematicClass/ge:themeClassification/@xlink:href <br>//schema-element(ge:NaturalGeomorphologicFeature)/ge:themeClass/ge:ThematicClass/ge:themeClassification/@xlink:href <br> | 1 (0..\* for the parent) | No
