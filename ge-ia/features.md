# Feature references

**Purpose**: Verify that referenced features can be retrieved.

**Prerequisites**

**Test method**

* Verify that any feature reference in an association role is publicly accessible via HTTP, i.e. inspect all relevant properties. If a reference (@xlink:href) has a value that starts with "#", verify that an element with a `gml:id` attribute with the referenced identifier exists in the same document. If the reference starts with "http", verify that a HTTP GET request to the URI retrieves an XML document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following association roles:

* [Borehole.logElement](#logElement): MappedInterval
* [GeologicCollection.geophObjectSet](#geophObjectSet): GeophObjectSet
* [GeologicCollection.geophObjectMember](#geophObjectMember): GeophObject
* [GeologicCollection.boreholeMember](#boreholeMember): Borehole
* [GeologicCollection.mapMember](#mapMember): MappedFeature
* [GeologicUnit.geologicHistory](#geologicHistory): GeologicEvent
* [ShearDisplacementStructure.geologicHistory](#geologicHistory): GeologicEvent
* [Fold.geologicHistory](#geologicHistory): GeologicEvent
* [AnthropogenicGeomorphologicFeature.geologicHistory](#geologicHistory): GeologicEvent
* [NaturalGeomorphologicFeature.geologicHistory](#geologicHistory): GeologicEvent
* [MappedFeature.specification](#specification): GeologicUnit or ShearDisplacementStructure or Fold or AnthropogenicGeomorphologicFeature or NaturalGeomorphologicFeature
* [MappedInterval.specification](#specification): GeologicUnit or ShearDisplacementStructure or Fold or AnthropogenicGeomorphologicFeature or NaturalGeomorphologicFeature
* [ActiveWell.groundWaterBody](#groundWaterBody): GroundWaterBody
* [ActiveWell.environmentalMonitoringFacility](#environmentalMonitoringFacility): EnvironmentalMonitoringFacility
* [ActiveWell.borehole](#borehole): Borehole
* [Aquifer.aquitard](#aquitard): Aquitard
* [Aquifer.hydrogeologicalObject](#hydrogeologicalObject): HydrogeologicalObject
* [Aquifer.HydrogeologicalObject](#HydrogeologicalObject): AquiferSystem
* [AquiferSystem.aquitard](#aquitard2): Aquitard
* [AquiferSystem.aquiclude](#aquiclude): Aquiclude
* [AquiferSystem.aquifer](#aquifer): Aquifer
* [Aquitard.aquiferSystem](#aquiferSystem): AquiferSystem
* [Aquitard.aquifer](#aquifer2): Aquifer 
* [GroundWaterBody.activeWell](#activeWell): ActiveWell
* [GroundWaterBody.aquiferSystem](#aquiferSystem): AquiferSystem* [GroundWaterBody.hydrogeologicalObjectNatural](#hydrogeologicalObjectNatural): HydrogeologicalObjectNatural
* [GroundWaterBody.observationWell](#observationWell): EnvironmentalMonitoringFacility
* [ActiveWell.aquifer](#aquifer3): Aquifer
* [HydrogeologicalObjectNatural.aquifer](#aquifer4): Aquifer
* [HydrogeologicalObjectNatural.groundWaterBody](#groundWaterBody2): GroundWaterBody
* [Aquifer.geologicStructure](#geologicStructure): GeologicStructure
* [AquiferSystem.geologicStructure](#geologicStructure): GeologicStructure
* [Aquitard.geologicStructure](#geologicStructure): GeologicStructure
* [Aquiclude.geologicStructure](#geologicStructure): GeologicStructure


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                         |  XPath expression    | Multiplicity    | Voidable
------------------------------------ | ---------------------|-----------------|------------
logElement <a name="logElement"></a> | //schema-element(ge:Borehole)/ge:logElement/@xlink:href | 1..\* | Yes
geophObjectSet <a name="geophObjectSet"></a> | //schema-element(ge:GeologicCollection)/ge:geophObjectSet/@xlink:href | 1 | Yes
geophObjectMember <a name="geophObjectMember"></a> | //schema-element(ge:GeologicCollection)/ge:geophObjectMember/@xlink:href | 1 | Yes
boreholeMember <a name="boreholeMember"></a> | //schema-element(ge:GeologicCollection)/ge:boreholeMember/@xlink:href | 1..\* | Yes
mapMember <a name="mapMember"></a> | //schema-element(ge:GeologicCollection)/ge:mapMember/@xlink:href | 1..\* | Yes
geologicHistory <a name="geologicHistory"></a> | //schema-element(ge:GeologicUnit)/ge:geologicHistory/@xlink:href <br> //schema-element(ge:ShearDisplacementStructure)/ge:geologicHistory/@xlink:href <br> //schema-element(ge:Fold)/ge:geologicHistory/@xlink:href <br> //schema-element(ge:AnthropogenicGeomorphologicFeature)/ge:geologicHistory/@xlink:href <br>//schema-element(ge:NaturalGeomorphologicFeature)/ge:geologicHistory/@xlink:href <br> | 1..\* | Yes
specification <a name="specification"></a> | //schema-element(ge:MappedFeature)/ge:specification/@xlink:href <br> //schema-element(ge:MappedInterval)/ge:specification/@xlink:href | 1 | No
groundWaterBody <a name="groundWaterBody"></a> | //schema-element(ge_hg:ActiveWell)/ge_hg:groundWaterBody/@xlink:href | 0..\* | Yes
environmentalMonitoringFacilityelement <a name="element"></a> | //schema-element(ge_hg:ActiveWell)/ge_hg:environmentalMonitoringFacility/@xlink:href | 0..1 | Yes
borehole <a name="borehole"></a> | //schema-element(ge_hg:ActiveWell)/ge_hg:borehole/@xlink:href | 0..1 | Yes
aquitard <a name="aquitard"></a> | //schema-element(ge_hg:Aquifer)/ge_hg:aquitard/@xlink:href | 0..\* | Yes
hydrogeologicalObject <a name="hydrogeologicalObject"></a> | //schema-element(ge_hg:Aquifer)/ge_hg:hydrogeologicalObject/@xlink:href | 0..\* | Yes
aquiferSystem <a name="aquiferSystem"></a> | //schema-element(ge_hg:Aquifer)/ge_hg:aquiferSystem/@xlink:href | 0..1 | Yes
aquitard <a name="aquitard2"></a> | //schema-element(ge_hg:AquiferSystem)/ge_hg:aquitard/@xlink:href | 0..\* | Yes
aquiclude <a name="aquiclude"></a> | //schema-element(ge_hg:AquiferSystem)/ge_hg:aquiclude/@xlink:href | 0..\* | Yes
aquifer <a name="aquifer"></a> | //schema-element(ge_hg:AquiferSystem)/ge_hg:aquifer/@xlink:href | 0..\* | Yes
aquiferSystem <a name="aquiferSystem"></a> | //schema-element(ge_hg:Aquitard)/ge_hg:aquiferSystem/@xlink:href | 0..1 | Yes
aquifer <a name="aquifer2"></a> | //schema-element(ge_hg:Aquitard)/ge_hg:aquifer/@xlink:href | 0..\* | Yes
activeWell <a name="activeWell"></a> | //schema-element(ge_hg:GroundWaterBody)/ge_hg:activeWell/@xlink:href | 0..\* | Yes
aquiferSystem <a name="aquiferSystem"></a> | //schema-element(ge_hg:GroundWaterBody)/ge_hg:aquiferSystem/@xlink:href | 0..1 | Yes
hydrogeologicalObjectNatural <a name="hydrogeologicalObjectNatural"></a> | //schema-element(ge_hg:GroundWaterBody)/ge_hg:hydrogeologicalObjectNatural/@xlink:href | 0..\* | Yes
observationWell <a name="observationWell"></a> | //schema-element(ge_hg:GroundWaterBody)/ge_hg:observationWell/@xlink:href | 0..\* | Yes
aquifer <a name="aquifer3"></a> | //schema-element(ge_hg:ActiveWell)/ge_hg:aquifer/@xlink:href | 0..1 | Yes
aquifer <a name="aquifer4"></a> | //schema-element(ge_hg:HydrogeologicalObjectNatural)/ge_hg:aquifer/@xlink:href | 0..1 | Yes
groundWaterBody <a name="groundWaterBody2"></a> | //schema-element(ge_hg:HydrogeologicalObjectNatural)/ge_hg:groundWaterBody/@xlink:href | 0..1 | Yes
geologicStructure <a name="geologicStructure"></a> | //schema-element(ge_hg:Aquifer)/ge_hg:geologicStructure/@xlink:href <br> //schema-element(ge_hg:AquiferSystem)/ge_hg:geologicStructure/@xlink:href <br> //schema-element(ge_hg:Aquitard)/ge_hg:geologicStructure/@xlink:href <br> //schema-element(ge_hg:Aquiclude)/ge_hg:geologicStructure/@xlink:href | 0..\* | Yes
