# Basic Language Archive Metadata (Bundle User)

> **Blam** The standard blasty noise. The power of the blam can sometimes be measured by the size of the word when it is written, or by the number of exclamation marks at the end of the word.
> 			[urban dictionary](http://www.urbandictionary.com/define.php?term=blam&defid=305474)

Basic Language Archive Metadata (BLAM) is designed to provide basic metadata for language repositories. The metadata scheme maximises discoverability and user oriented information without a proliferation of data fields or work for the data producer. Basic Language Archive Metadata is a suite of [CMDI](https://www.clarin.eu/content/component-metadata) profiles and currently consist of two pairs of profiles: 

* BLAM Bundle Repository: [documentation](https://github.com/fxru/blam-metadata/blob/master/BLAMBundleRepository.md), [profile](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1475136016193&registrySpace=public)
* BLAM Bundle User: described in this document [below](#blam-bundle-user) (outdated)
* BLAM Collection Repository: [documentation](https://github.com/fxru/blam-metadata/blob/master/BLAMCollectionRepository.md), [profile](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1487686159207&registrySpace=public)

BLAM Bundle contains information about bundles as provided by the repository. Data producers are asked to submit a subset of this information during ingest. The BLAM Bundle User profile defines this subset of 40 data fields. The separate definition of the BLAM Bundle User profile enhances the usability for data producers and can be validated independently from the more comprehensive BLAM Bundle Repository profile. The Basic Language Archive Metadata Bundle User profile is intended to be the primary source of user input for BLAM Bundle Repository. However, BLAM Bundle Repository is designed to allow automatic import of information from other metadata formats. The formats actively considered are: 

* IMDI Metadata Format: [ISLE Meta Data Initative, Version 3.0.4 (2003)](https://tla.mpi.nl/imdi-metadata/)
* CMDI imdi-session-profile: [clarin.eu:cr1:p_1271859438204](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1271859438204&registrySpace=public)
* CMDI ELDP_Bundle: [clarin.eu:cr1:p_1407745711992](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1407745711992&registrySpace=public)
* CMDI lat-session: [clarin.eu:cr1:p_1407745712035](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1407745712035&registrySpace=public)  

BLAM Bundle is designed with a focus on discoverability and display. Data producers can submit additional metadata information to document their data and their research. The preferred format are other CMDI profiles or comparably standardized metadata formats.

The data fields of BLAM Bundle were defined to facilitate interoperability with metacatalogues, in particular [DataCite](https://search.datacite.org/), [OLAC](http://search.language-archives.org/), and [VLO](https://vlo.clarin.eu/).

* OLAC metadata: [specifications](http://www.language-archives.org/OLAC/metadata.html), [usage](http://www.language-archives.org/NOTE/usage.html)
* DataCite Metadata: [Schema 4.0](https://schema.datacite.org/meta/kernel-4.0/)
* CLARIN VLO facets: [facets mapping](https://lux17.mpi.nl/isocat/clarin/vlo/mapping/index.html)

Recommended tools to create BLAM metadata are [CMDI Maker](http://cmdi-maker.uni-koeln.de/), [COMEDI](http://clarino.uib.no/comedi/), and [Arbil](https://tla.mpi.nl/tools/tla-tools/arbil/).

BLAM! &#x1F4A5; That’s it, enjoy documenting your data!

## BLAM-Bundle-User

**Description:** The Basic Language Archive Metadata Bundle profile aims to provide a basic metadata profile for language repositories. The profiles cover fundamental domain specific, but project independent, descriptive metadata as well as basic administrative and structural metadata. BLAM Bundle focusses on discoverability and human-readable display without a proliferation of data fields and work for the data producer.

* [BundleGeneralInfo](#bundlegeneralinfo)
* [BundlePublicationInfo](#bundlepublicationinfo)
* [ProjectInfo](#projectinfo)
* [BundleDataInfo](#bundledatainfo)
* [BundleAdministrativeInfo](#bundleadministrativeinfo)
* [BundleStructuralInfo](#bundlestructuralinfo)

### BundleGeneralInfo
**Description:** BundleGeneralInfo contains general descriptive metadata about the bundle.

	Number of occurrences:	1-1

- [BundleDisplayTitle](#bundledisplaytitle) &#x1F4A5;
- [BundleDescription](#bundledescription) &#x1F4A5;
- [BundleKeywords](#bundlekeywords)
	- [BundleKeyword](#bundlekeyword) &#x1F4A5;
- [BundleObjectLanguages](#bundleobjectlanguages)
	- [BundleObjectLanguage](#bundleobjectlanguage)
		- [ObjectLanguageDisplayName](#objectlanguagedisplayname) &#x1F4A5;
		- [ObjectLanguageGlottologCode](#objectlanguageglottologcode) &#x1F4A5;
- [BundleRecordingDate](#bundlerecordingdate) &#x1F4A5;
- [BundleLocation](#bundlelocation)
	- [BundleGeoLocation](#bundlegeolocation) &#x1F4A5;
	- [BundleLocationDisplayName](#bundlelocationdisplayname) &#x1F4A5;
	- [BundleRegionDisplayName](#bundleregiondisplayname) &#x1F4A5; 
	- [BundleCountryDisplayName](#bundlecountrydisplayname)  &#x1F4A5;

[Back to Top](#blam-bundle-repository)

#### BundleDisplayTitle 
**Description:** &#x1F4A5; The BundleDisplayTitle element provides a human readable name of the bundle. It should contain a meaningful and recognisable title for the bundle. The content of the BundleDisplayTitle element will be used as the human readable identifier in interfaces. Data producers can provide BundleDisplayTitle values for multiple interface languages. This field will be used as the human readable identifier for the bundle in citation and interfaces.

	Discovery:					searchable
	Display:					page, list
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	resource title
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2545_d873f2ab-2a2f-29d6-a9ab-260cde57f227

	VLO Facet: 					name
	OLAC (DCMI):				http://purl.org/dc/terms/title
	DataCite:        			Title
	IMDI Element:               //Session/Title
	ELDP-CMDI Element:			ELDP_Bundle:Title
	IMDI-CMDI Element:	
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleDescription 
**Description:** &#x1F4A5; The BundleDescription element provides a human readable description of the bundle. It should contain a description of the content of the collection. The content of the BundleDescription element will be used as the human readable description in interfaces. Its content can be queried by repositories for free-text metadata search. Data producers can provide BundleDescription values for multiple interface languages.

	Discovery:					searchable
	Display:					page, list (excerpt)
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	description
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2520_9eeedfb4-47d3-ddee-cfcb-99ac634bf1db

	VLO Facet: 					description
	OLAC (DCMI):				http://purl.org/dc/terms/description
	DataCite:        			Description
	IMDI Element:               //Session/Description
	ELDP-CMDI Element:          ELDP_Bundle:Description
	IMDI-CMDI Element:
	lat-session:				

#### BundleKeywords
**Description:** BundleKeywords should be used to describe the content and nature of data to enhance the discoverability and facilitate finer granularity for searches and browsing of the data. Repositories can use keyword metadata to define meaningful subsets of the data and provide a better browsing experience. 

								Number of occurrences:	0-1

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleKeyword 
**Description:** &#x1F4A5; BundleKeyword should contain a single keyword or a keyphrase and should be used to describe the content and nature of data to enhance the discoverability and facilitate finer granularity for searches and browsing of the data. Repositories can use keyword metadata to define meaningful subsets of the data and provide a better browsing experience. 

	Discovery:					searchable, browsing facet
	Display:					page, list
	User provided:				yes		

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	metadata tag
	CCR URI:               		http://hdl.handle.net/11459/CCR_C-5436_6ab57c2c-5f8d-3561-6db6-d75da23d2637

	VLO Facet: 					keywords
	OLAC (DCMI):				—
	DataCite:        			Subject
	IMDI Element:               various (closest match: //Session/Keys/*)
	ELDP-CMDI Element:          CCR:ELDP_Bundle:Keywords:Keyword
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleObjectLanguages
**Description:** BundleObjectLanguages contains information about the language or languages that are the object of the resource. 

	Number of occurrences:		1-1

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleObjectLanguage
**Description:** BundleObjectLanguage contains information about the language that is the object of the resource.

	Number of occurrences:		1-unbounded

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### ObjectLanguageDisplayName
**Description:** &#x1F4A5; The ObjectLanguageDisplayName element contains the name of the object language in the version recommended by the data producer. Repositories should treat the name provided by this element as the primary language name when displaying the metadata in relation to this particular data set (e.g. collection or bundle). The repository may use alternative names provided by services such as Glottolog or Ethnologue to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no language name is given for a particular interface language. Data producers can provide LanguageDisplayName values for multiple interface languages. 

	Discovery:					searchable, browsing facet
	Display:					page, list
	User provided:				yes		

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	Language Name
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d

	VLO Facet: 					languageCode
	OLAC (DCMI):				http://purl.org/dc/terms/language
	DataCite:        			Language
	IMDI Element:               //Session/MDGroup/Content/Languages/Language/Name
	ELDP-CMDI Element:          
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### ObjectLanguageGlottologCode
**Description:**  &#x1F4A5; The ObjectLanguageGlottologCode element contains the Glottolog code for the object language as provided by glottolog.org.

	Discovery:					searchable
	Display:					page
	User provided:				yes	

	ValueScheme:				[a-z]{4}[0-9]{4}
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	
	CCR URI:                

	VLO Facet: 
	OLAC (DCMI):
	DataCite:        
	IMDI Element:               
	ELDP-CMDI Element:          
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleRecordingDate
**Description:** &#x1F4A5; The BundleRecordingDate element contains the date at which a recording occured. The date must be provided conforming to ISO 8601 in the form YYYY-MM-DD, YYYY-MM, or YYYY.

	Discovery:					searchable, browsing facet (collection)
	Display:					page
	User provided:				yes		

	ValueScheme:				([0-9]{4}(-(0[1-9]|1[012])(-([0-2][0-9]|3[01]))?)?)|Unknown
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	Date of Recording
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-5257_6572a4ea-cc70-c721-bbd8-2f6c28cc71a1

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			date subType:created
	IMDI Element:               //Session/date
	ELDP-CMDI Element:          
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleLocation
**Description:** BundleLocation contains information about the most relevant or salient location in relation to the data contained in the bundle. The default location would be the location of recording. However, any other location vowed as most relevant to the data can be set as the BundleLocation. The information provided in the component is intended for discoverability and display purposes. Detailed documentation of geographic information should be outsourced into an additional metadata file.

	Number of occurrences:		1-1

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleGeoLocation
**Description:** &#x1F4A5; The BundleGeoLocation element contains a geographical coordinates for a location point in the form *LATITUDE,LONGITUDE* as decimal degrees (e.g. 50.926735,6.930392).

	Discovery:					browsing facet (map)
	Display:					page, list (both map)
	User provided:				yes				

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	geographical coordinates
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2523_283c7b54-06ed-3d6c-4bb0-c8a79a8236fd

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			GeoLocation:geoLocationPoint
	IMDI Element:               —
	ELDP-CMDI Element:          
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleLocationDisplayName
**Description:** &#x1F4A5; The BundleLocationDisplayName element contains the name of a location in the version recommended by the data producer. Repositories should treat the name provided by this element as the primary location name when displaying the metadata in relation to this particular data set (e.g. collection or bundle).The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance the browsing and search experience. The repository may also translate the name into other languages if no BundleLocationDisplayName name is given for a particular interface language. 

	Discovery:					searchable, browsing facet
	Display:					page
	User provided:				yes		

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	place name
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-5580_03e458f2-f873-8645-76eb-40e001b6c1ac

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        
	IMDI Element:               //Session/MDGroup/Location/Address
	ELDP-CMDI Element:          
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleRegionDisplayName
**Description:** &#x1F4A5; The BundleRegionDisplayName element optionally contains the name of an administrative subdivision such as state, province, or any other culturally salient unit in the version recommended by the data producer. The data producer can decided which level of subdivision is relevant and will improve discoverability. Repositories should treat the name provided by this element as the primary location name when displaying the metadata in relation to this particular data set (e.g. collection or bundle). The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no RegionDisplayName value is given for a particular interface language.

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	location region
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2533_fa6e1812-e29b-3cf6-e15a-50aa34b9be68

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			—
	IMDI Element:               //Session/MDGroup/Location/Region
	ELDP-CMDI Element:          
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleCountryDisplayName
**Description:** &#x1F4A5; The BundleCountryDisplayName element contains the name of the country to which the location belongs in the version recommended by the data producer. Repositories should treat the name provided by this element as the primary country name when displaying the metadata in relation to this particular data set (e.g. collection or bundle). The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no BundleCountryDisplayName name is given for a particular interface language. Data producers can provide BundleCountryDisplayName values for multiple interface languages.  

	Discovery:					searchable
	Display:					page
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	location country
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2532_d004b0a6-fd1d-3ca3-abf1-1e6aeb3e37b2

	VLO Facet: 					country
	OLAC (DCMI):				—
	DataCite:        			—
	IMDI Element:               //Session/MDGroup/Location/Country
	ELDP-CMDI Element:          
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

### BundlePublicationInfo
**Description:** The BundlePublicationInfo component contains metadata pertaining the publication of the resource. The information provided in this component is used for display and in particular to generate bibliographical references to the resource.

	Number of occurrences:		1-1

- [BundleCreators](#bundlecreators) 
	- [BundleCreator](#bundlecreator)
		- [CreatorDisplayName](#creatordisplayname) &#x1F4A5;
		- [CreatorNameIdentifier](#creatornameidentifier) &#x1F4A5;
		- [CreatorAffiliation](#creatoraffiliation) &#x1F4A5;
- [BundlePublicationYear](#bundlepublicationyear) &#x1F4A5;
- [BundleContributors](#bundlecontributors)
	- [BundleContributor](#bundlecontributor)
		- [ContributorDisplayName](#contributordisplayname) &#x1F4A5;
		- [ContributorNameIdentifier](#contributornameidentifier) &#x1F4A5;
		- [ContributorAffiliation](#contributoraffiliation) &#x1F4A5;

[Back to Top](#blam-bundle-repository)

#### BundleCreators
**Description:** The BundleCreator component contains information about the creator or creators of the resource. BundleCreators are treated as creators of the resource and thus similar to authors in respect to quotation, references, and metadata display. Other individuals involved in the production or processing of the resource should be added as [BundleContributors](bundlecontributors).

	Number of occurrences:		1-1

[Back to Top](#blam-bundle-repository) | [Back to BundlePublicationInfo](#bundlepublicationinfo)

##### BundleCreator
**Description:** The BundleCreator component contains information about the creator of the resource. 

	Number of occurrences:		1-unbounded

[Back to Top](#blam-bundle-repository) | [Back to BundlePublicationInfo](#bundlepublicationinfo)

###### CreatorDisplayName
**Description:** &#x1F4A5; The CreatorDisplayName element contains the name of the creator in a form that lends itself to alphabetical sorting. The value of this field can be used to generate a bibliographical citation reference for the resource. This usage should guide the formatting. The data producer determines what is the proper order of names for an alphabetically sorted list.

	Discovery:					searchable
	Display:					page
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	creator
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-6836_d35e73a8-ec72-d3c4-e39a-4b0fefd32cdc

	VLO Facet: 					—
	OLAC (DCMI):				contributor
	DataCite:        			creator
	IMDI Element:               //Session/MDGroup/Actors/Actor/FullName[../Role/contains(text(), 'Researcher') or ../Role/contains(text(), 'Depositor')]
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundlePublicationInfo](#bundlepublicationinfo)

###### CreatorNameIdentifier
**Description:** &#x1F4A5; The CreatorNameIdentifier contains an URI that uniquely identifies the creator according to an established scheme. ORCID and INSI are considered best practices. An email address in the form of an mailto URI is a fallback.
**Attribute** *identifierType*: ORCID and ISNI are considered best practices. An email address in the form of an mailto URI is a fallback. *Values*: ORCID, ISNI, Email, Other

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				anyURI
	Number of occurrences:  	0-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			Creator:nameIdentifier
	IMDI Element:               —
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) |  [Back to BundlePublicationInfo](#bundlepublicationinfo)

###### CreatorAffiliation
**Description:** &#x1F4A5; The CreatorAffiliation contains the organisational or institutional affiliation of the creator as provided by the depositor.

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			Creator:affiliation
	IMDI Element:               —
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) |  [Back to BundlePublicationInfo](#bundlepublicationinfo)

#### BundlePublicationYear
**Description:** &#x1F4A5; BundlePublicationYear contains the year of publication in the form YYYY conforming to ISO 8601. The default value is the ingest date into the repository unless an embargo has been set for the resource. In that case the end year of the embargo is taken as the year of publication. For legacy data, the  value of BundlePublicationDate can be set to a point before the ingest. The value of this field should be used to generate a bibliographical citation reference for the resource. 

	Discovery:					searchable, browsing facet
	Display:					page
	User provided:				yes

	ValueScheme:				gYear
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	publication date
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2538_8b697452-7ef3-9fce-ccf9-a7f344f11317

	VLO Facet: 					—
	OLAC (DCMI):				Date:dcterms:available
	DataCite:        			PublicationYear
	IMDI Element:               —
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) |  [Back to BundlePublicationInfo](#bundlepublicationinfo)

#### BundleContributors
**Description:** The BundleContributors component contains information about the creator or creators of the resource. BundleCreators are treated as creators of the resource and thus similar to authors in respect to quotation, references, and metadata display. Other individuals involved in the production or processing of the resource should be added as [BundleContributors](bundlecontributors).

	Number of occurrences:		0-1

[Back to Top](#blam-bundle-repository) | [Back to BundlePublicationInfo](#bundlepublicationinfo)

##### BundleContributor
**Description:** The BundleContributor component contains information about a contributor to the resource. 

	Number of occurrences:		1-unbounded

[Back to Top](#blam-bundle-repository) | [Back to BundlePublicationInfo](#bundlepublicationinfo)

###### ContributorDisplayName
**Description:** &#x1F4A5; The CreatorDisplayName element contains the name of the creator. The data producer determines what is the proper order of names.

	Discovery:					searchable
	Display:					page
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	creator
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-6836_d35e73a8-ec72-d3c4-e39a-4b0fefd32cdc

	VLO Facet: 					—
	OLAC (DCMI):				contributor
	DataCite:        			creator
	IMDI Element:               //Session/MDGroup/Actors/Actor/FullName[../Role/contains(text(), 'Researcher') or ../Role/contains(text(), 'Depositor')]
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundlePublicationInfo](#bundlepublicationinfo)

###### ContributorNameIdentifier
**Description:** &#x1F4A5; The ContributorNameIdentifier contains an URI that uniquely identifies the contributor according to an established scheme. ORCID and INSI are considered best practices. An email address in the form of an mailto URI is a fallback.
**Attribute** *identifierType*: ORCID and ISNI are considered best practices. An email address in the form of an mailto URI is a fallback. *Values*: ORCID, ISNI, Email, Other

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				anyURI
	Number of occurrences:  	0-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			Creator:nameIdentifier
	IMDI Element:               —
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) |  [Back to BundlePublicationInfo](#bundlepublicationinfo)

###### ContributorAffiliation
**Description:** &#x1F4A5; The ContributorAffiliation contains the organisational or institutional affiliation of the contributor as provided by the depositor.

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			Creator:affiliation
	IMDI Element:               —
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) |  [Back to BundlePublicationInfo](#bundlepublicationinfo)

### ProjectInfo
**Description:** ProjectInfo contains descriptive information about the project or the projects relating to the resource.

	Number of occurrences:		0-1

- [Project](#project)
	- [ProjectDisplayName](#projectdisplayname) &#x1F4A5;
	- [ProjectDescription](#projectdescription) &#x1F4A5;
	- [FunderInfos](#funderinfos)
		- [FunderInfo](#funderinfo)
			- [FunderName](#fundername) &#x1F4A5;
			- [FunderIdentifier](#funderidentifier) &#x1F4A5;
			- [GrantIdentifier](#grantidentifier) &#x1F4A5;
			- [GrantURI](#Granturi) &#x1F4A5;

[Back to Top](#blam-bundle-repository)

#### Project
**Description:** Project contains descriptive information about the project relating to bundle data.

	Number of occurrences:		1-unbounded

[Back to Top](#blam-bundle-repository) | [Back to ProjectInfo](#projectinfo)

#### ProjectDisplayName
**Description:** &#x1F4A5; The ProjectDisplayName element provides a human readable name of the project. The preferred form is the abbreviation by which the project is generally known. The long form is best placed in the project description.

	Discovery:					searchable, browsing facet
	Display:					page
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	project name
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2536_13fc5f10-c14a-1f64-a669-32736f6d3ef5

	VLO Facet: 					projectName
	OLAC (DCMI):				—
	DataCite:                   —
	IMDI Element:               	
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) | [Back to ProjectInfo](#projectinfo)

#### ProjectDescription
**Description:** &#x1F4A5; The ProjectDescription element provides a human readable description of the project including full project name. It should contain a description of the project’s objective or activity. The content of the ProjectDescription element will be used as the human readable description in interfaces. Its content can be queried by repositories for free-text metadata search. Data producers can provide ProjectDescription values for multiple interface languages.

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:            		—
	IMDI Element:               	           
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) | [Back to ProjectInfo](#projectinfo)

#### FunderInfos
**Description:** The FunderInfos component contains information about the funding organisation or organisations associated with this resource.

	Number of occurrences:		0-1

[Back to Top](#blam-bundle-repository) | [Back to ProjectInfo](#projectinfo)

#### FunderInfo
**Description:** The FunderInfo component contains information about the funding organisation associated with this resource.

	Number of occurrences:		1-unbounded

[Back to Top](#blam-bundle-repository) | [Back to ProjectInfo](#projectinfo)

#### FunderName
**Description:** &#x1F4A5; The FunderName element provides the name of the funding organisation. The preferred form is the abbreviation by with the funding agency is generally known. 

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	funder
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2522_3bdc6af1-bf1b-3f5d-2938-62d99a1980ab

	VLO Facet: 					—
	OLAC (DCMI):				Contributor:sponsor
	DataCite:                	Contributor:contributorType:Funder
	IMDI Element:               		   
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:		

[Back to Top](#blam-bundle-repository) | [Back to ProjectInfo](#projectinfo)

#### FunderIdentifier
**Description:** &#x1F4A5; The FunderIdentifier contains an URI that uniquely identifies the funding body according to an established scheme.

**Attribute** *FunderIdentifierType*: The FunderIdentifierType attribute determines the identifier type used. *Values:* CrossrefFunder, ISNI, GRID,  Other

	Discovery:					searchable
	Display:					page	
	User provided:				yes

	ValueScheme:				anyURI
	Number of occurrences:  	0-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               —   
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to ProjectInfo](#projectinfo)

#### GrantIdentifier
**Description:** &#x1F4A5; GrantIdentifier contains an element that uniquely identifies the grant according to an established scheme. Best Practice: funding body specific identifier such as NSF grant number or BMBF Förderkennzeichen.

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               —   
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to ProjectInfo](#projectinfo)

#### GrantURI
**Description:** &#x1F4A5; The GrantURI contains an URI that uniquely identifies the grant and funding body according to an established scheme.

	Discovery:					searchable
	Display:					page	
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	0-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):			
	DataCite:                		
	IMDI Element:               —       
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to ProjectInfo](#projectinfo)

### BundleDataInfo
**Description:** BundleDataInfo contains descriptive metadata about the annotation state of the data.

	Number of occurrences:		0-1

- [SegmentationUnits](#segmentationunits) 
	- [SegmentationUnit](#segmentationunit) &#x1F4A5;
- [TranscriptionTypes](#transcriptiontypes)
	- [TranscriptionType](#transcriptiontype) &#x1F4A5;
- [TranslationLanguages](#translationlanguages) 
	- [TranslationLanguage](#translationlanguage)
		- [TranslationLanguageCode](#translationlanguagecode) &#x1F4A5;
- [AnnotationTypes](#annotationtypes) 
	- [AnnotationType](#annotationtype) &#x1F4A5; 

[Back to Top](#blam-bundle-repository)

#### SegmentationUnits
**Description:** SegmentationUnits contains metadata about the criteria applied to segment the resource. 

	Number of occurrences:		0-1

[Back to Top](#blam-bundle-repository) | [Back to BundleDataInfo](#bundledatainfo)

#### SegmentationUnit
**Description:** &#x1F4A5; SegmentationUnit describes the criteria applied to segment the resource. This element applies to annotations of audio-visual data and is intended to facilitate the identification of useful data for a specific research question. The best practice is to use keywords.

Examples:  `clause` `intonation unit` 

	Discovery:					searchable, browsing facet
	Display:					page, list	
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	segmentation unit
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-3819_833e225a-f7c9-2c41-4bd3-c55c81ef7559

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               —       
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to BundleDataInfo](#bundledatainfo)

#### TranscriptionTypes
**Description:** TranscriptionTypes contains metadata about the level of transcription of audio-visual data in the annotations. 

	Number of occurrences:		0-1

[Back to Top](#blam-bundle-repository) | [Back to BundleDataInfo](#bundledatainfo)

#### TranscriptionType
**Description:** &#x1F4A5; TranscriptionType describes the level of transcription of audio-visual data in the annotations. Data with no TranscriptionType metadata will be treated as not transcribed by the repository.

Examples: `phonemic` `phonetic` `orthographic`  

	Discovery:					searchable, browsing facet
	Display:					page, list	
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               —   
	ELDP-CMDI Element:			—
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to BundleDataInfo](#bundledatainfo)

#### TranslationLanguages
**Description:** TranslationLanguages contains metadata about the languages used in translation of the data.

	Number of occurrences:		0-1

[Back to Top](#blam-bundle-repository) | [Back to BundleDataInfo](#bundledatainfo)

#### TranslationLanguage
**Description:** TranslationLanguage contains metadata about a particular language used in translation of the data. Data with no TranslationLanguage metadata will be treated as not translated by the repository. Data with several TranslationLanguage elements will be treated as having several translations.

	Number of occurrences:		1-unbounded

[Back to Top](#blam-bundle-repository) | [Back to BundleDataInfo](#bundledatainfo)

#### TranslationLanguageCode
**Description:** &#x1F4A5; The TranslationLanguageCode element describes the annotation of the type translation. It contains a language code (ISO 639-3) which identifies the language used in the translation. Data with no TranslationLanguage metadata will be treated as not translated by the repository. Data with several TranslationLanguage elements will be treated as having several translations.

	Discovery:					no
	Display:					page, list
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               —   
	ELDP-CMDI Element:  		—
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to BundleDataInfo](#bundledatainfo)

#### AnnotationTypes
**Description:** AnnotationTypes contains metadata describing the level and type of annotation of audio-visual data.

	Number of occurrences:		0-1

[Back to Top](#blam-bundle-repository) | [Back to BundleDataInfo](#bundledatainfo)

#### AnnotationType
**Description:** &#x1F4A5; AnnotationType describes the level and type of annotation of audio-visual data in the annotations. Data with no annotation metadata will be treated as not annotated by the repository.

**Examples:** `word-by-word` `GRAID` `PoS Tagging`  

	Discovery:					searchable, browsing facet
	Display:					page, list
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               —   
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to BundleDataInfo](#bundledatainfo)

### BundleAdministrativeInfo
**Description:** BundleAdministrativeInfo contains administrative metadata that will be publicly communicated, especially in regard to metacatalogues and user interfaces.

	Number of occurrences:		1-1

- [BundleIsIdenticalTo](#bundleisidenticalto) &#x1F4A5;
- [BundleIsDerivedFrom](#bundleisderivedfrom) &#x1F4A5;
- [License](#license)
	- [LicenseIdentifier](#licenseidentifier) &#x1F4A5;

[Back to Top](#blam-bundle-repository)

#### BundleIsIdenticalTo
**Description:** &#x1F4A5; The BundleIsIdenticalTo element contains an URI that uniquely identifies an identical resource. This element should only be used if it can be ascertained that the identified resource and the current resource will remain identical; else BundleIsDerivedFrom should be used.

	Discovery:					no
	Display:					page
	User provided:				yes		

	ValueScheme:				anyURI
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	RelatedIdentifier:relationType:IsIdenticalTo
	IMDI Element:               —       
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to BundleAdministrativeInfo](#bundleadministrativeinfo)

#### BundleIsDerivedFrom
**Description:** &#x1F4A5; The BundleIsDerivedFrom element contains an URI that uniquely identifies the resource from which the current resource is derived.

	Discovery:					no
	Display:					page
	User provided:				yes

	ValueScheme:				anyURI
	Number of occurrences:  	0-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				Relation:dcterms:isVersionOf
	DataCite:                	RelatedIdentifier:relationType:IsDerivedFrom
	IMDI Element:               —    
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to BundleAdministrativeInfo](#bundleadministrativeinfo)

#### License
**Description:** The License component contains information about the license under which the resource is available.

	Number of occurrences:		1-unbounded

[Back to Top](#blam-bundle-repository) | [Back to BundleAdministrativeInfo](#bundleadministrativeinfo)

#### LicenseIdentifier
**Description:** &#x1F4A5; The LicenseIdentifier provides a URI for the license.

	Discovery:					no
	Display:					page
	User provided:				yes

	ValueScheme:				anyURI
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	license URL
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-6586_2c79d86a-5a75-0890-d407-7d9cb86b9beb

	VLO Facet: 					distributionType
	OLAC (DCMI):				dcterms:license
	DataCite:                	rightsURI
	IMDI Element:               —
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to BundleAdministrativeInfo](#bundleadministrativeinfo)

### BundleStructuralInfo
**Description:** BundleStructuralInfo contains structural metadata that describes the internal structure of the bundle.

	Number of occurrences:		1-1

- [BundleAdditionalMetadataFile](#bundleadditionalmetadatafile)
	- [FileName](#filename-metadatafile) &#x1F4A5; 
	- [IsMetadataOf](#ismetadataof-metadatafile) &#x1F4A5;
	- [FileDescription](#filedescription-metadatafile)  &#x1F4A5;
- [BundleResources](#bundleresources)
	- [MediaResource](#mediaresource)
		- [FileName] (#filename-mediaresource) &#x1F4A5;
		- [FileDescription](#filedescription-mediaresource)  &#x1F4A5;
	- [WrittenResource](#writtenresource)
		- [FileName] (#filename-writtenresource) &#x1F4A5;
		- [IsAnnotationOf](#isannotationof-writtenresource) &#x1F4A5;
		- [FileDescription](#filedescription-writtenresource)  &#x1F4A5; 
	- [OtherResource](#otherresource)
		- [FileName] (#filename-otherresource) &#x1F4A5;
		- [FileDescription](#filedescription-otherresource)  &#x1F4A5;

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

#### BundleAdditionalMetadataFile
**Description:** The BundleAdditionalMetadataFile component contains metadata about additional metadata files contained in the bundle.

	Number of occurrences:		0-unbounded

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

##### FileName (MetadataFile)
**Description:** &#x1F4A5; The FileName element contains the name of the file as provided by the depositor.

	Discovery:					no
	Display:					page
	User provided:				no		

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               	       
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:		

##### IsMetadataOf (MetadataFile)
**Description:** &#x1F4A5; The IsMetadataOf element contains a PID that uniquely identifies the file described by the file described in this component.

	Discovery:					no
	Display:					page
	User provided:				yes

	ValueScheme:				anyURI
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	RelatedIdentifier:relationType:IsMetadataFor
	IMDI Element:               —  
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

##### FileDescription (MetadataFile)
**Description:** &#x1F4A5; The FileDescription contains a human readable, file specific description. This element should be used to provide file specific that cannot be added to the bundle description. Any information applicable to the whole bundle should be added to the BundleDescription element.

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	
	CCR URI:                	

	VLO Facet: 					description
	OLAC (DCMI):				http://purl.org/dc/terms/description
	DataCite:        			Description
	IMDI Element:               	
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

#### BundleResources
**Description:** The BundleResources component contains metadata about files contained in the bundle.

	Number of occurrences:		1-1

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

##### MediaResource
**Description:** The MediaResource component contains metadata about media files contained in the bundle.

	Number of occurrences:		0-unbounded

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

###### FileName (MediaResource)
**Description:** &#x1F4A5; The FileName element contains the name of the file as provided by the depositor.

	Discovery:					no
	Display:					page
	User provided:				no		

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               	       
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:		

###### FileDescription (MediaResource)
**Description:** &#x1F4A5; The FileDescription contains a human readable, file specific description. This element should be used to provide file specific that cannot be added to the bundle description. Any information applicable to the whole bundle should be added to the BundleDescription element.

	Discovery:					searchable
	Display:					page	
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	description
	CCR URI:                	

	VLO Facet: 					description
	OLAC (DCMI):				http://purl.org/dc/terms/description
	DataCite:        			Description
	IMDI Element:               	
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

##### WrittenResource
**Description:** The WrittenResource component contains metadata about annotation files and other character encoded information contained in the bundle.

	Number of occurrences:		0-unbounded

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

###### FileName (WrittenResource)
**Description:** &#x1F4A5; The FileName element contains the name of the file as provided by the depositor.

	Discovery:					no
	Display:					page
	User provided:				no		

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               	       
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:			

###### IsAnnotationOf (WrittenResource)
**Description:** &#x1F4A5; The IsAnnotationOf element contains a PID that uniquely identifies the file annotated by the file described in this component.

	Discovery:					no
	Display:					page
	User provided:				yes (processed)

	ValueScheme:				anyURI
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               —  
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

###### FileDescription (WrittenResource)
**Description:** &#x1F4A5; The FileDescription contains a human readable, file specific description. This element should be used to provide file specific that cannot be added to the bundle description. Any information applicable to the whole bundle should be added to the BundleDescription element.

	Discovery:					searchable
	Display:					page	
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	description
	CCR URI:                	

	VLO Facet: 					description
	OLAC (DCMI):				http://purl.org/dc/terms/description
	DataCite:        			Description
	IMDI Element:               	
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

##### OtherResource
**Description:** The OtherResource component contains metadata about additional files contained in the bundle that are not covered by the BundleAdditionalMetadataFile, MediaResource, and WrittenResource components.

	Number of occurrences:		0-unbounded

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

###### FileName (OtherResource)
**Description:** &#x1F4A5; The FileName element contains the name of the file as provided by the depositor.

	Discovery:					no
	Display:					page
	User provided:				no		

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               	       
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:		

###### FileDescription (OtherResource)
**Description:** &#x1F4A5; The FileDescription contains a human readable, file specific description. This element should be used to provide file specific that cannot be added to the bundle description. Any information applicable to the whole bundle should be added to the BundleDescription element.

	Discovery:					searchable
	Display:					page	
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	description
	CCR URI:                	

	VLO Facet: 					description
	OLAC (DCMI):				http://purl.org/dc/terms/description
	DataCite:        			Description
	IMDI Element:               	
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo) 
