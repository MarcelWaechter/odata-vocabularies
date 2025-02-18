# UI Vocabulary
**Namespace: [com.sap.vocabularies.UI.v1](UI.xml)**

Terms for presenting data in user interfaces

The SAP UI Vocabulary aims to optimize usage of data in UI channels.
It focuses on usage patterns of data in UIs, not on UI patterns, and it is completely independent of the
UI technologies or devices used to visualize the data.

These usage patterns represent certain semantic views on business data, some of them very general,
others centering around the concept of a Thing, i.e. something tangible to end users.
Examples for Things are semantic object instances or business object instances.
One example for a usage pattern is the collection of properties which helps the user to identify a Thing,
the [UI.Identification](#Identification) term.
Another example is the [UI.LineItem](#LineItem) term, which is a set of properties suitable for visualizing
a collection of business object instances, e.g. as a list or table.


## Terms

Term|Type|Description
:---|:---|:----------
[HeaderInfo](./UI.xml#L64:~:text=<Term%20Name="-,HeaderInfo,-")|[HeaderInfoType](#HeaderInfoType)|<a name="HeaderInfo"></a>Information for the header area of an entity representation. HeaderInfo is mandatory for main entity types of the model
[Identification](./UI.xml#L115:~:text=<Term%20Name="-,Identification,-")|\[[DataFieldAbstract](#DataFieldAbstract)\]|<a name="Identification"></a>Collection of fields identifying the object
[Badge](./UI.xml#L120:~:text=<Term%20Name="-,Badge,-")|[BadgeType](#BadgeType)|<a name="Badge"></a>Information usually displayed in the form of a business card
[LineItem](./UI.xml#L147:~:text=<Term%20Name="-,LineItem,-")|\[[DataFieldAbstract](#DataFieldAbstract)\]|<a name="LineItem"></a>Collection of data fields for representation in a table or list
[StatusInfo](./UI.xml#L152:~:text=<Term%20Name="-,StatusInfo,-")|\[[DataFieldAbstract](#DataFieldAbstract)\]|<a name="StatusInfo"></a>Collection of data fields describing the status of an entity
[FieldGroup](./UI.xml#L157:~:text=<Term%20Name="-,FieldGroup,-")|[FieldGroupType](#FieldGroupType)|<a name="FieldGroup"></a>Group of fields with an optional label
[ConnectedFields](./UI.xml#L171:~:text=<Term%20Name="-,ConnectedFields,-")|[ConnectedFieldsType](#ConnectedFieldsType)|<a name="ConnectedFields"></a>Group of semantically connected fields with a representation template and an optional label ([Example](./UI.xml#L173))
[GeoLocations](./UI.xml#L236:~:text=<Term%20Name="-,GeoLocations,-")|\[[GeoLocationType](#GeoLocationType)\]|<a name="GeoLocations"></a>Collection of geographic locations
[GeoLocation](./UI.xml#L240:~:text=<Term%20Name="-,GeoLocation,-")|[GeoLocationType](#GeoLocationType)|<a name="GeoLocation"></a>Geographic location
[Contacts](./UI.xml#L260:~:text=<Term%20Name="-,Contacts,-")|\[AnnotationPath\]|<a name="Contacts"></a>Collection of contacts<br>Each collection item MUST reference an annotation of a Communication.Contact<br>Allowed terms:<br>- [Contact](Communication.md#Contact)
[MediaResource](./UI.xml#L271:~:text=<Term%20Name="-,MediaResource,-")|[MediaResourceType](#MediaResourceType)|<a name="MediaResource"></a>Properties that describe a media resource<br>Either `Url` or `Stream` MUST be present, and never both.
[DataPoint](./UI.xml#L351:~:text=<Term%20Name="-,DataPoint,-")|[DataPointType](#DataPointType)|<a name="DataPoint"></a>Visualization of a single point of data, typically a number; may also be textual, e.g. a status value
[KPI](./UI.xml#L659:~:text=<Term%20Name="-,KPI,-")|[KPIType](#KPIType)|<a name="KPI"></a>A Key Performance Indicator (KPI) bundles a SelectionVariant and a DataPoint, and provides details for progressive disclosure
[Chart](./UI.xml#L705:~:text=<Term%20Name="-,Chart,-")|[ChartDefinitionType](#ChartDefinitionType)|<a name="Chart"></a>Visualization of multiple data points
[ValueCriticality](./UI.xml#L929:~:text=<Term%20Name="-,ValueCriticality,-") *([Experimental](Common.md#Experimental))*|\[[ValueCriticalityType](#ValueCriticalityType)\]|<a name="ValueCriticality"></a>Assign criticalities to primitive values. This information can be used for semantic coloring.
[CriticalityLabels](./UI.xml#L942:~:text=<Term%20Name="-,CriticalityLabels,-") *([Experimental](Common.md#Experimental))*|\[[CriticalityLabelType](#CriticalityLabelType)\]|<a name="CriticalityLabels"></a>Assign labels to criticalities. This information can be used for semantic coloring. When applied to a property, a label for a criticality must be provided, if more than one value of the annotated property has been assigned to the same criticality. There must be no more than one label per criticality.
[SelectionFields](./UI.xml#L963:~:text=<Term%20Name="-,SelectionFields,-")|\[PropertyPath\]|<a name="SelectionFields"></a>Properties that might be relevant for filtering a collection of entities of this type
[Facets](./UI.xml#L971:~:text=<Term%20Name="-,Facets,-")|\[[Facet](#Facet)\]|<a name="Facets"></a>Collection of facets
[HeaderFacets](./UI.xml#L975:~:text=<Term%20Name="-,HeaderFacets,-")|\[[Facet](#Facet)\]|<a name="HeaderFacets"></a>Facets for additional object header information
[QuickViewFacets](./UI.xml#L979:~:text=<Term%20Name="-,QuickViewFacets,-")|\[[Facet](#Facet)\]|<a name="QuickViewFacets"></a>Facets that may be used for a quick overview of the object
[QuickCreateFacets](./UI.xml#L983:~:text=<Term%20Name="-,QuickCreateFacets,-")|\[[Facet](#Facet)\]|<a name="QuickCreateFacets"></a>Facets that may be used for a (quick) create of the object
[FilterFacets](./UI.xml#L987:~:text=<Term%20Name="-,FilterFacets,-")|\[[ReferenceFacet](#ReferenceFacet)\]|<a name="FilterFacets"></a>Facets that reference UI.FieldGroup annotations to group filterable fields
[SelectionPresentationVariant](./UI.xml#L1060:~:text=<Term%20Name="-,SelectionPresentationVariant,-")|[SelectionPresentationVariantType](#SelectionPresentationVariantType)|<a name="SelectionPresentationVariant"></a>A SelectionPresentationVariant bundles a Selection Variant and a Presentation Variant
[PresentationVariant](./UI.xml#L1084:~:text=<Term%20Name="-,PresentationVariant,-")|[PresentationVariantType](#PresentationVariantType)|<a name="PresentationVariant"></a>Defines how the result of a queried collection of entities is shaped and how this result is displayed
[SelectionVariant](./UI.xml#L1197:~:text=<Term%20Name="-,SelectionVariant,-")|[SelectionVariantType](#SelectionVariantType)|<a name="SelectionVariant"></a>A SelectionVariant denotes a combination of parameters and filters to query the annotated entity set
[ThingPerspective](./UI.xml#L1353:~:text=<Term%20Name="-,ThingPerspective,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="ThingPerspective"></a>The annotated term is a Thing Perspective
[IsSummary](./UI.xml#L1356:~:text=<Term%20Name="-,IsSummary,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="IsSummary"></a>This Facet and all included Facets are the summary of the thing. At most one Facet of a thing can be tagged with this term
[PartOfPreview](./UI.xml#L1360:~:text=<Term%20Name="-,PartOfPreview,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="PartOfPreview"></a>This record and all included structural elements are part of the Thing preview<br>This term can be applied e.g. to UI.Facet and UI.DataField
[Map](./UI.xml#L1364:~:text=<Term%20Name="-,Map,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="Map"></a>Target MUST reference a UI.GeoLocation, Communication.Address or a collection of these
[Gallery](./UI.xml#L1368:~:text=<Term%20Name="-,Gallery,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="Gallery"></a>Target MUST reference a UI.MediaResource
[IsImageURL](./UI.xml#L1373:~:text=<Term%20Name="-,IsImageURL,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="IsImageURL"></a>Properties and terms annotated with this term MUST contain a valid URL referencing an resource with a MIME type image<br>Can be annotated with:<br>- [IsNaturalPerson](Common.md#IsNaturalPerson)
[IsImage](./UI.xml#L1383:~:text=<Term%20Name="-,IsImage,-") *([Experimental](Common.md#Experimental))*|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="IsImage"></a>Properties annotated with this term MUST be a stream property annotated with a MIME type image. Entity types annotated with this term MUST be a media entity type annotated with a MIME type image.<br>Can be annotated with:<br>- [IsNaturalPerson](Common.md#IsNaturalPerson)
[MultiLineText](./UI.xml#L1394:~:text=<Term%20Name="-,MultiLineText,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="MultiLineText"></a>Properties and parameters annotated with this annotation should be rendered as multi-line text (e.g. text area)
[Placeholder](./UI.xml#L1399:~:text=<Term%20Name="-,Placeholder,-")|String|<a name="Placeholder"></a>A short, human-readable text that gives a hint or an example to help the user with data entry
[TextArrangement](./UI.xml#L1404:~:text=<Term%20Name="-,TextArrangement,-")|[TextArrangementType](#TextArrangementType)|<a name="TextArrangement"></a>Describes the arrangement of a code or ID value and its text<br>This term annotates one of the following:<br> (1) a [`Common.Text`](Common.md#Text) annotation of the code or ID property where the annotation value is the text<br> (2) an entity type, this has the same effect as annotating all `Common.Text` annotations of properties of that entity type.
[Note](./UI.xml#L1427:~:text=<Term%20Name="-,Note,-") *([Experimental](Common.md#Experimental))*|[NoteType](#NoteType)|<a name="Note"></a>Visualization of a note attached to an entity<br>Administrative data is given by the annotations [`Common.CreatedBy`](Common.md#CreatedBy), [`Common.CreatedAt`](Common.md#CreatedAt), [`Common.ChangedBy`](Common.md#ChangedBy), [`Common.ChangedAt`](Common.md#ChangedAt) on the same entity type.
[Importance](./UI.xml#L1480:~:text=<Term%20Name="-,Importance,-")|[ImportanceType](#ImportanceType)|<a name="Importance"></a>Expresses the importance of e.g. a DataField or an annotation
[Hidden](./UI.xml#L1495:~:text=<Term%20Name="-,Hidden,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="Hidden"></a>Properties or facets (see UI.Facet) annotated with this term will not be rendered if the annotation evaluates to true.<br>Hidden properties usually carry technical information that is used for application control and is of no direct interest to end users. The annotation value may be an expression to dynamically hide or render the annotated feature. If a navigation property is annotated with `Hidden` true, all subsequent parts are hidden - independent of their own potential `Hidden` annotations.
[IsCopyAction](./UI.xml#L1503:~:text=<Term%20Name="-,IsCopyAction,-") *([Experimental](Common.md#Experimental))*|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="IsCopyAction"></a>The annotated [`DataFieldForAction`](#DataFieldForAction) record references an action that deep-copies an instance of the annotated entity type<br>The referenced action MUST be bound to the annotated entity type and MUST create a new instance of the same entity type as a deep copy of the bound instance. Upon successful completion, the response MUST contain a `Location` header that contains the edit URL or read URL of the created entity, and the response MUST be either `201 Created` and a representation of the created entity, or `204 No Content` if the request included a `Prefer` header with a value of `return=minimal` and did not include the system query options `$select` and `$expand`.
[CreateHidden](./UI.xml#L1515:~:text=<Term%20Name="-,CreateHidden,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="CreateHidden"></a>EntitySets annotated with this term can control the visibility of the Create operation dynamically<br>The annotation value should be a path to another property from a related entity.
[UpdateHidden](./UI.xml#L1520:~:text=<Term%20Name="-,UpdateHidden,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="UpdateHidden"></a>EntitySets annotated with this term can control the visibility of the Edit/Save operation dynamically<br>The annotation value should be a path to another property from the same or a related entity.
[DeleteHidden](./UI.xml#L1525:~:text=<Term%20Name="-,DeleteHidden,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="DeleteHidden"></a>EntitySets annotated with this term can control the visibility of the Delete operation dynamically<br>The annotation value should be a path to another property from the same or a related entity.
[HiddenFilter](./UI.xml#L1530:~:text=<Term%20Name="-,HiddenFilter,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="HiddenFilter"></a>Properties annotated with this term will not be rendered as filter criteria if the annotation evaluates to true.<br>Properties annotated with `HiddenFilter` are intended as parts of a `$filter` expression that cannot be directly influenced by end users. The properties will be rendered in all other places, e.g. table columns or form fields. This is in contrast to properties annotated with [Hidden](#Hidden) that are not rendered at all. If a navigation property is annotated with `HiddenFilter` true, all subsequent parts are hidden in filter - independent of their own potential `HiddenFilter` annotations.
[AdaptationHidden](./UI.xml#L1539:~:text=<Term%20Name="-,AdaptationHidden,-") *([Experimental](Common.md#Experimental))*|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="AdaptationHidden"></a>Properties or entities annotated with this term can't be used for UI adaptation/configuration/personalization<br>The tagged elements can only be used in UI based on metadata, annnotations or code.
[DataFieldDefault](./UI.xml#L1545:~:text=<Term%20Name="-,DataFieldDefault,-")|[DataFieldAbstract](#DataFieldAbstract)|<a name="DataFieldDefault"></a>Default representation of a property as a datafield, e.g. when the property is added as a table column or form field via personalization<br>Only concrete subtypes of [DataFieldAbstract](#DataFieldAbstract) can be used for a DataFieldDefault. For type [DataField](#DataField) and its subtypes the annotation target SHOULD be the same property that is referenced via a path expression in the `Value` of the datafield.
[Criticality](./UI.xml#L1769:~:text=<Term%20Name="-,Criticality,-")|[CriticalityType](#CriticalityType)|<a name="Criticality"></a>Service-calculated criticality, alternative to UI.CriticalityCalculation
[CriticalityCalculation](./UI.xml#L1773:~:text=<Term%20Name="-,CriticalityCalculation,-")|[CriticalityCalculationType](#CriticalityCalculationType)|<a name="CriticalityCalculation"></a>Parameters for client-calculated criticality, alternative to UI.Criticality
[Emphasized](./UI.xml#L1777:~:text=<Term%20Name="-,Emphasized,-") *([Experimental](Common.md#Experimental))*|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="Emphasized"></a>Highlight something that is of special interest<br>The usage of a property or operation should be highlighted as it's of special interest for the end user
[OrderBy](./UI.xml#L1783:~:text=<Term%20Name="-,OrderBy,-") *([Experimental](Common.md#Experimental))*|PropertyPath|<a name="OrderBy"></a>Sort by the referenced property instead of by the annotated property<br>Example: annotated property `SizeCode` has string values XS, S, M, L, XL, referenced property SizeOrder has numeric values -2, -1, 0, 1, 2. Numeric ordering by SizeOrder will be more understandable than lexicographic ordering by SizeCode.
[ParameterDefaultValue](./UI.xml#L1789:~:text=<Term%20Name="-,ParameterDefaultValue,-")|PrimitiveType?|<a name="ParameterDefaultValue"></a>Define default values for action parameters<br>For unbound actions the default value can either be a constant expression, or a dynamic expression using absolute paths, e.g. singletons or function import results. Whereas for bound actions the bound entity and its properties and associated properties can be used as default values
[RecommendationState](./UI.xml#L1795:~:text=<Term%20Name="-,RecommendationState,-")|[RecommendationStateType](#RecommendationStateType)|<a name="RecommendationState"></a>Indicates whether a field contains or has a recommended value<br>Intelligent systems can help users by recommending input the user may "prefer".
[RecommendationList](./UI.xml#L1825:~:text=<Term%20Name="-,RecommendationList,-")|[RecommendationListType](#RecommendationListType)|<a name="RecommendationList"></a>Specifies how to get a list of recommended values for a property or parameter<br>Intelligent systems can help users by recommending input the user may "prefer".
[ExcludeFromNavigationContext](./UI.xml#L1857:~:text=<Term%20Name="-,ExcludeFromNavigationContext,-")|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="ExcludeFromNavigationContext"></a>The contents of this property must not be propagated to the app-to-app navigation context
[DoNotCheckScaleOfMeasuredQuantity](./UI.xml#L1861:~:text=<Term%20Name="-,DoNotCheckScaleOfMeasuredQuantity,-") *([Experimental](Common.md#Experimental))*|Boolean|<a name="DoNotCheckScaleOfMeasuredQuantity"></a>Do not check the number of fractional digits of the annotated measured quantity<br>The annotated property contains a measured quantity, and the user may enter more fractional digits than defined for the corresponding unit of measure.<br/>This switches off the validation of user input with respect to decimals.
[LeadingEntitySet](./UI.xml#L1871:~:text=<Term%20Name="-,LeadingEntitySet,-") *([Experimental](Common.md#Experimental))*|String|<a name="LeadingEntitySet"></a>The referenced entity set is the preferred starting point for UIs using this service

<a name="HeaderInfoType"></a>
## [HeaderInfoType](./UI.xml#L68:~:text=<ComplexType%20Name="-,HeaderInfoType,-")


Property|Type|Description
:-------|:---|:----------
[TypeName](./UI.xml#L69:~:text=<ComplexType%20Name="-,HeaderInfoType,-")|String|Name of the main entity type
[TypeNamePlural](./UI.xml#L73:~:text=<ComplexType%20Name="-,HeaderInfoType,-")|String|Plural form of the name of the main entity type
[Title](./UI.xml#L77:~:text=<ComplexType%20Name="-,HeaderInfoType,-")|[DataFieldAbstract?](#DataFieldAbstract)|Title, e.g. for overview pages<br>This can be a [DataField](#DataField) and any of its children, or a [DataFieldForAnnotation](#DataFieldForAnnotation) targeting [ConnectedFields](#ConnectedFields).
[Description](./UI.xml#L87:~:text=<ComplexType%20Name="-,HeaderInfoType,-")|[DataFieldAbstract?](#DataFieldAbstract)|Description, e.g. for overview pages<br>This can be a [DataField](#DataField) and any of its children, or a [DataFieldForAnnotation](#DataFieldForAnnotation) targeting [ConnectedFields](#ConnectedFields).
[Image](./UI.xml#L97:~:text=<ComplexType%20Name="-,HeaderInfoType,-") *([Experimental](Common.md#Experimental))*|Stream?|Image for an instance of the entity type. If the property has a valid value, it can be used for the visualization of the instance. If it is not available or not valid the value of the property `ImageUrl` can be used instead.
[ImageUrl](./UI.xml#L101:~:text=<ComplexType%20Name="-,HeaderInfoType,-")|URL?|Image URL for an instance of the entity type. If the property has a valid value, it can be used for the visualization of the instance. If it is not available or not valid the value of the property `TypeImageUrl` can be used instead.
[TypeImageUrl](./UI.xml#L105:~:text=<ComplexType%20Name="-,HeaderInfoType,-")|URL?|Image URL for the entity type
[Initials](./UI.xml#L109:~:text=<ComplexType%20Name="-,HeaderInfoType,-") *([Experimental](Common.md#Experimental))*|String?|Latin letters to be used in case no `Image`, `ImageUrl`, or `TypeImageUrl` is present

<a name="BadgeType"></a>
## [BadgeType](./UI.xml#L124:~:text=<ComplexType%20Name="-,BadgeType,-")


Property|Type|Description
:-------|:---|:----------
[HeadLine](./UI.xml#L125:~:text=<ComplexType%20Name="-,BadgeType,-")|[DataField](#DataField)|Headline
[Title](./UI.xml#L128:~:text=<ComplexType%20Name="-,BadgeType,-")|[DataField](#DataField)|Title
[ImageUrl](./UI.xml#L131:~:text=<ComplexType%20Name="-,BadgeType,-")|URL?|Image URL for an instance of the entity type. If the property has a valid value, it can be used for the visualization of the instance. If it is not available or not valid the value of the property `TypeImageUrl` can be used instead.
[TypeImageUrl](./UI.xml#L135:~:text=<ComplexType%20Name="-,BadgeType,-")|URL?|Image URL for the entity type
[MainInfo](./UI.xml#L139:~:text=<ComplexType%20Name="-,BadgeType,-")|[DataField?](#DataField)|Main information on the business card
[SecondaryInfo](./UI.xml#L142:~:text=<ComplexType%20Name="-,BadgeType,-")|[DataField?](#DataField)|Additional information on the business card

<a name="FieldGroupType"></a>
## [FieldGroupType](./UI.xml#L161:~:text=<ComplexType%20Name="-,FieldGroupType,-")


Property|Type|Description
:-------|:---|:----------
[Label](./UI.xml#L162:~:text=<ComplexType%20Name="-,FieldGroupType,-")|String?|Label for the field group
[Data](./UI.xml#L166:~:text=<ComplexType%20Name="-,FieldGroupType,-")|\[[DataFieldAbstract](#DataFieldAbstract)\]|Collection of data fields

<a name="ConnectedFieldsType"></a>
## [ConnectedFieldsType](./UI.xml#L198:~:text=<ComplexType%20Name="-,ConnectedFieldsType,-")
Group of semantically connected fields with a representation template and an optional label

Property|Type|Description
:-------|:---|:----------
[Label](./UI.xml#L200:~:text=<ComplexType%20Name="-,ConnectedFieldsType,-")|String?|Label for the connected fields
[Template](./UI.xml#L204:~:text=<ComplexType%20Name="-,ConnectedFieldsType,-")|String|Template for representing the connected fields<br>Template variables are identifiers enclosed in curly braces, e.g. `{MaterialName} - {MaterialClassName}`. The `Data` collection assigns values to the template variables.
[Data](./UI.xml#L209:~:text=<ComplexType%20Name="-,ConnectedFieldsType,-")|[Dictionary](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#Dictionary)|Dictionary of template variables<br>Each template variable used in `Template` must be assigned a value here. The value must be of type [DataFieldAbstract](#DataFieldAbstract)

<a name="GeoLocationType"></a>
## [GeoLocationType](./UI.xml#L244:~:text=<ComplexType%20Name="-,GeoLocationType,-")
Properties that define a geographic location

Property|Type|Description
:-------|:---|:----------
[Latitude](./UI.xml#L246:~:text=<ComplexType%20Name="-,GeoLocationType,-")|Double?|Geographic latitude
[Longitude](./UI.xml#L249:~:text=<ComplexType%20Name="-,GeoLocationType,-")|Double?|Geographic longitude
[Location](./UI.xml#L252:~:text=<ComplexType%20Name="-,GeoLocationType,-")|GeographyPoint?|A point in a round-earth coordinate system
[Address](./UI.xml#L255:~:text=<ComplexType%20Name="-,GeoLocationType,-")|[AddressType?](Communication.md#AddressType)|vCard-style address

<a name="MediaResourceType"></a>
## [MediaResourceType](./UI.xml#L276:~:text=<ComplexType%20Name="-,MediaResourceType,-")


Property|Type|Description
:-------|:---|:----------
[Url](./UI.xml#L277:~:text=<ComplexType%20Name="-,MediaResourceType,-")|URL?|URL of media resource<br>Can be annotated with:<br>- [LinkTarget](HTML5.md#LinkTarget)
[Stream](./UI.xml#L286:~:text=<ComplexType%20Name="-,MediaResourceType,-") *([Experimental](Common.md#Experimental))*|Stream?|Stream of media resource<br>Can be annotated with:<br>- [LinkTarget](HTML5.md#LinkTarget)
[ContentType](./UI.xml#L295:~:text=<ComplexType%20Name="-,MediaResourceType,-")|MediaType?|Content type, such as application/pdf, video/x-flv, image/jpeg
[ByteSize](./UI.xml#L299:~:text=<ComplexType%20Name="-,MediaResourceType,-")|Int64?|Resource size in bytes
[ChangedAt](./UI.xml#L302:~:text=<ComplexType%20Name="-,MediaResourceType,-")|DateTimeOffset?|Date of last change
[Thumbnail](./UI.xml#L305:~:text=<ComplexType%20Name="-,MediaResourceType,-")|[ImageType?](#ImageType)|Thumbnail image
[Title](./UI.xml#L308:~:text=<ComplexType%20Name="-,MediaResourceType,-")|[DataField](#DataField)|Resource title
[Description](./UI.xml#L311:~:text=<ComplexType%20Name="-,MediaResourceType,-")|[DataField?](#DataField)|Resource description

<a name="ImageType"></a>
## [ImageType](./UI.xml#L315:~:text=<ComplexType%20Name="-,ImageType,-")
Properties that describe an image

Either `Url` or `Stream` MUST be present, and never both.

Property|Type|Description
:-------|:---|:----------
[Url](./UI.xml#L318:~:text=<ComplexType%20Name="-,ImageType,-")|URL|URL of image
[Stream](./UI.xml#L322:~:text=<ComplexType%20Name="-,ImageType,-") *([Experimental](Common.md#Experimental))*|Stream?|Stream of image<br>Can be annotated with:<br>- [LinkTarget](HTML5.md#LinkTarget)
[Width](./UI.xml#L331:~:text=<ComplexType%20Name="-,ImageType,-")|String?|Width of image
[Height](./UI.xml#L334:~:text=<ComplexType%20Name="-,ImageType,-")|String?|Height of image

<a name="DataPointType"></a>
## [DataPointType](./UI.xml#L355:~:text=<ComplexType%20Name="-,DataPointType,-")


Property|Type|Description
:-------|:---|:----------
[Title](./UI.xml#L356:~:text=<ComplexType%20Name="-,DataPointType,-")|String?|Title of the data point
[Description](./UI.xml#L360:~:text=<ComplexType%20Name="-,DataPointType,-")|String?|Short description
[LongDescription](./UI.xml#L364:~:text=<ComplexType%20Name="-,DataPointType,-")|String?|Full description
[Value](./UI.xml#L368:~:text=<ComplexType%20Name="-,DataPointType,-")|PrimitiveType|Numeric value<br>The value is typically provided via a `Path` construct. The path MUST lead to a direct property of the same entity type or a property of a complex property (recursively) of that entity type, navigation segments are not allowed.<br/>It could be annotated with either `UoM.ISOCurrency` or `UoM.Unit`. Percentage values are annotated with `UoM.Unit = '%'`. A renderer should take an optional `Common.Text` annotation into consideration.
[TargetValue](./UI.xml#L380:~:text=<ComplexType%20Name="-,DataPointType,-")|PrimitiveType?|Target value
[ForecastValue](./UI.xml#L383:~:text=<ComplexType%20Name="-,DataPointType,-")|PrimitiveType?|Forecast value
[MinimumValue](./UI.xml#L386:~:text=<ComplexType%20Name="-,DataPointType,-")|Decimal?|Minimum value (for output rendering)
[MaximumValue](./UI.xml#L389:~:text=<ComplexType%20Name="-,DataPointType,-")|Decimal?|Maximum value (for output rendering)
[ValueFormat](./UI.xml#L392:~:text=<ComplexType%20Name="-,DataPointType,-")|[NumberFormat?](#NumberFormat)|Number format
[Visualization](./UI.xml#L395:~:text=<ComplexType%20Name="-,DataPointType,-")|[VisualizationType?](#VisualizationType)|Preferred visualization
[SampleSize](./UI.xml#L398:~:text=<ComplexType%20Name="-,DataPointType,-")|PrimitiveType?|Sample size used for the determination of the data point; should contain just integer value as Edm.Byte, Edm.SByte, Edm.Intxx, and Edm.Decimal with scale 0.
[ReferencePeriod](./UI.xml#L405:~:text=<ComplexType%20Name="-,DataPointType,-")|[ReferencePeriod?](#ReferencePeriod)|Reference period
[Criticality](./UI.xml#L408:~:text=<ComplexType%20Name="-,DataPointType,-")|[CriticalityType?](#CriticalityType)|Service-calculated criticality, alternative to CriticalityCalculation
[CriticalityLabels](./UI.xml#L411:~:text=<ComplexType%20Name="-,DataPointType,-")|AnnotationPath?|Custom labels for the criticality legend. Annotation path MUST end in UI.CriticalityLabels<br>Allowed terms:<br>- [CriticalityLabels](#CriticalityLabels)
[CriticalityRepresentation](./UI.xml#L419:~:text=<ComplexType%20Name="-,DataPointType,-") *([Experimental](Common.md#Experimental))*|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[CriticalityCalculation](./UI.xml#L423:~:text=<ComplexType%20Name="-,DataPointType,-")|[CriticalityCalculationType?](#CriticalityCalculationType)|Parameters for client-calculated criticality, alternative to Criticality
[Trend](./UI.xml#L426:~:text=<ComplexType%20Name="-,DataPointType,-")|[TrendType?](#TrendType)|Service-calculated trend, alternative to TrendCalculation
[TrendCalculation](./UI.xml#L429:~:text=<ComplexType%20Name="-,DataPointType,-")|[TrendCalculationType?](#TrendCalculationType)|Parameters for client-calculated trend, alternative to Trend
[Responsible](./UI.xml#L432:~:text=<ComplexType%20Name="-,DataPointType,-")|[ContactType?](Communication.md#ContactType)|Contact person

<a name="NumberFormat"></a>
## [NumberFormat](./UI.xml#L437:~:text=<ComplexType%20Name="-,NumberFormat,-")
Describes how to visualise a number

Property|Type|Description
:-------|:---|:----------
[ScaleFactor](./UI.xml#L439:~:text=<ComplexType%20Name="-,NumberFormat,-")|Decimal?|Display value in *ScaleFactor* units, e.g. 1000 for k (kilo), 1e6 for M (Mega)
[NumberOfFractionalDigits](./UI.xml#L442:~:text=<ComplexType%20Name="-,NumberFormat,-")|Byte?|Number of fractional digits of the scaled value to be visualized

<a name="VisualizationType"></a>
## [VisualizationType](./UI.xml#L447:~:text=<EnumType%20Name="-,VisualizationType,-")


Member|Value|Description
:-----|----:|:----------
[Number](./UI.xml#L448:~:text=<EnumType%20Name="-,VisualizationType,-")|0|Visualize as a number
[BulletChart](./UI.xml#L451:~:text=<EnumType%20Name="-,VisualizationType,-")|1|Visualize as bullet chart - requires TargetValue
[Progress](./UI.xml#L454:~:text=<EnumType%20Name="-,VisualizationType,-")|2|Visualize as progress indicator - requires TargetValue
[Rating](./UI.xml#L457:~:text=<EnumType%20Name="-,VisualizationType,-")|3|Visualize as partially or completely filled stars/hearts/... - requires TargetValue
[Donut](./UI.xml#L460:~:text=<EnumType%20Name="-,VisualizationType,-")|4|Visualize as donut, optionally with missing segment - requires TargetValue
[DeltaBulletChart](./UI.xml#L463:~:text=<EnumType%20Name="-,VisualizationType,-")|5|Visualize as delta bullet chart - requires TargetValue

<a name="ReferencePeriod"></a>
## [ReferencePeriod](./UI.xml#L468:~:text=<ComplexType%20Name="-,ReferencePeriod,-")
Reference period

Property|Type|Description
:-------|:---|:----------
[Description](./UI.xml#L470:~:text=<ComplexType%20Name="-,ReferencePeriod,-")|String?|Short description of the reference period
[Start](./UI.xml#L474:~:text=<ComplexType%20Name="-,ReferencePeriod,-")|DateTimeOffset?|Start of the reference period
[End](./UI.xml#L477:~:text=<ComplexType%20Name="-,ReferencePeriod,-")|DateTimeOffset?|End of the reference period

<a name="CriticalityType"></a>
## [CriticalityType](./UI.xml#L482:~:text=<EnumType%20Name="-,CriticalityType,-")
Criticality of a value or status, represented e.g. via semantic colors (https://experience.sap.com/fiori-design-web/foundation/colors/#semantic-colors)

Member|Value|Description
:-----|----:|:----------
[VeryNegative](./UI.xml#L484:~:text=<EnumType%20Name="-,CriticalityType,-") *([Experimental](Common.md#Experimental))*|-1|Very negative / dark-red status - risk - out of stock - late
[Neutral](./UI.xml#L488:~:text=<EnumType%20Name="-,CriticalityType,-")|0|Neutral / grey status - inactive - open - in progress
[Negative](./UI.xml#L491:~:text=<EnumType%20Name="-,CriticalityType,-")|1|Negative / red status - attention - overload - alert
[Critical](./UI.xml#L494:~:text=<EnumType%20Name="-,CriticalityType,-")|2|Critical / orange status - warning
[Positive](./UI.xml#L497:~:text=<EnumType%20Name="-,CriticalityType,-")|3|Positive / green status - completed - available - on track - acceptable
[VeryPositive](./UI.xml#L500:~:text=<EnumType%20Name="-,CriticalityType,-") *([Experimental](Common.md#Experimental))*|4|Very positive - above max stock - excess
[Information](./UI.xml#L504:~:text=<EnumType%20Name="-,CriticalityType,-") *([Experimental](Common.md#Experimental))*|5|Information - noticable - informative

<a name="CriticalityCalculationType"></a>
## [CriticalityCalculationType](./UI.xml#L510:~:text=<ComplexType%20Name="-,CriticalityCalculationType,-"): [CriticalityThresholdsType](#CriticalityThresholdsType)
Describes how to calculate the criticality of a value depending on the improvement direction


The calculation is done by comparing a value to the threshold values relevant for the specified improvement direction.

The value to be compared is
  - Value - if ReferenceValue is not specified
  - Value sub ReferenceValue – if ReferenceValue is specified and IsRelativeDifference is not specified or specified as false
  - (Value sub ReferenceValue) divBy ReferenceValue – if ReferenceValue is specified and IsRelativeDifference is specified as true

For improvement direction `Target`, the criticality is calculated using both low and high threshold values. It will be
  - Positive if the value is greater than or equal to AcceptanceRangeLowValue and lower than or equal to AcceptanceRangeHighValue
  - Neutral if the value is greater than or equal to ToleranceRangeLowValue and lower than AcceptanceRangeLowValue OR greater than AcceptanceRangeHighValue and lower than or equal to ToleranceRangeHighValue
  - Critical if the value is greater than or equal to DeviationRangeLowValue and lower than ToleranceRangeLowValue OR greater than ToleranceRangeHighValue  and lower than or equal to DeviationRangeHighValue
  - Negative if the value is lower than DeviationRangeLowValue or greater than DeviationRangeHighValue

For improvement direction `Minimize`, the criticality is calculated using the high threshold values. It is
  - Positive if the value is lower than or equal to AcceptanceRangeHighValue
  - Neutral if the value is  greater than AcceptanceRangeHighValue and lower than or equal to ToleranceRangeHighValue
  - Critical if the value is greater than ToleranceRangeHighValue and lower than or equal to DeviationRangeHighValue
  - Negative if the value is greater than DeviationRangeHighValue

For improvement direction `Maximize`, the criticality is calculated using the low threshold values. It is
  - Positive if the value is greater than or equal to AcceptanceRangeLowValue
  - Neutral if the value is less than AcceptanceRangeLowValue and greater than or equal to ToleranceRangeLowValue
  - Critical if the value is lower than ToleranceRangeLowValue and greater than or equal to DeviationRangeLowValue
  - Negative if the value is lower than DeviationRangeLowValue

Thresholds are optional. For unassigned values, defaults are determined in this order:
  - For DeviationRange, an omitted LowValue translates into the smallest possible number (-INF), an omitted HighValue translates into the largest possible number (+INF)
  - For ToleranceRange, an omitted LowValue will be initialized with DeviationRangeLowValue, an omitted HighValue will be initialized with DeviationRangeHighValue
  - For AcceptanceRange, an omitted LowValue will be initialized with ToleranceRangeLowValue, an omitted HighValue will be initialized with ToleranceRangeHighValue
          

Property|Type|Description
:-------|:---|:----------
[*AcceptanceRangeLowValue*](./UI.xml#L565:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Lowest value that is considered positive
[*AcceptanceRangeHighValue*](./UI.xml#L568:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Highest value that is considered positive
[*ToleranceRangeLowValue*](./UI.xml#L571:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Lowest value that is considered neutral
[*ToleranceRangeHighValue*](./UI.xml#L574:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Highest value that is considered neutral
[*DeviationRangeLowValue*](./UI.xml#L577:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Lowest value that is considered critical
[*DeviationRangeHighValue*](./UI.xml#L580:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Highest value that is considered critical
[ReferenceValue](./UI.xml#L545:~:text=<ComplexType%20Name="-,CriticalityCalculationType,-") *([Experimental](Common.md#Experimental))*|PrimitiveType?|Reference value for the calculation, e.g. number of sales for the last year
[IsRelativeDifference](./UI.xml#L549:~:text=<ComplexType%20Name="-,CriticalityCalculationType,-") *([Experimental](Common.md#Experimental))*|Boolean|Calculate with a relative difference
[ImprovementDirection](./UI.xml#L553:~:text=<ComplexType%20Name="-,CriticalityCalculationType,-")|[ImprovementDirectionType](#ImprovementDirectionType)|Describes in which direction the value improves
[ConstantThresholds](./UI.xml#L556:~:text=<ComplexType%20Name="-,CriticalityCalculationType,-") *([Experimental](Common.md#Experimental))*|\[[LevelThresholdsType](#LevelThresholdsType)\]|List of thresholds depending on the aggregation level as a set of constant values<br>Constant thresholds shall only be used in order to refine constant values given for the data point overall (aggregation level with empty collection of property paths), but not if the thresholds are based on other measure elements.

<a name="CriticalityThresholdsType"></a>
## [CriticalityThresholdsType](./UI.xml#L563:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")
Thresholds for calculating the criticality of a value

**Derived Types:**
- [CriticalityCalculationType](#CriticalityCalculationType)
- [LevelThresholdsType](#LevelThresholdsType)

Property|Type|Description
:-------|:---|:----------
[AcceptanceRangeLowValue](./UI.xml#L565:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Lowest value that is considered positive
[AcceptanceRangeHighValue](./UI.xml#L568:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Highest value that is considered positive
[ToleranceRangeLowValue](./UI.xml#L571:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Lowest value that is considered neutral
[ToleranceRangeHighValue](./UI.xml#L574:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Highest value that is considered neutral
[DeviationRangeLowValue](./UI.xml#L577:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Lowest value that is considered critical
[DeviationRangeHighValue](./UI.xml#L580:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Highest value that is considered critical

<a name="ImprovementDirectionType"></a>
## [ImprovementDirectionType](./UI.xml#L585:~:text=<EnumType%20Name="-,ImprovementDirectionType,-")
Describes which direction of a value change is seen as an improvement

Member|Value|Description
:-----|----:|:----------
[Minimize](./UI.xml#L587:~:text=<EnumType%20Name="-,ImprovementDirectionType,-")|1|Lower is better
[Target](./UI.xml#L590:~:text=<EnumType%20Name="-,ImprovementDirectionType,-")|2|Closer to the target is better
[Maximize](./UI.xml#L593:~:text=<EnumType%20Name="-,ImprovementDirectionType,-")|3|Higher is better

<a name="LevelThresholdsType"></a>
## [LevelThresholdsType](./UI.xml#L598:~:text=<ComplexType%20Name="-,LevelThresholdsType,-"): [CriticalityThresholdsType](#CriticalityThresholdsType) *([Experimental](Common.md#Experimental))*
Thresholds for an aggregation level

Property|Type|Description
:-------|:---|:----------
[*AcceptanceRangeLowValue*](./UI.xml#L565:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Lowest value that is considered positive
[*AcceptanceRangeHighValue*](./UI.xml#L568:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Highest value that is considered positive
[*ToleranceRangeLowValue*](./UI.xml#L571:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Lowest value that is considered neutral
[*ToleranceRangeHighValue*](./UI.xml#L574:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Highest value that is considered neutral
[*DeviationRangeLowValue*](./UI.xml#L577:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Lowest value that is considered critical
[*DeviationRangeHighValue*](./UI.xml#L580:~:text=<ComplexType%20Name="-,CriticalityThresholdsType,-")|PrimitiveType?|Highest value that is considered critical
[AggregationLevel](./UI.xml#L601:~:text=<ComplexType%20Name="-,LevelThresholdsType,-")|\[PropertyPath\]|An unordered tuple of dimensions, i.e. properties which are intended to be used for grouping in aggregating requests. In analytical UIs, e.g. an analytical chart, the aggregation level typically corresponds to the visible dimensions.

<a name="TrendType"></a>
## [TrendType](./UI.xml#L606:~:text=<EnumType%20Name="-,TrendType,-")
The trend of a value

Member|Value|Description
:-----|----:|:----------
[StrongUp](./UI.xml#L608:~:text=<EnumType%20Name="-,TrendType,-")|1|Value grows strongly
[Up](./UI.xml#L611:~:text=<EnumType%20Name="-,TrendType,-")|2|Value grows
[Sideways](./UI.xml#L614:~:text=<EnumType%20Name="-,TrendType,-")|3|Value does not significantly grow or shrink
[Down](./UI.xml#L617:~:text=<EnumType%20Name="-,TrendType,-")|4|Value shrinks
[StrongDown](./UI.xml#L620:~:text=<EnumType%20Name="-,TrendType,-")|5|Value shrinks strongly

<a name="TrendCalculationType"></a>
## [TrendCalculationType](./UI.xml#L625:~:text=<ComplexType%20Name="-,TrendCalculationType,-")
Describes how to calculate the trend of a value


By default, the calculation is done by comparing the difference between Value and ReferenceValue to the threshold values.
If IsRelativeDifference is set, the difference of Value and ReferenceValue is divided by ReferenceValue and the relative difference is compared.

The trend is
  - StrongUp if the difference is greater than or equal to StrongUpDifference
  - Up if the difference is less than StrongUpDifference and greater than or equal to UpDifference
  - Sideways if the difference  is less than UpDifference and greater than DownDifference
  - Down if the difference is greater than StrongDownDifference and lower than or equal to DownDifference
  - StrongDown if the difference is lower than or equal to StrongDownDifference

Property|Type|Description
:-------|:---|:----------
[ReferenceValue](./UI.xml#L639:~:text=<ComplexType%20Name="-,TrendCalculationType,-")|PrimitiveType|Reference value for the calculation, e.g. number of sales for the last year
[IsRelativeDifference](./UI.xml#L642:~:text=<ComplexType%20Name="-,TrendCalculationType,-")|Boolean|Calculate with a relative difference
[UpDifference](./UI.xml#L645:~:text=<ComplexType%20Name="-,TrendCalculationType,-")|Decimal|Threshold for Up
[StrongUpDifference](./UI.xml#L648:~:text=<ComplexType%20Name="-,TrendCalculationType,-")|Decimal|Threshold for StrongUp
[DownDifference](./UI.xml#L651:~:text=<ComplexType%20Name="-,TrendCalculationType,-")|Decimal|Threshold for Down
[StrongDownDifference](./UI.xml#L654:~:text=<ComplexType%20Name="-,TrendCalculationType,-")|Decimal|Threshold for StrongDown

<a name="KPIType"></a>
## [KPIType](./UI.xml#L665:~:text=<ComplexType%20Name="-,KPIType,-")


Property|Type|Description
:-------|:---|:----------
[ID](./UI.xml#L666:~:text=<ComplexType%20Name="-,KPIType,-")|String?|Optional identifier to reference this instance from an external context
[ShortDescription](./UI.xml#L671:~:text=<ComplexType%20Name="-,KPIType,-") *([Experimental](Common.md#Experimental))*|String?|Very short description
[SelectionVariant](./UI.xml#L676:~:text=<ComplexType%20Name="-,KPIType,-")|[SelectionVariantType](#SelectionVariantType)|Selection variant, either specified inline or referencing another annotation via Path
[DataPoint](./UI.xml#L679:~:text=<ComplexType%20Name="-,KPIType,-")|[DataPointType](#DataPointType)|Data point, either specified inline or referencing another annotation via Path
[AdditionalDataPoints](./UI.xml#L682:~:text=<ComplexType%20Name="-,KPIType,-")|\[[DataPointType](#DataPointType)\]|Additional data points, either specified inline or referencing another annotation via Path<br>Additional data points are typically related to the main data point and provide complementing information or could be used for comparisons
[Detail](./UI.xml#L686:~:text=<ComplexType%20Name="-,KPIType,-")|[KPIDetailType?](#KPIDetailType)|Contains information about KPI details, especially drill-down presentations

<a name="KPIDetailType"></a>
## [KPIDetailType](./UI.xml#L690:~:text=<ComplexType%20Name="-,KPIDetailType,-")


Property|Type|Description
:-------|:---|:----------
[DefaultPresentationVariant](./UI.xml#L691:~:text=<ComplexType%20Name="-,KPIDetailType,-")|[PresentationVariantType?](#PresentationVariantType)|Presentation variant, either specified inline or referencing another annotation via Path
[AlternativePresentationVariants](./UI.xml#L694:~:text=<ComplexType%20Name="-,KPIDetailType,-")|\[[PresentationVariantType](#PresentationVariantType)\]|A list of alternative presentation variants, either specified inline or referencing another annotation via Path
[SemanticObject](./UI.xml#L697:~:text=<ComplexType%20Name="-,KPIDetailType,-")|String?|Name of the Semantic Object. If not specified, use Semantic Object annotated at the property referenced in KPI/DataPoint/Value
[Action](./UI.xml#L700:~:text=<ComplexType%20Name="-,KPIDetailType,-")|String?|Name of the Action on the Semantic Object. If not specified, let user choose which of the available actions to trigger.

<a name="ChartDefinitionType"></a>
## [ChartDefinitionType](./UI.xml#L709:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")


Property|Type|Description
:-------|:---|:----------
[Title](./UI.xml#L710:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")|String?|Title of the chart
[Description](./UI.xml#L714:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")|String?|Short description
[ChartType](./UI.xml#L718:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")|[ChartType](#ChartType)|Chart type
[AxisScaling](./UI.xml#L721:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")|[ChartAxisScalingType?](#ChartAxisScalingType)|Describes the scale of the chart value axes
[Measures](./UI.xml#L724:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")|\[PropertyPath\]|Measures of the chart, e.g. size and color in a bubble chart
[DynamicMeasures](./UI.xml#L728:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")|\[AnnotationPath\]|Dynamic properties introduced by annotations and used as measures of the chart<br>If the annotation referenced by an annotation path does not apply to the same collection of entities as the one being visualized according to the `UI.Chart` annotation, the annotation path MUST be silently ignored.<br>Allowed terms:<br>- [AggregatedProperty](Analytics.md#AggregatedProperty)<br>- [CustomAggregate](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Aggregation.V1.md#CustomAggregate)
[MeasureAttributes](./UI.xml#L741:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")|\[[ChartMeasureAttributeType](#ChartMeasureAttributeType)\]|Describes Attributes for Measures. All Measures used in this collection must also be part of the Measures Property.
[Dimensions](./UI.xml#L746:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")|\[PropertyPath\]|Dimensions of the chart, e.g. x- and y-axis of a bubble chart
[DimensionAttributes](./UI.xml#L749:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")|\[[ChartDimensionAttributeType](#ChartDimensionAttributeType)\]|Describes Attributes for Dimensions. All Dimensions used in this collection must also be part of the Dimensions Property.
[Actions](./UI.xml#L754:~:text=<ComplexType%20Name="-,ChartDefinitionType,-")|\[[DataFieldForActionAbstract](#DataFieldForActionAbstract)\]|Available actions

<a name="ChartType"></a>
## [ChartType](./UI.xml#L759:~:text=<EnumType%20Name="-,ChartType,-")


Member|Value|Description
:-----|----:|:----------
[Column](./UI.xml#L760:~:text=<EnumType%20Name="-,ChartType,-")|0|
[ColumnStacked](./UI.xml#L761:~:text=<EnumType%20Name="-,ChartType,-")|1|
[ColumnDual](./UI.xml#L762:~:text=<EnumType%20Name="-,ChartType,-")|2|
[ColumnStackedDual](./UI.xml#L763:~:text=<EnumType%20Name="-,ChartType,-")|3|
[ColumnStacked100](./UI.xml#L764:~:text=<EnumType%20Name="-,ChartType,-")|4|
[ColumnStackedDual100](./UI.xml#L765:~:text=<EnumType%20Name="-,ChartType,-")|5|
[Bar](./UI.xml#L766:~:text=<EnumType%20Name="-,ChartType,-")|6|
[BarStacked](./UI.xml#L767:~:text=<EnumType%20Name="-,ChartType,-")|7|
[BarDual](./UI.xml#L768:~:text=<EnumType%20Name="-,ChartType,-")|8|
[BarStackedDual](./UI.xml#L769:~:text=<EnumType%20Name="-,ChartType,-")|9|
[BarStacked100](./UI.xml#L770:~:text=<EnumType%20Name="-,ChartType,-")|10|
[BarStackedDual100](./UI.xml#L771:~:text=<EnumType%20Name="-,ChartType,-")|11|
[Area](./UI.xml#L772:~:text=<EnumType%20Name="-,ChartType,-")|12|
[AreaStacked](./UI.xml#L773:~:text=<EnumType%20Name="-,ChartType,-")|13|
[AreaStacked100](./UI.xml#L774:~:text=<EnumType%20Name="-,ChartType,-")|14|
[HorizontalArea](./UI.xml#L775:~:text=<EnumType%20Name="-,ChartType,-")|15|
[HorizontalAreaStacked](./UI.xml#L776:~:text=<EnumType%20Name="-,ChartType,-")|16|
[HorizontalAreaStacked100](./UI.xml#L777:~:text=<EnumType%20Name="-,ChartType,-")|17|
[Line](./UI.xml#L778:~:text=<EnumType%20Name="-,ChartType,-")|18|
[LineDual](./UI.xml#L779:~:text=<EnumType%20Name="-,ChartType,-")|19|
[Combination](./UI.xml#L780:~:text=<EnumType%20Name="-,ChartType,-")|20|
[CombinationStacked](./UI.xml#L781:~:text=<EnumType%20Name="-,ChartType,-")|21|
[CombinationDual](./UI.xml#L782:~:text=<EnumType%20Name="-,ChartType,-")|22|
[CombinationStackedDual](./UI.xml#L783:~:text=<EnumType%20Name="-,ChartType,-")|23|
[HorizontalCombinationStacked](./UI.xml#L784:~:text=<EnumType%20Name="-,ChartType,-")|24|
[Pie](./UI.xml#L785:~:text=<EnumType%20Name="-,ChartType,-")|25|
[Donut](./UI.xml#L786:~:text=<EnumType%20Name="-,ChartType,-")|26|
[Scatter](./UI.xml#L787:~:text=<EnumType%20Name="-,ChartType,-")|27|
[Bubble](./UI.xml#L788:~:text=<EnumType%20Name="-,ChartType,-")|28|
[Radar](./UI.xml#L789:~:text=<EnumType%20Name="-,ChartType,-")|29|
[HeatMap](./UI.xml#L790:~:text=<EnumType%20Name="-,ChartType,-")|30|
[TreeMap](./UI.xml#L791:~:text=<EnumType%20Name="-,ChartType,-")|31|
[Waterfall](./UI.xml#L792:~:text=<EnumType%20Name="-,ChartType,-")|32|
[Bullet](./UI.xml#L793:~:text=<EnumType%20Name="-,ChartType,-")|33|
[VerticalBullet](./UI.xml#L794:~:text=<EnumType%20Name="-,ChartType,-")|34|
[HorizontalWaterfall](./UI.xml#L795:~:text=<EnumType%20Name="-,ChartType,-")|35|
[HorizontalCombinationDual](./UI.xml#L796:~:text=<EnumType%20Name="-,ChartType,-")|36|
[HorizontalCombinationStackedDual](./UI.xml#L797:~:text=<EnumType%20Name="-,ChartType,-")|37|
[Donut100](./UI.xml#L798:~:text=<EnumType%20Name="-,ChartType,-") *([Experimental](Common.md#Experimental))*|38|

<a name="ChartAxisScalingType"></a>
## [ChartAxisScalingType](./UI.xml#L804:~:text=<ComplexType%20Name="-,ChartAxisScalingType,-")


Property|Type|Description
:-------|:---|:----------
[ScaleBehavior](./UI.xml#L805:~:text=<ComplexType%20Name="-,ChartAxisScalingType,-")|[ChartAxisScaleBehaviorType](#ChartAxisScaleBehaviorType)|Scale is fixed or adapts automatically to rendered values
[AutoScaleBehavior](./UI.xml#L808:~:text=<ComplexType%20Name="-,ChartAxisScalingType,-")|[ChartAxisAutoScaleBehaviorType?](#ChartAxisAutoScaleBehaviorType)|Settings for automatic scaling
[FixedScaleMultipleStackedMeasuresBoundaryValues](./UI.xml#L811:~:text=<ComplexType%20Name="-,ChartAxisScalingType,-")|[FixedScaleMultipleStackedMeasuresBoundaryValuesType?](#FixedScaleMultipleStackedMeasuresBoundaryValuesType)|Boundary values for fixed scaling of a stacking chart type with multiple measures

<a name="ChartAxisScaleBehaviorType"></a>
## [ChartAxisScaleBehaviorType](./UI.xml#L816:~:text=<EnumType%20Name="-,ChartAxisScaleBehaviorType,-")


Member|Value|Description
:-----|----:|:----------
[AutoScale](./UI.xml#L817:~:text=<EnumType%20Name="-,ChartAxisScaleBehaviorType,-")|0|Value axes scale automatically
[FixedScale](./UI.xml#L820:~:text=<EnumType%20Name="-,ChartAxisScaleBehaviorType,-")|1|Fixed minimum and maximum values are applied, which are derived from the @UI.MeasureAttributes.DataPoint/MinimumValue and .../MaximumValue annotation by default. For stacking chart types with multiple measures, they are taken from ChartAxisScalingType/FixedScaleMultipleStackedMeasuresBoundaryValues.

<a name="ChartAxisAutoScaleBehaviorType"></a>
## [ChartAxisAutoScaleBehaviorType](./UI.xml#L829:~:text=<ComplexType%20Name="-,ChartAxisAutoScaleBehaviorType,-")


Property|Type|Description
:-------|:---|:----------
[ZeroAlwaysVisible](./UI.xml#L830:~:text=<ComplexType%20Name="-,ChartAxisAutoScaleBehaviorType,-")|Boolean|Forces the value axis to always display the zero value
[DataScope](./UI.xml#L833:~:text=<ComplexType%20Name="-,ChartAxisAutoScaleBehaviorType,-")|[ChartAxisAutoScaleDataScopeType](#ChartAxisAutoScaleDataScopeType)|Determines the automatic scaling

<a name="ChartAxisAutoScaleDataScopeType"></a>
## [ChartAxisAutoScaleDataScopeType](./UI.xml#L838:~:text=<EnumType%20Name="-,ChartAxisAutoScaleDataScopeType,-")


Member|Value|Description
:-----|----:|:----------
[DataSet](./UI.xml#L839:~:text=<EnumType%20Name="-,ChartAxisAutoScaleDataScopeType,-")|0|Minimum and maximum axes values are determined from the entire data set
[VisibleData](./UI.xml#L842:~:text=<EnumType%20Name="-,ChartAxisAutoScaleDataScopeType,-")|1|Minimum and maximum axes values are determined from the currently visible data. Scrolling will change the scale.

<a name="FixedScaleMultipleStackedMeasuresBoundaryValuesType"></a>
## [FixedScaleMultipleStackedMeasuresBoundaryValuesType](./UI.xml#L847:~:text=<ComplexType%20Name="-,FixedScaleMultipleStackedMeasuresBoundaryValuesType,-")


Property|Type|Description
:-------|:---|:----------
[MinimumValue](./UI.xml#L848:~:text=<ComplexType%20Name="-,FixedScaleMultipleStackedMeasuresBoundaryValuesType,-")|Decimal|Minimum value on value axes
[MaximumValue](./UI.xml#L851:~:text=<ComplexType%20Name="-,FixedScaleMultipleStackedMeasuresBoundaryValuesType,-")|Decimal|Maximum value on value axes

<a name="ChartDimensionAttributeType"></a>
## [ChartDimensionAttributeType](./UI.xml#L856:~:text=<ComplexType%20Name="-,ChartDimensionAttributeType,-")


Property|Type|Description
:-------|:---|:----------
[Dimension](./UI.xml#L857:~:text=<ComplexType%20Name="-,ChartDimensionAttributeType,-")|PropertyPath?|
[Role](./UI.xml#L858:~:text=<ComplexType%20Name="-,ChartDimensionAttributeType,-")|[ChartDimensionRoleType?](#ChartDimensionRoleType)|
[HierarchyLevel](./UI.xml#L859:~:text=<ComplexType%20Name="-,ChartDimensionAttributeType,-") *([Experimental](Common.md#Experimental))*|Int32?|For a dimension with a hierarchy, members are selected from this level. The root node of the hierarchy is at level 0.
[ValuesForSequentialColorLevels](./UI.xml#L863:~:text=<ComplexType%20Name="-,ChartDimensionAttributeType,-") *([Experimental](Common.md#Experimental))*|\[String\]|All values in this collection should be assigned to levels of the same color.
[EmphasizedValues](./UI.xml#L867:~:text=<ComplexType%20Name="-,ChartDimensionAttributeType,-") *([Experimental](Common.md#Experimental))*|\[String\]|All values in this collection should be emphasized.
[EmphasisLabels](./UI.xml#L871:~:text=<ComplexType%20Name="-,ChartDimensionAttributeType,-") *([Experimental](Common.md#Experimental))*|[EmphasisLabelType?](#EmphasisLabelType)|Assign a label to values with an emphasized representation. This is required, if more than one emphasized value has been specified.

<a name="ChartMeasureAttributeType"></a>
## [ChartMeasureAttributeType](./UI.xml#L877:~:text=<ComplexType%20Name="-,ChartMeasureAttributeType,-")
Exactly one of `Measure` and `DynamicMeasure` must be present

Property|Type|Description
:-------|:---|:----------
[Measure](./UI.xml#L879:~:text=<ComplexType%20Name="-,ChartMeasureAttributeType,-")|PropertyPath?|
[DynamicMeasure](./UI.xml#L882:~:text=<ComplexType%20Name="-,ChartMeasureAttributeType,-")|AnnotationPath?|Dynamic property introduced by an annotation and used as a measure in a chart<br>If the annotation referenced by an annotation path does not apply to the same collection of entities as the one being visualized according to the `UI.Chart` annotation, the annotation path MUST be silently ignored.<br>Allowed terms:<br>- [AggregatedProperty](Analytics.md#AggregatedProperty)<br>- [CustomAggregate](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Aggregation.V1.md#CustomAggregate)
[Role](./UI.xml#L895:~:text=<ComplexType%20Name="-,ChartMeasureAttributeType,-")|[ChartMeasureRoleType?](#ChartMeasureRoleType)|
[DataPoint](./UI.xml#L896:~:text=<ComplexType%20Name="-,ChartMeasureAttributeType,-")|AnnotationPath?|Annotation path MUST end in @UI.DataPoint and the data point's Value MUST be the same property as in Measure<br>Allowed terms:<br>- [DataPoint](#DataPoint)
[UseSequentialColorLevels](./UI.xml#L904:~:text=<ComplexType%20Name="-,ChartMeasureAttributeType,-") *([Experimental](Common.md#Experimental))*|Boolean|All measures for which this setting is true should be assigned to levels of the same color.

<a name="ChartDimensionRoleType"></a>
## [ChartDimensionRoleType](./UI.xml#L910:~:text=<EnumType%20Name="-,ChartDimensionRoleType,-")


Member|Value|Description
:-----|----:|:----------
[Category](./UI.xml#L911:~:text=<EnumType%20Name="-,ChartDimensionRoleType,-")|0|
[Series](./UI.xml#L912:~:text=<EnumType%20Name="-,ChartDimensionRoleType,-")|1|
[Category2](./UI.xml#L913:~:text=<EnumType%20Name="-,ChartDimensionRoleType,-")|2|

<a name="ChartMeasureRoleType"></a>
## [ChartMeasureRoleType](./UI.xml#L916:~:text=<EnumType%20Name="-,ChartMeasureRoleType,-")


Member|Value|Description
:-----|----:|:----------
[Axis1](./UI.xml#L917:~:text=<EnumType%20Name="-,ChartMeasureRoleType,-")|0|
[Axis2](./UI.xml#L918:~:text=<EnumType%20Name="-,ChartMeasureRoleType,-")|1|
[Axis3](./UI.xml#L919:~:text=<EnumType%20Name="-,ChartMeasureRoleType,-")|2|

<a name="EmphasisLabelType"></a>
## [EmphasisLabelType](./UI.xml#L922:~:text=<ComplexType%20Name="-,EmphasisLabelType,-") *([Experimental](Common.md#Experimental))*
Assigns a label to the set of emphasized values and optionally also for non-emphasized values. This information can be used for semantic coloring.

Property|Type|Description
:-------|:---|:----------
[EmphasizedValuesLabel](./UI.xml#L925:~:text=<ComplexType%20Name="-,EmphasisLabelType,-")|String|
[NonEmphasizedValuesLabel](./UI.xml#L926:~:text=<ComplexType%20Name="-,EmphasisLabelType,-")|String?|

<a name="ValueCriticalityType"></a>
## [ValueCriticalityType](./UI.xml#L933:~:text=<ComplexType%20Name="-,ValueCriticalityType,-") *([Experimental](Common.md#Experimental))*
Assigns a fixed criticality to a primitive value. This information can be used for semantic coloring.

Property|Type|Description
:-------|:---|:----------
[Value](./UI.xml#L936:~:text=<ComplexType%20Name="-,ValueCriticalityType,-")|PrimitiveType?|MUST be a fixed value of primitive type
[Criticality](./UI.xml#L939:~:text=<ComplexType%20Name="-,ValueCriticalityType,-")|[CriticalityType?](#CriticalityType)|

<a name="CriticalityLabelType"></a>
## [CriticalityLabelType](./UI.xml#L953:~:text=<ComplexType%20Name="-,CriticalityLabelType,-") *([Experimental](Common.md#Experimental))*
Assigns a label to a criticality. This information can be used for semantic coloring.

Property|Type|Description
:-------|:---|:----------
[Criticality](./UI.xml#L956:~:text=<ComplexType%20Name="-,CriticalityLabelType,-")|[CriticalityType](#CriticalityType)|
[Label](./UI.xml#L957:~:text=<ComplexType%20Name="-,CriticalityLabelType,-")|String|Criticality label

<a name="Facet"></a>
## [*Facet*](./UI.xml#L991:~:text=<ComplexType%20Name="-,Facet,-")
Abstract base type for facets

**Derived Types:**
- [CollectionFacet](#CollectionFacet)
- [ReferenceFacet](#ReferenceFacet)
- [ReferenceURLFacet](#ReferenceURLFacet)

Property|Type|Description
:-------|:---|:----------
[Label](./UI.xml#L999:~:text=<ComplexType%20Name="-,Facet,-")|String?|Facet label
[ID](./UI.xml#L1003:~:text=<ComplexType%20Name="-,Facet,-")|String?|Unique identifier of a facet. ID should be stable, as long as the perceived semantics of the facet is unchanged.

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [PartOfPreview](#PartOfPreview)

<a name="CollectionFacet"></a>
## [CollectionFacet](./UI.xml#L1007:~:text=<ComplexType%20Name="-,CollectionFacet,-"): [Facet](#Facet)
Collection of facets

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L999:~:text=<ComplexType%20Name="-,Facet,-")|String?|Facet label
[*ID*](./UI.xml#L1003:~:text=<ComplexType%20Name="-,Facet,-")|String?|Unique identifier of a facet. ID should be stable, as long as the perceived semantics of the facet is unchanged.
[Facets](./UI.xml#L1009:~:text=<ComplexType%20Name="-,CollectionFacet,-")|\[[Facet](#Facet)\]|Nested facets. An empty collection may be used as a placeholder for content added via extension points.

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [PartOfPreview](#PartOfPreview)

<a name="ReferenceFacet"></a>
## [ReferenceFacet](./UI.xml#L1013:~:text=<ComplexType%20Name="-,ReferenceFacet,-"): [Facet](#Facet)
Facet that refers to a thing perspective, e.g. LineItem

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L999:~:text=<ComplexType%20Name="-,Facet,-")|String?|Facet label
[*ID*](./UI.xml#L1003:~:text=<ComplexType%20Name="-,Facet,-")|String?|Unique identifier of a facet. ID should be stable, as long as the perceived semantics of the facet is unchanged.
[Target](./UI.xml#L1015:~:text=<ComplexType%20Name="-,ReferenceFacet,-")|AnnotationPath|Referenced information: Communication.Contact, Communication.Address, or a term that is tagged with UI.ThingPerspective, e.g. UI.StatusInfo, UI.LineItem, UI.Identification, UI.FieldGroup, UI.Badge<br>Allowed terms:<br>- [Address](Communication.md#Address)<br>- [Contact](Communication.md#Contact)<br>- [Badge](#Badge)<br>- [Chart](#Chart)<br>- [Contacts](#Contacts)<br>- [DataPoint](#DataPoint)<br>- [FieldGroup](#FieldGroup)<br>- [GeoLocation](#GeoLocation)<br>- [GeoLocations](#GeoLocations)<br>- [HeaderInfo](#HeaderInfo)<br>- [Identification](#Identification)<br>- [KPI](#KPI)<br>- [LineItem](#LineItem)<br>- [MediaResource](#MediaResource)<br>- [Note](#Note)<br>- [PresentationVariant](#PresentationVariant)<br>- [SelectionFields](#SelectionFields)<br>- [SelectionPresentationVariant](#SelectionPresentationVariant)<br>- [StatusInfo](#StatusInfo)

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [PartOfPreview](#PartOfPreview)

<a name="ReferenceURLFacet"></a>
## [ReferenceURLFacet](./UI.xml#L1042:~:text=<ComplexType%20Name="-,ReferenceURLFacet,-"): [Facet](#Facet)
Facet that refers to a URL

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L999:~:text=<ComplexType%20Name="-,Facet,-")|String?|Facet label
[*ID*](./UI.xml#L1003:~:text=<ComplexType%20Name="-,Facet,-")|String?|Unique identifier of a facet. ID should be stable, as long as the perceived semantics of the facet is unchanged.
[Url](./UI.xml#L1044:~:text=<ComplexType%20Name="-,ReferenceURLFacet,-")|URL|URL of referenced information<br>Can be annotated with:<br>- [LinkTarget](HTML5.md#LinkTarget)
[UrlContentType](./UI.xml#L1053:~:text=<ComplexType%20Name="-,ReferenceURLFacet,-")|MediaType?|Media type of referenced information

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [PartOfPreview](#PartOfPreview)

<a name="SelectionPresentationVariantType"></a>
## [SelectionPresentationVariantType](./UI.xml#L1066:~:text=<ComplexType%20Name="-,SelectionPresentationVariantType,-")


Property|Type|Description
:-------|:---|:----------
[ID](./UI.xml#L1067:~:text=<ComplexType%20Name="-,SelectionPresentationVariantType,-")|String?|Optional identifier to reference this variant from an external context
[Text](./UI.xml#L1072:~:text=<ComplexType%20Name="-,SelectionPresentationVariantType,-")|String?|Name of the bundling variant
[SelectionVariant](./UI.xml#L1076:~:text=<ComplexType%20Name="-,SelectionPresentationVariantType,-")|[SelectionVariantType](#SelectionVariantType)|Selection variant, either specified inline or referencing another annotation via Path
[PresentationVariant](./UI.xml#L1079:~:text=<ComplexType%20Name="-,SelectionPresentationVariantType,-")|[PresentationVariantType](#PresentationVariantType)|Presentation variant, either specified inline or referencing another annotation via Path

<a name="PresentationVariantType"></a>
## [PresentationVariantType](./UI.xml#L1090:~:text=<ComplexType%20Name="-,PresentationVariantType,-")


Property|Type|Description
:-------|:---|:----------
[ID](./UI.xml#L1091:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|String?|Optional identifier to reference this variant from an external context
[Text](./UI.xml#L1094:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|String?|Name of the presentation variant
[MaxItems](./UI.xml#L1098:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|Int32?|Maximum number of items that should be included in the result
[SortOrder](./UI.xml#L1101:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|\[[SortOrderType](Common.md#SortOrderType)\]|Collection can be provided inline or as a reference to a Common.SortOrder annotation via Path
[GroupBy](./UI.xml#L1104:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|\[PropertyPath\]|Sequence of groupable properties p1, p2, ... defining how the result is composed of instances representing groups, one for each combination of value properties in the queried collection. The sequence specifies a certain level of aggregation for the queried collection, and every group instance will provide aggregated values for properties that are aggregatable. Moreover, the series of sub-sequences (p1), (p1, p2), ... forms a leveled hierarchy, which may become relevant in combination with `InitialExpansionLevel`.
[TotalBy](./UI.xml#L1113:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|\[PropertyPath\]|Sub-sequence q1, q2, ... of properties p1, p2, ... specified in GroupBy. With this, additional levels of aggregation are requested in addition to the most granular level defined by GroupBy: Every element in the series of sub-sequences (q1), (q1, q2), ... introduces an additional aggregation level included in the result.
[Total](./UI.xml#L1120:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|\[PropertyPath\]|Aggregatable properties for which aggregated values should be provided for the additional aggregation levels specified in TotalBy.
[DynamicTotal](./UI.xml#L1126:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|\[AnnotationPath\]|Dynamic properties introduced by annotations for which aggregated values should be provided for the additional aggregation levels specified in TotalBy<br>If the annotation referenced by an annotation path does not apply to the same collection of entities as the one being presented according to the `UI.PresentationVariant` annotation, the annotation path MUST be silently ignored.<br>Allowed terms:<br>- [AggregatedProperty](Analytics.md#AggregatedProperty)<br>- [CustomAggregate](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Aggregation.V1.md#CustomAggregate)
[IncludeGrandTotal](./UI.xml#L1139:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|Boolean|Result should include a grand total for the properties specified in Total
[InitialExpansionLevel](./UI.xml#L1142:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|Int32|Level up to which the hierarchy defined for the queried collection should be expanded initially. The hierarchy may be implicitly imposed by the sequence of the GroupBy, or by an explicit hierarchy annotation.
[Visualizations](./UI.xml#L1148:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|\[AnnotationPath\]|Lists available visualization types. Currently supported types are `UI.LineItem`, `UI.Chart`, and `UI.DataPoint`. For each type, no more than a single annotation is meaningful. Multiple instances of the same visualization type shall be modeled with different presentation variants. A reference to `UI.Lineitem` should always be part of the collection (least common denominator for renderers). The first entry of the collection is the default visualization.<br>Allowed terms:<br>- [Chart](#Chart)<br>- [DataPoint](#DataPoint)<br>- [LineItem](#LineItem)
[RequestAtLeast](./UI.xml#L1165:~:text=<ComplexType%20Name="-,PresentationVariantType,-")|\[PropertyPath\]|Properties that should always be included in the result of the queried collection<br>Properties in `RequestAtLeast` must occur either in the `$select` clause of an OData request or among the grouping properties in an `$apply=groupby((grouping properties),...)` clause of an aggregating OData request.
[SelectionFields](./UI.xml#L1188:~:text=<ComplexType%20Name="-,PresentationVariantType,-") *([Experimental](Common.md#Experimental))*|\[PropertyPath\]|Properties that should be presented for filtering a collection of entities. Can be provided inline or as a reference to a `UI.SelectionFields` annotation via Path.

<a name="SelectionVariantType"></a>
## [SelectionVariantType](./UI.xml#L1202:~:text=<ComplexType%20Name="-,SelectionVariantType,-")


Property|Type|Description
:-------|:---|:----------
[ID](./UI.xml#L1203:~:text=<ComplexType%20Name="-,SelectionVariantType,-")|String?|May contain identifier to reference this instance from an external context
[Text](./UI.xml#L1208:~:text=<ComplexType%20Name="-,SelectionVariantType,-")|String?|Name of the selection variant
[Parameters](./UI.xml#L1212:~:text=<ComplexType%20Name="-,SelectionVariantType,-")|\[[ParameterAbstract](#ParameterAbstract)\]|Parameters of the selection variant
[FilterExpression](./UI.xml#L1215:~:text=<ComplexType%20Name="-,SelectionVariantType,-")|String?|Filter string for query part of URL, without `$filter=`
[SelectOptions](./UI.xml#L1220:~:text=<ComplexType%20Name="-,SelectionVariantType,-")|\[[SelectOptionType](#SelectOptionType)\]|ABAP Select Options Pattern

<a name="ParameterAbstract"></a>
## [*ParameterAbstract*](./UI.xml#L1227:~:text=<ComplexType%20Name="-,ParameterAbstract,-")
Key property of a parameter entity type

**Derived Types:**
- [Parameter](#Parameter)
- [IntervalParameter](#IntervalParameter)

<a name="Parameter"></a>
## [Parameter](./UI.xml#L1230:~:text=<ComplexType%20Name="-,Parameter,-"): [ParameterAbstract](#ParameterAbstract)
Single-valued parameter

Property|Type|Description
:-------|:---|:----------
[PropertyName](./UI.xml#L1232:~:text=<ComplexType%20Name="-,Parameter,-")|PropertyPath|Path to a key property of a parameter entity type
[PropertyValue](./UI.xml#L1235:~:text=<ComplexType%20Name="-,Parameter,-")|PrimitiveType|Value for the key property

<a name="IntervalParameter"></a>
## [IntervalParameter](./UI.xml#L1239:~:text=<ComplexType%20Name="-,IntervalParameter,-"): [ParameterAbstract](#ParameterAbstract)
Interval parameter formed with a 'from' and a 'to' property

Property|Type|Description
:-------|:---|:----------
[PropertyNameFrom](./UI.xml#L1241:~:text=<ComplexType%20Name="-,IntervalParameter,-")|PropertyPath|Path to the 'from' property of a parameter entity type
[PropertyValueFrom](./UI.xml#L1244:~:text=<ComplexType%20Name="-,IntervalParameter,-")|PrimitiveType|Value for the 'from' property
[PropertyNameTo](./UI.xml#L1247:~:text=<ComplexType%20Name="-,IntervalParameter,-")|PropertyPath|Path to the 'to' property of a parameter entity type
[PropertyValueTo](./UI.xml#L1250:~:text=<ComplexType%20Name="-,IntervalParameter,-")|PrimitiveType|Value for the 'to' property

<a name="SelectOptionType"></a>
## [SelectOptionType](./UI.xml#L1255:~:text=<ComplexType%20Name="-,SelectOptionType,-")
List of value ranges for a single property

Exactly one of `PropertyName` and `DynamicPropertyName` must be present

Property|Type|Description
:-------|:---|:----------
[PropertyName](./UI.xml#L1258:~:text=<ComplexType%20Name="-,SelectOptionType,-")|PropertyPath?|Path to the property
[DynamicPropertyName](./UI.xml#L1270:~:text=<ComplexType%20Name="-,SelectOptionType,-")|AnnotationPath?|Dynamic property introduced by annotations for which value ranges are specified<br>If the annotation referenced by the annotation path does not apply to the same collection of entities as the one being filtered according to the `UI.SelectionVariant` annotation, this instance of `UI.SelectionVariant/SelectOptions` MUST be silently ignored. For an example, see the `UI.SelectionVariant` annotation in the [example](../examples/DynamicProperties-sample.xml).<br>Allowed terms:<br>- [AggregatedProperty](Analytics.md#AggregatedProperty)<br>- [CustomAggregate](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Aggregation.V1.md#CustomAggregate)
[Ranges](./UI.xml#L1284:~:text=<ComplexType%20Name="-,SelectOptionType,-")|\[[SelectionRangeType](#SelectionRangeType)\]|List of value ranges

<a name="SelectionRangeType"></a>
## [SelectionRangeType](./UI.xml#L1289:~:text=<ComplexType%20Name="-,SelectionRangeType,-")
Value range. If the range option only requires a single value, the value must be in the property Low

Property|Type|Description
:-------|:---|:----------
[Sign](./UI.xml#L1293:~:text=<ComplexType%20Name="-,SelectionRangeType,-")|[SelectionRangeSignType](#SelectionRangeSignType)|Include or exclude values
[Option](./UI.xml#L1296:~:text=<ComplexType%20Name="-,SelectionRangeType,-")|[SelectionRangeOptionType](#SelectionRangeOptionType)|Comparison operator
[Low](./UI.xml#L1299:~:text=<ComplexType%20Name="-,SelectionRangeType,-")|PrimitiveType|Single value or lower interval boundary
[High](./UI.xml#L1302:~:text=<ComplexType%20Name="-,SelectionRangeType,-")|PrimitiveType?|Upper interval boundary

<a name="SelectionRangeSignType"></a>
## [SelectionRangeSignType](./UI.xml#L1307:~:text=<EnumType%20Name="-,SelectionRangeSignType,-")


Member|Value|Description
:-----|----:|:----------
[I](./UI.xml#L1308:~:text=<EnumType%20Name="-,SelectionRangeSignType,-")|0|Inclusive
[E](./UI.xml#L1311:~:text=<EnumType%20Name="-,SelectionRangeSignType,-")|1|Exclusive

<a name="SelectionRangeOptionType"></a>
## [SelectionRangeOptionType](./UI.xml#L1316:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")
Comparison operator

Member|Value|Description
:-----|----:|:----------
[EQ](./UI.xml#L1318:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")|0|Equal to
[BT](./UI.xml#L1321:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")|1|Between
[CP](./UI.xml#L1324:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")|2|Contains pattern
[LE](./UI.xml#L1327:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")|3|Less than or equal to
[GE](./UI.xml#L1330:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")|4|Greater than or equal to
[NE](./UI.xml#L1333:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")|5|Not equal to
[NB](./UI.xml#L1336:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")|6|Not between
[NP](./UI.xml#L1339:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")|7|Does not contain pattern
[GT](./UI.xml#L1342:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")|8|Greater than
[LT](./UI.xml#L1345:~:text=<EnumType%20Name="-,SelectionRangeOptionType,-")|9|Less than

<a name="TextArrangementType"></a>
## [TextArrangementType](./UI.xml#L1412:~:text=<EnumType%20Name="-,TextArrangementType,-")


Member|Value|Description
:-----|----:|:----------
[TextFirst](./UI.xml#L1413:~:text=<EnumType%20Name="-,TextArrangementType,-")|0|Text is first, followed by the code/ID (e.g. in parentheses)
[TextLast](./UI.xml#L1416:~:text=<EnumType%20Name="-,TextArrangementType,-")|1|Code/ID is first, followed by the text (e.g. separated by a dash)
[TextSeparate](./UI.xml#L1419:~:text=<EnumType%20Name="-,TextArrangementType,-")|2|Code/ID and text are represented separately (code/ID will be shown and text can be visualized in a separate place)
[TextOnly](./UI.xml#L1422:~:text=<EnumType%20Name="-,TextArrangementType,-")|3|Only text is represented, code/ID is hidden (e.g. for UUIDs)

<a name="NoteType"></a>
## [NoteType](./UI.xml#L1439:~:text=<ComplexType%20Name="-,NoteType,-") *([Experimental](Common.md#Experimental))*


Property|Type|Description
:-------|:---|:----------
[Title](./UI.xml#L1441:~:text=<ComplexType%20Name="-,NoteType,-")|String?|Title of the note<br>The title of a note is hidden with an annotation `@UI.Note/Title/@UI.Hidden`, not with an annotation on the property targeted by `@UI.Note/Title`.<br>Can be annotated with:<br>- [Hidden](#Hidden)
[Content](./UI.xml#L1453:~:text=<ComplexType%20Name="-,NoteType,-")|String|Content of the note, as a string<br>The property targeted by `@UI.Note/Content` must be annotated with `Core.MediaType` and may be annotated with `Common.SAPObjectNodeTypeReference`. When it is tagged with `Core.IsLanguageDependent`, another property of the same entity type that is tagged with [`Common.IsLanguageIdentifier`](Common.md#IsLanguageIdentifier) determines the language of the note.<br>Can be annotated with:<br>- [MediaType](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#MediaType)<br>- [IsLanguageDependent](https://github.com/oasis-tcs/odata-vocabularies/blob/main/vocabularies/Org.OData.Core.V1.md#IsLanguageDependent)<br>- [SAPObjectNodeTypeReference](Common.md#SAPObjectNodeTypeReference)
[Type](./UI.xml#L1469:~:text=<ComplexType%20Name="-,NoteType,-")|String|A type used for grouping notes
[MaximalLength](./UI.xml#L1472:~:text=<ComplexType%20Name="-,NoteType,-")|Int32?|Type-specific maximal length of the content of the note
[MultipleNotes](./UI.xml#L1475:~:text=<ComplexType%20Name="-,NoteType,-")|Boolean|Whether the type allows multiple notes for one object

<a name="ImportanceType"></a>
## [ImportanceType](./UI.xml#L1483:~:text=<EnumType%20Name="-,ImportanceType,-")


Member|Value|Description
:-----|----:|:----------
[High](./UI.xml#L1484:~:text=<EnumType%20Name="-,ImportanceType,-")|0|High importance
[Medium](./UI.xml#L1487:~:text=<EnumType%20Name="-,ImportanceType,-")|1|Medium importance
[Low](./UI.xml#L1490:~:text=<EnumType%20Name="-,ImportanceType,-")|2|Low importance

<a name="DataFieldAbstract"></a>
## [*DataFieldAbstract*](./UI.xml#L1550:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")
Elementary building block that represents a piece of data and/or allows triggering an action

By using the applicable terms UI.Hidden, UI.Importance or HTML5.CssDefaults, the visibility, the importance and
          and the default css settings (as the width) of the data field can be influenced. 

**Derived Types:**
- [DataFieldForAnnotation](#DataFieldForAnnotation)
- *[DataFieldForActionAbstract](#DataFieldForActionAbstract)*
  - [DataFieldForAction](#DataFieldForAction)
  - [DataFieldForIntentBasedNavigation](#DataFieldForIntentBasedNavigation)
- [DataFieldForActionGroup](#DataFieldForActionGroup)
- [DataField](#DataField)
  - [DataFieldWithAction](#DataFieldWithAction)
  - [DataFieldWithIntentBasedNavigation](#DataFieldWithIntentBasedNavigation)
  - [DataFieldWithNavigationPath](#DataFieldWithNavigationPath)
  - [DataFieldWithUrl](#DataFieldWithUrl)
  - [DataFieldWithActionGroup](#DataFieldWithActionGroup)

Property|Type|Description
:-------|:---|:----------
[Label](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[Criticality](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[CriticalityRepresentation](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[IconUrl](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="CriticalityRepresentationType"></a>
## [CriticalityRepresentationType](./UI.xml#L1581:~:text=<EnumType%20Name="-,CriticalityRepresentationType,-")


Member|Value|Description
:-----|----:|:----------
[WithIcon](./UI.xml#L1582:~:text=<EnumType%20Name="-,CriticalityRepresentationType,-")|0|Criticality is represented with an icon
[WithoutIcon](./UI.xml#L1585:~:text=<EnumType%20Name="-,CriticalityRepresentationType,-")|1|Criticality is represented without icon, e.g. only via text color
[OnlyIcon](./UI.xml#L1588:~:text=<EnumType%20Name="-,CriticalityRepresentationType,-") *([Experimental](Common.md#Experimental))*|2|Criticality is represented only by using an icon

<a name="DataFieldForAnnotation"></a>
## [DataFieldForAnnotation](./UI.xml#L1594:~:text=<ComplexType%20Name="-,DataFieldForAnnotation,-"): [DataFieldAbstract](#DataFieldAbstract)
A structured piece of data described by an annotation

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[Target](./UI.xml#L1596:~:text=<ComplexType%20Name="-,DataFieldForAnnotation,-")|AnnotationPath|Target MUST reference an annotation of terms Communication.Contact, Communication.Address, UI.DataPoint, UI.Chart, UI.FieldGroup, or UI.ConnectedFields<br>Allowed terms:<br>- [Address](Communication.md#Address)<br>- [Contact](Communication.md#Contact)<br>- [Chart](#Chart)<br>- [ConnectedFields](#ConnectedFields)<br>- [DataPoint](#DataPoint)<br>- [FieldGroup](#FieldGroup)

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="DataFieldForActionAbstract"></a>
## [*DataFieldForActionAbstract*](./UI.xml#L1611:~:text=<ComplexType%20Name="-,DataFieldForActionAbstract,-"): [DataFieldAbstract](#DataFieldAbstract)
Triggers an action

**Derived Types:**
- [DataFieldForAction](#DataFieldForAction)
- [DataFieldForIntentBasedNavigation](#DataFieldForIntentBasedNavigation)

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[Inline](./UI.xml#L1613:~:text=<ComplexType%20Name="-,DataFieldForActionAbstract,-")|Boolean|Action should be placed close to (or even inside) the visualized term
[Determining](./UI.xml#L1616:~:text=<ComplexType%20Name="-,DataFieldForActionAbstract,-")|Boolean|Determines whether the action completes a process step (e.g. approve, reject).

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="DataFieldForAction"></a>
## [DataFieldForAction](./UI.xml#L1621:~:text=<ComplexType%20Name="-,DataFieldForAction,-"): [DataFieldForActionAbstract](#DataFieldForActionAbstract)
Triggers an OData action

The action is NOT tied to a data value (in contrast to [DataFieldWithAction](#DataFieldWithAction)).

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[*Inline*](./UI.xml#L1613:~:text=<ComplexType%20Name="-,DataFieldForActionAbstract,-")|Boolean|Action should be placed close to (or even inside) the visualized term
[*Determining*](./UI.xml#L1616:~:text=<ComplexType%20Name="-,DataFieldForActionAbstract,-")|Boolean|Determines whether the action completes a process step (e.g. approve, reject).
[Action](./UI.xml#L1624:~:text=<ComplexType%20Name="-,DataFieldForAction,-")|[ActionName](#ActionName)|Name of an Action, Function, ActionImport, or FunctionImport in scope
[InvocationGrouping](./UI.xml#L1627:~:text=<ComplexType%20Name="-,DataFieldForAction,-")|[OperationGroupingType?](#OperationGroupingType)|Expresses how invocations of this action on multiple instances should be grouped

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="OperationGroupingType"></a>
## [OperationGroupingType](./UI.xml#L1631:~:text=<EnumType%20Name="-,OperationGroupingType,-")


Member|Value|Description
:-----|----:|:----------
[Isolated](./UI.xml#L1632:~:text=<EnumType%20Name="-,OperationGroupingType,-")|0|Invoke each action in isolation from other actions
[ChangeSet](./UI.xml#L1635:~:text=<EnumType%20Name="-,OperationGroupingType,-")|1|Group all actions into a single change set

<a name="DataFieldForIntentBasedNavigation"></a>
## [DataFieldForIntentBasedNavigation](./UI.xml#L1640:~:text=<ComplexType%20Name="-,DataFieldForIntentBasedNavigation,-"): [DataFieldForActionAbstract](#DataFieldForActionAbstract)
Triggers intent-based UI navigation

The navigation intent is expressed as a Semantic Object and optionally an Action on that object.

It is NOT tied to a data value (in contrast to [DataFieldWithIntentBasedNavigation](#DataFieldWithIntentBasedNavigation)).

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[*Inline*](./UI.xml#L1613:~:text=<ComplexType%20Name="-,DataFieldForActionAbstract,-")|Boolean|Action should be placed close to (or even inside) the visualized term
[*Determining*](./UI.xml#L1616:~:text=<ComplexType%20Name="-,DataFieldForActionAbstract,-")|Boolean|Determines whether the action completes a process step (e.g. approve, reject).
[SemanticObject](./UI.xml#L1647:~:text=<ComplexType%20Name="-,DataFieldForIntentBasedNavigation,-")|String|Name of the Semantic Object
[Action](./UI.xml#L1650:~:text=<ComplexType%20Name="-,DataFieldForIntentBasedNavigation,-")|String?|Name of the Action on the Semantic Object. If not specified, let user choose which of the available actions to trigger.
[NavigationAvailable](./UI.xml#L1653:~:text=<ComplexType%20Name="-,DataFieldForIntentBasedNavigation,-")|Boolean|The navigation intent is for that user with the selected context and parameters available
[RequiresContext](./UI.xml#L1656:~:text=<ComplexType%20Name="-,DataFieldForIntentBasedNavigation,-")|Boolean|Determines whether a context needs to be passed to the target of this navigation.
[Mapping](./UI.xml#L1659:~:text=<ComplexType%20Name="-,DataFieldForIntentBasedNavigation,-")|\[[SemanticObjectMappingType](Common.md#SemanticObjectMappingType)\]|Maps properties of the annotated entity type to properties of the Semantic Object

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="DataFieldForActionGroup"></a>
## [DataFieldForActionGroup](./UI.xml#L1664:~:text=<ComplexType%20Name="-,DataFieldForActionGroup,-"): [DataFieldAbstract](#DataFieldAbstract) *([Experimental](Common.md#Experimental))*
Collection of OData actions and intent based navigations

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[Actions](./UI.xml#L1667:~:text=<ComplexType%20Name="-,DataFieldForActionGroup,-")|\[[DataFieldForActionAbstract](#DataFieldForActionAbstract)\]|Collection of data fields that refer to actions or intent based navigations

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="DataField"></a>
## [DataField](./UI.xml#L1672:~:text=<ComplexType%20Name="-,DataField,-"): [DataFieldAbstract](#DataFieldAbstract)
A piece of data

**Derived Types:**
- [DataFieldWithAction](#DataFieldWithAction)
- [DataFieldWithIntentBasedNavigation](#DataFieldWithIntentBasedNavigation)
- [DataFieldWithNavigationPath](#DataFieldWithNavigationPath)
- [DataFieldWithUrl](#DataFieldWithUrl)
- [DataFieldWithActionGroup](#DataFieldWithActionGroup)

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[Value](./UI.xml#L1674:~:text=<ComplexType%20Name="-,DataField,-")|Untyped|The data field's value

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="DataFieldWithAction"></a>
## [DataFieldWithAction](./UI.xml#L1701:~:text=<ComplexType%20Name="-,DataFieldWithAction,-"): [DataField](#DataField)
A piece of data that allows triggering an OData action

The action is tied to a data value. This is in contrast to [DataFieldForAction](#DataFieldForAction) which is not tied to a specific data value.

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[Value](./UI.xml#L1704:~:text=<ComplexType%20Name="-,DataFieldWithAction,-")|PrimitiveType|The data field's value
[Action](./UI.xml#L1705:~:text=<ComplexType%20Name="-,DataFieldWithAction,-")|[ActionName](#ActionName)|Name of an Action, Function, ActionImport, or FunctionImport in scope

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="DataFieldWithIntentBasedNavigation"></a>
## [DataFieldWithIntentBasedNavigation](./UI.xml#L1710:~:text=<ComplexType%20Name="-,DataFieldWithIntentBasedNavigation,-"): [DataField](#DataField)
A piece of data that allows triggering intent-based UI navigation

The navigation intent is expressed as a Semantic Object and optionally an Action on that object.

It is tied to a data value which should be rendered as a hyperlink.
This is in contrast to [DataFieldForIntentBasedNavigation](#DataFieldForIntentBasedNavigation) which is not tied to a specific data value.

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[Value](./UI.xml#L1718:~:text=<ComplexType%20Name="-,DataFieldWithIntentBasedNavigation,-")|PrimitiveType|The data field's value
[SemanticObject](./UI.xml#L1719:~:text=<ComplexType%20Name="-,DataFieldWithIntentBasedNavigation,-")|String|Name of the Semantic Object
[Action](./UI.xml#L1722:~:text=<ComplexType%20Name="-,DataFieldWithIntentBasedNavigation,-")|String?|Name of the Action on the Semantic Object. If not specified, let user choose which of the available actions to trigger.
[Mapping](./UI.xml#L1725:~:text=<ComplexType%20Name="-,DataFieldWithIntentBasedNavigation,-")|\[[SemanticObjectMappingType](Common.md#SemanticObjectMappingType)\]|Maps properties of the annotated entity type to properties of the Semantic Object

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="DataFieldWithNavigationPath"></a>
## [DataFieldWithNavigationPath](./UI.xml#L1730:~:text=<ComplexType%20Name="-,DataFieldWithNavigationPath,-"): [DataField](#DataField)
A piece of data that allows navigating to related data

It should be rendered as a hyperlink

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[Value](./UI.xml#L1733:~:text=<ComplexType%20Name="-,DataFieldWithNavigationPath,-")|PrimitiveType|The data field's value
[Target](./UI.xml#L1734:~:text=<ComplexType%20Name="-,DataFieldWithNavigationPath,-")|NavigationPropertyPath|Contains either a navigation property or a term cast, where term is of type Edm.EntityType or a concrete entity type or a collection of these types

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="DataFieldWithUrl"></a>
## [DataFieldWithUrl](./UI.xml#L1741:~:text=<ComplexType%20Name="-,DataFieldWithUrl,-"): [DataField](#DataField)
A piece of data that allows navigating to other information on the Web

It should be rendered as a hyperlink

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[Value](./UI.xml#L1744:~:text=<ComplexType%20Name="-,DataFieldWithUrl,-")|PrimitiveType|The data field's value
[Url](./UI.xml#L1745:~:text=<ComplexType%20Name="-,DataFieldWithUrl,-")|URL|Target of the hyperlink<br>Can be annotated with:<br>- [LinkTarget](HTML5.md#LinkTarget)
[UrlContentType](./UI.xml#L1754:~:text=<ComplexType%20Name="-,DataFieldWithUrl,-")|MediaType?|Media type of the hyperlink target, e.g. `video/mp4`

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="DataFieldWithActionGroup"></a>
## [DataFieldWithActionGroup](./UI.xml#L1760:~:text=<ComplexType%20Name="-,DataFieldWithActionGroup,-"): [DataField](#DataField) *([Experimental](Common.md#Experimental))*
Collection of OData actions and intent based navigations

Property|Type|Description
:-------|:---|:----------
[*Label*](./UI.xml#L1565:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|String?|A short, human-readable text suitable for labels and captions in UIs
[*Criticality*](./UI.xml#L1569:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityType?](#CriticalityType)|Criticality of the data field value
[*CriticalityRepresentation*](./UI.xml#L1572:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|[CriticalityRepresentationType?](#CriticalityRepresentationType)|Decides if criticality is visualized in addition by means of an icon
[*IconUrl*](./UI.xml#L1575:~:text=<ComplexType%20Name="-,DataFieldAbstract,-")|URL?|Optional icon
[Value](./UI.xml#L1763:~:text=<ComplexType%20Name="-,DataFieldWithActionGroup,-")|PrimitiveType|The data field's value
[Actions](./UI.xml#L1764:~:text=<ComplexType%20Name="-,DataFieldWithActionGroup,-")|\[[DataField](#DataField)\]|Collection of data fields that are either [DataFieldWithAction](#DataFieldWithAction), [DataFieldWithIntentBasedNavigation](#DataFieldWithIntentBasedNavigation), [DataFieldWithNavigationPath](#DataFieldWithNavigationPath), or [DataFieldWithUrl](#DataFieldWithUrl)

**Applicable Annotation Terms:**

- [Hidden](#Hidden)
- [Importance](#Importance)
- [PartOfPreview](#PartOfPreview)
- [CssDefaults](HTML5.md#CssDefaults)
- [FieldControl](Common.md#FieldControl)

<a name="RecommendationStateType"></a>
## [RecommendationStateType](./UI.xml#L1802:~:text=<TypeDefinition%20Name="-,RecommendationStateType,-")
**Type:** Byte

Indicates whether a field contains or has a recommended value

Editable fields for which a recommendation has been pre-filled or that have recommendations that differ from existing human input need to be highlighted.

Allowed Value|Description
:------------|:----------
[0](./UI.xml#L1809:~:text=<TypeDefinition%20Name="-,RecommendationStateType,-")|regular - with human or default input, no recommendation
[1](./UI.xml#L1813:~:text=<TypeDefinition%20Name="-,RecommendationStateType,-")|highlighted - without human input and with recommendation
[2](./UI.xml#L1817:~:text=<TypeDefinition%20Name="-,RecommendationStateType,-")|warning - with human or default input and with recommendation

<a name="RecommendationListType"></a>
## [RecommendationListType](./UI.xml#L1832:~:text=<ComplexType%20Name="-,RecommendationListType,-")
Reference to a recommendation list

A recommendation consists of one or more values for editable fields plus a rank between 0.0 and 9.9, with 9.9 being the best recommendation.

Property|Type|Description
:-------|:---|:----------
[CollectionPath](./UI.xml#L1837:~:text=<ComplexType%20Name="-,RecommendationListType,-")|String|Resource path of a collection of recommended values
[RankProperty](./UI.xml#L1840:~:text=<ComplexType%20Name="-,RecommendationListType,-")|String|Name of the property within the collection of recommended values that describes the rank of the recommendation
[Binding](./UI.xml#L1843:~:text=<ComplexType%20Name="-,RecommendationListType,-")|\[[RecommendationBinding](#RecommendationBinding)\]|List of pairs of a local property and recommended value property

<a name="RecommendationBinding"></a>
## [RecommendationBinding](./UI.xml#L1848:~:text=<ComplexType%20Name="-,RecommendationBinding,-")


Property|Type|Description
:-------|:---|:----------
[LocalDataProperty](./UI.xml#L1849:~:text=<ComplexType%20Name="-,RecommendationBinding,-")|PropertyPath|Path to editable property for which recommended values exist
[ValueListProperty](./UI.xml#L1852:~:text=<ComplexType%20Name="-,RecommendationBinding,-")|String|Path to property in the collection of recommended values. Format is identical to PropertyPath annotations.

<a name="ActionName"></a>
## [ActionName](./UI.xml#L1876:~:text=<TypeDefinition%20Name="-,ActionName,-")
**Type:** String

Name of an Action, Function, ActionImport, or FunctionImport in scope

Possible values are
        
- Namespace-qualified name of an action or function (`foo.bar`)
- Namespace-qualified name of an action or function followed by parentheses with the parameter signature to identify a specific overload, like in an [annotation target](https://docs.oasis-open.org/odata/odata-csdl-xml/v4.01/odata-csdl-xml-v4.01.html#sec_Target) (`foo.bar(baz.qux)`)
- Simple name of an action import or function import of the annotated service (`quux`)
- Namespace-qualified name of an entity container, followed by a slash and the simple name of an action import or function import in any referenced schema (`foo.corge/quux`)
