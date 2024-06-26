# DataIntegration Vocabulary
**Namespace: [com.sap.vocabularies.DataIntegration.v1](DataIntegration.xml)**

Terms for Data Integration


## Terms

Term|Type|Description
:---|:---|:----------
[Extractable](DataIntegration.xml#L32)|Boolean|<a name="Extractable"></a>Defines if entity set is extractable
[OriginalDataType](DataIntegration.xml#L36)|String|<a name="OriginalDataType"></a>Original data type of the annotated property in its source system ([Example](DataIntegration.xml#L39))<br>The provider of an OData service maps its local type definitions to Edm types. Sometimes, specific type information is lost. This additional annotation gives the consumer hints about the type original type definition.
[OriginalName](DataIntegration.xml#L46)|String|<a name="OriginalName"></a>Original name of the annotated model element in its source model ([Example](DataIntegration.xml#L49))<br>The provider of an OData service maps its local names to Edm identifiers, which may require removing or replacing characters that are not allowed.
[ConversionExit](DataIntegration.xml#L56)|String|<a name="ConversionExit"></a>Identifier that describes the special output conversion of the annotated property in the source system ([Example](DataIntegration.xml#L59))<br>The provider of an OData service maps its local type definitions to Edm types. Sometimes, specific type information is lost. This additional annotation gives the consumer hints about the type original type definition.
[SourceSystem](DataIntegration.xml#L66)|String|<a name="SourceSystem"></a>Identifier that classifies the type of the source system<br>The original type name used in annotation OriginalDataType depend are specific to different source system. Sourc system type ABAP uses other type names as source system type HANA.
[DeltaMethod](DataIntegration.xml#L83)|[DeltaMethodType](#DeltaMethodType)|<a name="DeltaMethod"></a>Defines which delta method the entity set supports. Only evaluated if Capabilities.ChangeTracking/Supported is true

<a name="DeltaMethodType"></a>
## [DeltaMethodType](DataIntegration.xml#L71)


Flag Member|Value|Description
:-----|----:|:----------
[INSERT](DataIntegration.xml#L72)|1|Delta is supported for inserts
[UPDATE](DataIntegration.xml#L75)|2|Delta is supported for updates
[DELETE](DataIntegration.xml#L78)|4|Delta is supported for deletes
