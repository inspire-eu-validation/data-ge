# Constraints

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

The following checks are performed for every feature in the dataset.

* Check that the [shape](#shapeCampaign) attribute of the spatial object type Campaign is of type GM_Surface (OCL: "inv: shape.oclIsKindOf(GM_Surface)" ).
* Check that the [projectedGeometry](#projectedGeometry1) attribute of the spatial object types GeophStation, GeophProfile and GeophSwath is of type GM_Point, GM_Curve or GM_Surface (OCL: "inv: projectedGeometry.oclIsKindOf(GM_Point) or projectedGeometry.oclIsKindOf(GM_Curve) or projectedGeometry.oclIsKindOf(GM_Surface) " ).
* Check that the [projectedGeometry](#projectedGeometry2) attribute of the spatial object type GeophObjectSet is of type GM_Point, GM_Curve or GM_Surface (OCL: "inv: projectedGeometry.oclIsKindOf(GM_Point) or projectedGeometry.oclIsKindOf(GM_Curve) or projectedGeometry.oclIsKindOf(GM_Surface) " ).
* Check that the [shape](#shapeGeophProfile) attribute of the spatial object type GeophProfile is of type GM_Curve (OCL: "inv: shape.oclIsKindOf(GM_Curve)" ).
* Check that the [shape](#shapeGeophStation) attribute of the spatial object type GeophStation is of type GM_Point (OCL: "inv: shape.oclIsKindOf(GM_Point)" ).
* Check that the [shape](#shapeGeophSwath) attribute of the spatial object type GeophSwath is of type GM_Surface (OCL: "inv: shape.oclIsKindOf(GM_Surface)" ).


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-GE](./README.md#ref_TG_DS_GE) 5.3.2.1.1.

**Test type**: Automated

**Notes** 

Verify that the OCL constraints that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
shape <a name="shapeCampaign"></a> | //schema-element(ge_gp:Campaign)/sams:shape/gml:Surface | 1 | Yes
projectedGeometry <a name="projectedGeometry1"></a> | //schema-element(ge_gp:GeophStation)/ge_gp:projectedGeometry/(gml:Point or gml:Curve or gml:Surface) <br> //schema-element(ge_gp:GeophProfile)/ge_gp:projectedGeometry/(gml:Point or gml:Curve or gml:Surface) <br> //schema-element(ge_gp:GeophSwath)/ge_gp:projectedGeometry/(gml:Point or gml:Curve or gml:Surface) | 1..\* | No
projectedGeometry <a name="projectedGeometry2"></a> | //schema-element(ge_gp:GeophObjectSet)/ge_gp:projectedGeometry/(gml:Point or gml:Curve or gml:Surface) | 1..\* | No
shape <a name="shapeGeophProfile"></a> | //schema-element(ge_gp:GeophProfile)/sams:shape/gml:Curve | 1 | Yes
shape <a name="shapeGeophStation"></a> | //schema-element(ge_gp:GeophStation)/sams:shape/gml:Point | 1 | Yes
shape <a name="shapeGeophSwath"></a> | //schema-element(ge_gp:GeophSwath)/sams:shape/gml:Surface | 1 | Yes