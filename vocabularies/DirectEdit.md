# DirectEdit Vocabulary
**Namespace: [com.sap.vocabularies.DirectEdit.v1](DirectEdit.xml)**

Terms for Direct-Edit User Interfaces


## Terms

Term|Type|Description
:---|:---|:----------
[SideEffects](DirectEdit.xml#L38) *([Experimental](Common.md#Experimental))*|[SideEffectsType](#SideEffectsType)|<a name="SideEffects"></a>Determine side effects of client-side data modification

<a name="SideEffectsType"></a>
## [SideEffectsType](DirectEdit.xml#L43) *([Experimental](Common.md#Experimental))*


After a change to a property whose path is contained in `Triggers`, the client should pass the entity with the changed property to the `CalculationFunction` and receive the entity with all changes that happen as side effects of the given change.

Property|Type|Description
:-------|:---|:----------
[Triggers](DirectEdit.xml#L48)|\[String\]|List of paths to the properties whose changes should trigger the side effects calculation.
[CalculationFunction](DirectEdit.xml#L52)|[QualifiedName](Common.md#QualifiedName)|<p>The operation calculating the side effects. While non-changing for the service, this technically is an action bound to the entity set so that the parameters can be sent in the POST request body. The action has the following non-binding parameters:</p> <ul> <li><code>Qualifier</code> of type <a href="https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#SimpleIdentifier"><code>Core.SimpleIdentifier</code></a> or cast-compatible: the qualifier of the <code>SideEffects</code> annotation</li> <li><code>Trigger</code> of type <code>Edm.String</code>: the trigger of the side-effects determination, see <code>Triggers</code> property</li> <li><code>Data</code> of either the entity type of the annotated entity set or a complex type that is structure-compatible with it</li> </ul> <p>The <strong>return type</strong> of the action also needs to be either the entity type of the annotated entity set or structure-compatible with it, it can be the same type as for <code>Data</code>.</p> <p>Structure-compatible means:</p> <ul> <li>each primitive property that has the same name as a corresponding primitive property of the entity type of the annotated entity set is cast-compatible with the corresponding property and is nullable,</li> <li>each complex property that has the same name as a corresponding complex or navigation property of the entity type of the annotated entity set is structure-compatible with the corresponding property</li> <li>it may contain properties without a corresponding property in the entity type</li> <li>it may omit properties of the entity type</li> </ul> 
