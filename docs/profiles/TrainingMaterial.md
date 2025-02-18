# TrainingMaterial profile

## Description
A specification for describing training materials in life sciences. The Life Science Training Materials specification provides a way to describe bioscience training material on the World Wide Web. It defines a set of metadata and vocabularies, built on top of existing technologies and standards, that can be used to represent events in Web pages and applications. The goal of the specification is to make it easier to discover, exchange and integrate life science training material information across the Internet.<h4>Summary of Changes</h4> No changes since 0.9-DRAFT of the TrainingMaterials profile. Version: 1.0-RELEASE

## Minimum properties

| Name              | Description                          | Cardinality |
| :---------------- | :----------------------------------- | :---------- |
| [description](https://schema.org/description) |  A description of the item.  | one |
| [keywords](https://schema.org/keywords) |  Keywords or tags used to describe this content. Multiple entries in a keywords list are typically delimited by commas.  | many |
| [name](https://schema.org/name) |  The name of the item.  | one |
| [conformsTo](None) | This is used to state the Bioschemas profile that the markup relates to. The identifier can be the url for the version of this bioschemas class on github: https://github.com/BioSchemas/specifications/blob/master/TrainingMaterial/jsonld/TrainingMaterial_v1.0-RELEASE.json  | many |


## Recommended properties

| Name              | Description                          | Cardinality |
| :---------------- | :----------------------------------- | :---------- |
| [about](https://schema.org/about) | The subject of this Training Material. Use the DefinedTerm type to add a  controlled vocabulary term to describe the topic (such as from the EDAM  ontology) The subject matter of the content.  Inverse property: subjectOf.  | many |
| [abstract](https://schema.org/abstract) |  An abstract is a short description that summarizes a CreativeWork.  | one |
| [audience](https://schema.org/audience) | A succinct description of the intended target audience for your materials: e.g., graduates, postgraduates, clinicians. An intended audience, i.e. a group for whom something was created. Supersedes serviceAudience.  | many |
| [author](https://schema.org/author) |  Those involved in the preparation, creation and/or presentation of the published work, specifically writing the initial draft The author of this content or rating. Please note that author is special in that HTML 5 provides a special mechanism for indicating authorship via the rel tag. That is equivalent to this and may be used interchangeably.  | many |
| [competencyRequired](https://schema.org/competencyRequired) |  Knowledge, skill, ability or personal attribute that must be demonstrated by a person or other entity in order to do something such as earn an Educational Occupational Credential or understand a LearningResource.  | many |
| [educationalLevel](https://schema.org/educationalLevel) | The students level of ability in the topic being taught. Examples of skill levels include 'beginner', 'intermediate' or 'advanced'. The level in terms of progression through an educational or training context. Examples of educational levels include 'beginner', 'intermediate' or 'advanced', and formal sets of level indicators.  | one |
| [identifier](https://schema.org/identifier) | An identifier for this resource such as a DOI or compact URI  The identifier property represents any kind of identifier for any kind of Thing, such as ISBNs, GTIN codes, UUIDs etc. Schema.org provides dedicated properties for representing many of these, either as textual strings or as URL (URI) links. See background notes for more details.  | many |
| [inLanguage](https://schema.org/inLanguage) | Defaults to English if not specified. Please choose a value from [IETF BCP 47 standard](http://tools.ietf.org/html/bcp47). You can add multiple languages if the Training Material offers different translations The language of the content or performance or used in an action. Please use one of the language codes from the IETF BCP 47 standard. See also availableLanguage. Supersedes language.  | many |
| [learningResourceType](https://schema.org/learningResourceType) | This may include things such as video lecture, e-Learning module, or tutorial. The predominant type or kind characterizing the learning resource. For example, 'presentation', 'handout'.  | many |
| [license](https://schema.org/license) | If there is a licence it must be added. A license document that applies to this content, typically indicated by URL.  | many |
| [mentions](https://schema.org/mentions) | Datasets, tools, technologies, entities etc, which are referred to by this training material or actively used in this training material. Indicates that the CreativeWork contains a reference to, but is not necessarily about a concept.  | many |
| [teaches](https://schema.org/teaches) |  The item being described is intended to help a person learn the competency or learning outcome defined by the referenced term.  | many |
| [timeRequired](https://schema.org/timeRequired) | The estimated time it takes to work through this resource.  Please specify in [ISO 8601 duration format](https://en.wikipedia.org/wiki/ISO_8601). Approximate or typical time it takes to work with or through this learning resource for the typical intended target audience, e.g. 'PT30M', 'PT1H25M'.  | one |
| [url](https://schema.org/url) | The preferred URL of the Training Material. You must provide this value if it is known. URL of the item.  | one |


## Optional properties
| Name              | Description                          | Cardinality |
| :---------------- | :----------------------------------- | :---------- |
| [accessibilitySummary](https://schema.org/accessibilitySummary) |  A human-readable summary of specific accessibility features or deficiencies, consistent with the other accessibility metadata but expressing subtleties such as "short descriptions are present but long descriptions will be needed for non-visual users" or "short descriptions are present and no long descriptions are needed."  | one |
| [contributor](https://schema.org/contributor) | Contributors are those that made non-authorship contributions e.g. critical review, commentary or revision A secondary contributor to the CreativeWork or Event.  | many |
| [creativeWorkStatus](https://schema.org/creativeWorkStatus) | The status of a training material. If this is not filled in it will be regarded as Active.  Options are 'Active', 'Under development', and 'Archived'. The status of a creative work in terms of its stage in a lifecycle. Example terms include Incomplete, Draft, Published, Obsolete. Some organizations define a set of terms for the stages of their publication lifecycle.  | one |
| [dateCreated](https://schema.org/dateCreated) |  The date on which the CreativeWork was created or the item was added to a DataFeed.  | one |
| [dateModified](https://schema.org/dateModified) |  The date on which the CreativeWork was most recently modified or when the item's entry was modified within a DataFeed.  | one |
| [datePublished](https://schema.org/datePublished) |  Date of first broadcast/publication.  | one |
| [hasPart](https://schema.org/hasPart) | A sub-training material or externally referenced training material  Indicates an item or CreativeWork that is part of this item, or CreativeWork (in some sense).  Inverse property: isPartOf.  | many |
| [isPartOf](https://schema.org/isPartOf) | The Course this Training Material was/will be used in. Or a training material this training material is a part of (for example, if this is a module in a book, isPartOf can describe the book).  Inverse property: hasPart  If this varies in CourseInstances, use the workFeatured property  Indicates an item or CreativeWork that this item, or CreativeWork (in some sense), is part of.  Inverse property: hasPart.  | many |
| [recordedAt](https://schema.org/recordedAt) | The course instance or event where this training material was or will be featured.   Use isPartOf to refer to a Course, unless this training material is unique to a specific Course Instance. The Event where the CreativeWork was recorded. The CreativeWork may capture all or part of the event. Inverse property: recordedIn.  | many |
| [version](https://schema.org/version) | If this training material is versioned, its strongly recommended you use this property to list the version being displayed The version of the CreativeWork embodied by a specified resource.  | one |
| [workTranslation](https://schema.org/workTranslation) |  A work that is a translation of the content of this work. e.g. 西遊記 has an English workTranslation “Journey to the West”,a German workTranslation “Monkeys Pilgerfahrt” and a Vietnamese translation Tây du ký bình khảo. Inverse property: translationOfWork.  | many |
