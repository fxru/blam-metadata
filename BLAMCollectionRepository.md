# Basic Language Archive Metadata (Collection Repository)

> **Blam** The standard blasty noise. The power of the blam can sometimes be measured by the size of the word when it is written, or by the number of exclamation marks at the end of the word.
> 			[urban dictionary](http://www.urbandictionary.com/define.php?term=blam&defid=305474)

Basic Language Archive Metadata (BLAM) is designed to provide basic metadata for language repositories. The metadata scheme maximises discoverability and user oriented information without a proliferation of data fields and work for the data producer. Basic Language Archive Metadata is a suite of [CMDI](https://www.clarin.eu/content/component-metadata) profiles and currently consist of two pairs of profiles: 

* BLAM Collection Repository: [documentation](https://github.com/fxru/blam-metadata/blob/master/BLAMCollectionRepository.md)
* BLAM Collection User: documentation (to come)
* BLAM Collection Repository: described in this document [below](#blam-collection-repository)
* BLAM Collection User: documentation  (to come)

BLAM Collection Repository contains information about bundles as provided by the repository. Data providers are asked to submit a subset of this imformation during ingest. The BLAM Collection User profile defines this subset of 35 data fields of which 16 are obligatory. The separate definition of the BLAM Collection User profile enhances the usability for data providers and can be validated independently from the more comprehensive BLAM Collection Repository profile. The Basic Language Archive Metadata Collection User profile is intended to be the primary source of user input for BLAM Collection Repository. However, BLAM BCollectionRepository is designed to allow automatic import of information from other metadata formats. The formats actively considered are: 

* IMDI Metadata Format: [ISLE Meta Data Initative, Version 3.0.4 (2003)](https://tla.mpi.nl/imdi-metadata/)
* CMDI imdi-corpus-profile: [clarin.eu:cr1:p_1274880881885](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1274880881885&registrySpace=public)
* CMDI ELDP_Collection: [clarin.eu:cr1:p_1407745711991](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1407745711991&registrySpace=public)
* CMDI lat-corpus: [clarin.eu:cr1:p_1407745712064](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1407745712064&registrySpace=public)  

The data fields that are transferred from BLAM Collection User input are marked by &#x1F4A5; in this document. Obligatory data fields are indicated by &#x1F4CC; in this document.

BLAM Collection Repository is designed with a focus on discoverability and display. Data producers can submit additional metadata information to document their data and their research. The preferred format are other CMDI profiles or comparably standardized metadata formats.

The data fields of BLAM Collection Repository were defined to facilitate interoperability with metacatalogues, in particular [DataCite](https://search.datacite.org/), [OLAC](http://search.language-archives.org/), and [VLO](https://vlo.clarin.eu/).

* OLAC metadata: [specifications](http://www.language-archives.org/OLAC/metadata.html), [usage](http://www.language-archives.org/NOTE/usage.html)
* DataCite Metadata: [Schema 4.0](https://schema.datacite.org/meta/kernel-4.0/)
* CLARIN VLO facets: [facets mapping](https://lux17.mpi.nl/isocat/clarin/vlo/mapping/index.html)

Recommended tools to create BLAM metadata are [CMDI Maker](http://cmdi-maker.uni-koeln.de/), [COMEDI](http://clarino.uib.no/comedi/), and [Arbil](https://tla.mpi.nl/tools/tla-tools/arbil/).

BLAM! &#x1F4A5; That’s it, enjoy documenting your data!

## BLAM-Collection-Repository

**Description:** The Basic Language Archive Metadata Collection profile aims to provide a basic metadata profile for language repositories. The profiles cover fundamental domain specific, but project independent, descriptive metadata as well as basic administrative and structural metadata. BLAM Collection focusses on discoverability and human-readable display.

* [CollectionGeneralInfo](#colletiongeneralinfo)
* [CollectonPublicationInfo](#collectionpublicationinfo)
* [ProjectInfo](#projectinfo)
* [CollectionDataInfo](#collectiondatainfo)
* [CollectionAdministrativeInfo](#collectionadministrativeinfo)
* [CollectionStructuralInfo](#collectionstructuralinfo)

### CollectionGeneralInfo
**Description:** CollectionGeneralInfo contains general descriptive metadata about the collection.

	Number of occurrences:	1-1

- [CollectionID](#collectionid)
- [CollectionDisplayTitle](#collectiondisplaytitle) &#x1F4A5;
- [CollectionDescription](#collectiondescription) &#x1F4A5;
- [CollectionKeywords](#collectionkeywords)
	- [CollectionKeyword](#collectionkeyword) &#x1F4A5;
- [CollectionObjectLanguages](#collectionobjectlanguages)
	- [CollectionObjectLanguage*](#collectionobjectlanguage)
		- [ObjectLanguageDisplayName*](#objectlanguagedisplayname) &#x1F4A5;
		- [ObjectLanguageName*](#objectlanguagename)
		- [ObjectLanguageISO639-3Code*](#objectlanguageiso639-3code) &#x1F4A5;
		- [ObjectLanguageGlottologCode](#objectlanguageglottologcode)
		- [ObjectLanguageLanguageFamily](#objectlanguagelanguagefamily)
- [CollectionLocation](#collectionlocation)
	- [CollectionGeoLocation](#collectiongeolocation) &#x1F4A5;
	- [CollectionLocationDisplayName](#collectionlocationdisplayname) &#x1F4A5;
	- [CollectionLocationName](#collectionlocationname)
	- [CollectionRegionDisplayName](#collectionregiondisplayname) &#x1F4A5;
	- [CollectionRegionName](#collectionregionname) 
	- [CollectionCountryDisplayName](#collectionCountryDisplayName)  &#x1F4A5;
	- [CollectionCountryName](#collectionCountryName)
	- [CollectionCountryCode](#collectioncountrycode) 

[Back to Top](#blam-collection-repository)

#### CollectionID
**Description:** &#x1F4CC; The CollectionID element contains an identifier that consistently and uniquely identifies the collection described in the particular metadata token. The identifier should be a PID and is usually generated by the repository during the ingest process.

	Interface Facet:			no
	User provided:				no

	ValueScheme: 				anyURI
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	resource name
	CCR URI:                	hdl.handle.net—CCR_C-2544_3626545e-a21d-058c-ebfd-241c0464e7e5
	
	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:               	Identifier 
	IMDI Element:				//METATRANSCRIPT/@ArchiveHandle
	ELDP-CMDI Element:      	—
	IMDI-CMDI Element:
	LAT-IMDI:				

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionDisplayTitle 
**Description:** &#x1F4A5; &#x1F4CC; The CollectionDisplayTitle element provides a human readable name of the collection. It should contain a meaningful and recognisable title for the bundle. The content of the CollectionDisplayTitle element will be used as the human readable identifier in interfaces. Data providers can provide CollectionDisplayTitle values for multiple interface languages.

	Interface Facet:			yes, full text, display
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	yes
	CCR prefLabel@en:       	resource title
	CCR URI:                	hdl.handle.net—CCR_C-2545_d873f2ab-2a2f-29d6-a9ab-260cde57f227

	VLO Facet: 					name
	OLAC (DCMI):				purl.org—title <http://purl.org/dc/terms/title>
	DataCite:        			Title
	IMDI Element:               
	ELDP-CMDI Element:			
	IMDI-CMDI Element:		

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionDescription 
**Description:** &#x1F4A5; &#x1F4CC; The CollectionDescription element provides a human readable description of the bundle. It should contain a description of the content of the collection. The content of the CollectionDescription element will be used as the human readable description in interfaces. Its content can be queried by repositories for free-text metadata search. Data providers can provide CollectionDescription values for multiple interface languages.

	Interface Facet:			yes, full text, display
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	yes
	CCR prefLabel@en:       	description
	CCR URI:                	hdl.handle.net—CCR_C-2520_9eeedfb4-47d3-ddee-cfcb-99ac634bf1db <http://hdl.handle.net/11459/CCR_C-2520_9eeedfb4-47d3-ddee-cfcb-99ac634bf1db>

	VLO Facet: 					description
	OLAC (DCMI):				purl.org—description <http://purl.org/dc/terms/description>
	DataCite:        			Description
	IMDI Element:               
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

#### CollectionKeywords
**Description:** CollectionKeywords should be used to describe the content and nature of data to enhance the discoverability and facilitate finer granularity for searches and browsing of the data. Repositories can use keyword metadata to define meaningful subsets of the data and provide a better browsing experience. 

								Number of occurrences:	0-1

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionKeyword 
**Description:** &#x1F4A5; CollectionKeyword should contain a single keyword or keyphrase and should be used to describe the content and nature of data to enhance the discoverability and facilitate finer granularity for searches and browsing of the data. Repositories can use keyword metadata to define meaningful subsets of the data and provide a better browsing experience. 

	Interface Facet:			yes, full text, display
	User provided:				yes		

	ValueScheme:				string
	Number of occurrences:  	0-unbound
	Multilingual:           	yes
	CCR prefLabel@en:       	metadata tag
	CCR URI:               		hdl.handle.net—CCR_C-5436_6ab57c2c-5f8d-3561-6db6-d75da23d2637 <http://hdl.handle.net/11459/CCR_C-5436_6ab57c2c-5f8d-3561-6db6-d75da23d2637>

	VLO Facet: 					keywords
	OLAC (DCMI):				—
	DataCite:        			Subject
	IMDI Element:               various (closest match: //Session/Keys/*)
	ELDP-CMDI Element:          CCR:ELDP_Collection:Keywords:Keyword
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionObjectLanguages
**Description:** CollectionObjectLanguages contains information about the language or languages that are the object of the resource. 

	Number of occurrences:		1-1

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionObjectLanguage
**Description:** CollectionObjectLanguage contains information about the language that is the object of the resource.

	Number of occurrences:		1-unbound

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### ObjectLanguageDisplayName
**Description:** &#x1F4A5; &#x1F4CC; The ObjectLanguageDisplayName element contains the name of the object language in the version recommended by the data producer. Repositories should tread the name provided by this element as the primary language name when displaying the metadata in relation to this particular data set (e.g. collection or bundle).The repository may use alternative names provided by services such as Glottolog or Ethnologue to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no language name is given for a particular interface language. Data providers can provide LanguageDisplayName values for multiple interface languages. 

	Interface Facet:			yes, display, browsing
	User provided:				yes		

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	yes
	CCR prefLabel@en:       	Language Name
	CCR URI:                	hdl.handle.net—CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d <http://hdl.handle.net/11459/CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d>

	VLO Facet: 					languageCode
	OLAC (DCMI):				purl.org—language <http://purl.org/dc/terms/language>
	DataCite:        			Language
	IMDI Element:               
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### ObjectLanguageName
**Description:** The ObjectLanguageName element contains the name of the object language in the version as provided by services such as Glottolog or Ethnologue. 

	Interface Facet:			yes, browsing
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	0-unbound
	Multilingual:           	yes
	CCR prefLabel@en:       	Language Name
	CCR URI:                	hdl.handle.net—CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d <http://hdl.handle.net/11459/CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d>

	VLO Facet: 					languageCode
	OLAC (DCMI):				purl.org—language <http://purl.org/dc/terms/language>
	DataCite:        			Language
	IMDI Element:               
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### ObjectLanguageISO639-3Code
**Description:**  &#x1F4A5; &#x1F4CC; The ObjectLanguageISO639-3 element contains an ISO 639-3 language code for the object language.

	Interface Facet:			full text
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	Language ID
	CCR URI:                	hdl.handle.net—CCR_C-2482_08eded24-4086-7e3f-88e5-e0807fb01e17 <http://hdl.handle.net/11459/CCR_C-2482_08eded24-4086-7e3f-88e5-e0807fb01e17>

	VLO Facet: 					languageCode
	OLAC (DCMI):				purl.org—language <http://purl.org/dc/terms/language>
	DataCite:        			Language
	IMDI Element:               
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### ObjectLanguageGlottologCode
**Description:** &#x1F4CC; The ObjectLanguageISO639-3 element contains an ISO 639-3 language code for the object language.

	Interface Facet:			full text
	User provided:				no	

	ValueScheme:				string
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

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### ObjectLanguageLanguageFamily
**Description:** &#x1F4CC; The ObjectLanguageLanguageFamily element contains the name of the language family and sub-families or sub-groups the object language belongs to. The values are taken from Glottolog and given in the version as provided by this service. 

	Interface Facet:			yes, full text browsing
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-unbound
	Multilingual:           	yes
	CCR prefLabel@en:       	Language Name
	CCR URI:                	hdl.handle.net—CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d <http://hdl.handle.net/11459/CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d>

	VLO Facet: 					languageCode
	OLAC (DCMI):				purl.org—language <http://purl.org/dc/terms/language>
	DataCite:        			Language
	IMDI Element:               
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionLocation
**Description:** CollectionLocation contains information about the most relevant or salient location in relation to the data contained in the bundle. The default location would be the location of recording. However, any other location vowed as most relevant to the data can be set as the CollectionLocation. The information provided in the component is intended for discoverability and display purposes. Detailed documentation of geographic information should be outsourced into an additional metadata file.

	Number of occurrences:		1-1

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionGeoLocation
**Description:** &#x1F4A5; &#x1F4CC; The CollectionGeoLocation element contains a geographical coordinates for a location point conforming to ISO 6709. 

	Interface Facet:			display (map)
	User provided:				yes				

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	geographical coordinates
	CCR URI:                	hdl.handle.net—CCR_C-2523_283c7b54-06ed-3d6c-4bb0-c8a79a8236fd <http://hdl.handle.net/11459/CCR_C-2523_283c7b54-06ed-3d6c-4bb0-c8a79a8236fd>

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			GeoLocation:geoLocationPoint
	IMDI Element:               —
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionLocationDisplayName
**Description:** &#x1F4A5; &#x1F4CC; The CollectionLocationDisplayName element contains the name of a location in the version recommended by the data producer. Repositories should treat the name provided by this element as the primary location name when displaying the metadata in relation to this particular data set (e.g. collection or bundle).The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance the browsing and search experience. The repository may also translate the name into other languages if no CollectionLocationDisplayName name is given for a particular interface language. Data providers can provide CollectionLocationDisplayName values for multiple interface languages. 

	Interface Facet:			yes, full text
	User provided:				yes		

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	yes
	CCR prefLabel@en:       	place name
	CCR URI:                	hdl.handle.net—CCR_C-5580_03e458f2-f873-8645-76eb-40e001b6c1ac <http://hdl.handle.net/11459/CCR_C-5580_03e458f2-f873-8645-76eb-40e001b6c1ac>

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        
	IMDI Element:               //Session/MDGroup/Location/Address
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionLocationName
**Description:** The CollectionLocationName element contains the name of a location provided by services such as GeoNames. This name is used to improve discoverability and to enhance the browsing and search experience. GeoNames field: name (or toponymName).

	Interface Facet:			yes, full text
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	0-unbound
	Multilingual:           	yes
	CCR prefLabel@en:       	place name
	CCR URI:                	hdl.handle.net—CCR_C-5580_03e458f2-f873-8645-76eb-40e001b6c1ac <http://hdl.handle.net/11459/CCR_C-5580_03e458f2-f873-8645-76eb-40e001b6c1ac>

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        
	IMDI Element:				//Session/MDGroup/Location/Address
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionRegionDisplayName
**Description:** &#x1F4A5; The CollectionRegionDisplayName element optionally contains the name of an administrative subdivision such as state, province, or any other culturally salient unit in the version recommended by the data producer. The data producer can decided which level of subdivision is relevant and will improve discoverability. Repositories should tread the name provided by this element as the primary location name when displaying the metadata in relation to this particular data set (e.g. collection or bundle). The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no RegionDisplayName value is given for a particular interface language. Data providers can provide RegionDisplayName values for multiple interface languages.

	Interface Facet:			yes, full text
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-1
	Multilingual:           	yes
	CCR prefLabel@en:       	location region
	CCR URI:                	hdl.handle.net—CCR_C-2533_fa6e1812-e29b-3cf6-e15a-50aa34b9be68 <http://hdl.handle.net/11459/CCR_C-2533_fa6e1812-e29b-3cf6-e15a-50aa34b9be68>

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			—
	IMDI Element:              
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionRegionName
**Description:** The CollectionRegionName element contains the name of an administrative subdivision provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. GeoNames field: adminName1 

	Interface Facet:			yes, full text
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	0-unbound
	Multilingual:           	yes
	CCR prefLabel@en:       	location region
	CCR URI:                	hdl.handle.net—CCR_C-2533_fa6e1812-e29b-3cf6-e15a-50aa34b9be68 <http://hdl.handle.net/11459/CCR_C-2533_fa6e1812-e29b-3cf6-e15a-50aa34b9be68>

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			—
	IMDI Element:               //Session/MDGroup/Location/Region
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionCountryDisplayName
**Description:** &#x1F4A5; The CollectionCountryDisplayName element contains the name of the country to which the location belongs in the version recommended by the data producer. Repositories should tread the name provided by this element as the primary country name when displaying the metadata in relation to this particular data set (e.g. collection or bundle). The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no CollectionCountryDisplayName name is given for a particular interface language. Data providers can provide CollectionCountryDisplayName values for multiple interface languages.  

	Interface Facet:			yes, full text
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	0-1
	Multilingual:           	yes
	CCR prefLabel@en:       	location country
	CCR URI:                	hdl.handle.net—CCR_C-2532_d004b0a6-fd1d-3ca3-abf1-1e6aeb3e37b2 <http://hdl.handle.net/11459/CCR_C-2532_d004b0a6-fd1d-3ca3-abf1-1e6aeb3e37b2>

	VLO Facet: 					country
	OLAC (DCMI):				—
	DataCite:        			—
	IMDI Element:               //Session/MDGroup/Location/Country
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionCountryName
**Description:** The CollectionCountryName element contains the name of the country as provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. GeoNames field: countryName

	Interface Facet:			yes, full text
	User provided:				no	

	ValueScheme:				string
	Number of occurrences:  	0-1
	Multilingual:           	yes
	CCR prefLabel@en:       	location country
	CCR URI:                	hdl.handle.net—CCR_C-2532_d004b0a6-fd1d-3ca3-abf1-1e6aeb3e37b2 <http://hdl.handle.net/11459/CCR_C-2532_d004b0a6-fd1d-3ca3-abf1-1e6aeb3e37b2>

	VLO Facet: 					country
	OLAC (DCMI):				—
	DataCite:        			—
	IMDI Element:               //Session/MDGroup/Location/Country
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

#### CollectionCountryCode
**Description:** &#x1F4CC; The CollectionCountryCode element contains the ISO 3166-1 alpha 2 code of the country of the location as provided by services such as GeoNames GeoNames field: countryCode

	Interface Facet:			no, full text
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	country coding
	CCR URI:                	hdl.handle.net—CCR_C-2092_36cd7ca8-e412-9f29-7ea7-4a3ba4ba2c91 <http://hdl.handle.net/11459/CCR_C-2092_36cd7ca8-e412-9f29-7ea7-4a3ba4ba2c91>

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			—
	IMDI Element:               —
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-collection-repository) | [Back to CollectionGeneralInfo](#collectiongeneralinfo)

### CollectionPublicationInfo
**Description:** The CollectionPublicationInfo component contains metadata pertaining the publication of the resource. The information provided in this component is used for display and in particular to generate bibliographical references to the resource.

	Number of occurrences:		1-1

- [CollectionCreators](#collectioncreators) 
	- [CollectionCreator](#collectioncreator)
		- [CreatorDisplayName](#creatordisplayname) &#x1F4A5;
		- [CreatorNameIdentifier](#creatornameidentifier) &#x1F4A5;
		- [CreatorAffiliation](#creatoraffiliation) &#x1F4A5;
- [CollectionPublicationYear](#collectionpublicationyear) &#x1F4A5;
- [CollectionDataProvider](#collectiondataprovider)

[Back to Top](#blam-collection-repository)

#### CollectionCreators
**Description:** The CollectionCreator component contains information about the creator or creators of the resource.

	Number of occurrences:		1-1

[Back to Top](#blam-collection-repository) | [Back to CollectionPublicationInfo](#collectionpublicationinfo)

#### CollectionCreator
**Description:** The CollectionCreator component contains information about the creator of the resource.

	Number of occurrences:		1-unbound

[Back to Top](#blam-collection-repository) | [Back to CollectionPublicationInfo](#collectionpublicationinfo)

#### CreatorDisplayName
**Description:** &#x1F4A5; &#x1F4CC; The CreatorDisplayName element contains the name of the creator in a form that lends itself to alphabetical sorting. The value of this field can be used to generate a bibliographical citation reference for the resource. This usage should guide the formatting. The data provider determines what is the proper order of names for an alphabetically sorted list.

	Interface Facet:			yes, full text, citation
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	creator
	CCR URI:                	hdl.handle.net—CCR_C-6836_d35e73a8-ec72-d3c4-e39a-4b0fefd32cdc <http://hdl.handle.net/11459/CCR_C-6836_d35e73a8-ec72-d3c4-e39a-4b0fefd32cdc>

	VLO Facet: 					—
	OLAC (DCMI):				contributor
	DataCite:        			creator
	IMDI Element:               	
//Session/MDGroup/Actors/Actor/FullName[../Role/contains(text(), 'Researcher') or ../Role/contains(text(), 'Depositor')]
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) |  [Back to CollectionPublicationInfo](#collectionpublicationinfo)

#### CreatorNameIdentifier
**Description:** &#x1F4A5; The CreatorNameIdentifier contains an URI that uniquely identifies the creator according to an established scheme. Best Practice: ORCID, INSI

	Interface Facet:			no
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

[Back to Top](#blam-collection-repository) |  [Back to CollectionPublicationInfo](#collectionpublicationinfo)

#### CreatorAffiliation
**Description:** &#x1F4A5; The CreatorAffiliation contains the organisational or institutional affiliation of the creator as provided by the depositor.

	Interface Facet:			yes
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-unbound
	Multilingual:           	yes
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			Creator:affiliation
	IMDI Element:               —
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:			—

[Back to Top](#blam-collection-repository) |  [Back to CollectionPublicationInfo](#collectionpublicationinfo)

#### CollectionPublicationYear
**Description:** &#x1F4A5; &#x1F4CC; CollectionPublicationYear contains the year of publication in the form YYYY conforming to ISO 8601. The default value is the ingest date into the repository unless an embargo has been set for the resource. In that case the end year of the embargo is taken as the year of publication. For legacy data, the  value of CollectionPublicationDate can be set to a point before the ingest. The value of this field should be used to generate a bibliographical citation reference for the resource. 

	Interface Facet:			yes, display
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	publication date
	CCR URI:                	hdl.handle.net—CCR_C-2538_8b697452-7ef3-9fce-ccf9-a7f344f11317

	VLO Facet: 					—
	OLAC (DCMI):				Date:dcterms:available
	DataCite:        			PublicationYear
	IMDI Element:               —
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-collection-repository) |  [Back to CollectionPublicationInfo](#collectionpublicationinfo)

#### CollectionDataProvider
**Description:** &#x1F4CC; CollectionDataProvider contain the name of the data provider. The default value would be the name of the repository or its holding institution. The value of this field can be used to generate a bibliographical citation reference for the resource. 
			
	Interface Facet:			no
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	yes
	CCR prefLabel@en:       	publisher
	CCR URI:                	hdl.handle.net—CCR_C-6134_72c22724-2615-fd70-2eff-8cd3cb59e91d

	VLO Facet: 					—
	OLAC (DCMI):				Publisher
	DataCite:        			Publisher
	IMDI Element:               —
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:			—

[Back to Top](#blam-collection-repository) |  [Back to CollectionPublicationInfo](#collectionpublicationinfo)

### ProjectInfo
**Description:** ProjectInfo contains descriptive information about the project or the projects relating to the collection.

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

[Back to Top](#blam-collection-repository)

#### Project
**Description:** Project contains descriptive information about the project relating to bundle data.

	Number of occurrences:		1-unbound

[Back to Top](#blam-collection-repository) | [Back to ProjectInfo](#projectinfo)

#### ProjectDisplayName
**Description:** &#x1F4A5; &#x1F4CC; The ProjectDisplayName element provides a human readable name of the project. The preferred form is the abbreviation by with the project is generally known. The long form is best placed in the project description.

	Interface Facet:			yes, display
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	yes
	CCR prefLabel@en:       	project name
	CCR URI:                	hdl.handle.net—CCR_C-2536_13fc5f10-c14a-1f64-a669-32736f6d3ef5

	VLO Facet: 					projectName
	OLAC (DCMI):				—
	DataCite:                   —
	IMDI Element:               	
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to ProjectInfo](#projectinfo)

#### ProjectDescription
**Description:** &#x1F4A5; &#x1F4CC; The ProjectDescription element provides a human readable description of the project in eluding its full name or title. It should contain a description of the project objective or activity. The content of the ProjectDescription element will be used as the human readable description in interfaces. Its content can be queried by repositories for free-text metadata search. Data providers can provide ProjectDescription values for multiple interface languages

	Interface Facet:			yes, fulltext
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	yes
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:            		—
	IMDI Element:               	           
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to ProjectInfo](#projectinfo)

#### FunderInfos
**Description:** The FunderInfo scomponent contains information about the funding organisation or organisations associated with this resource.

	Number of occurrences:		0-unbound

[Back to Top](#blam-collection-repository) | [Back to ProjectInfo](#projectinfo)

#### FunderInfo
**Description:** The FunderInfo component contains information about the funding organisation associated with this resource.

	Number of occurrences:		1-unbound

[Back to Top](#blam-collection-repository) | [Back to ProjectInfo](#projectinfo)

#### FunderName
**Description:** &#x1F4A5; &#x1F4CC; The FunderName element provides the name of the funding organisation. The preferred form is the abbreviation by which the project is generally known. 

	Interface Facet:			yes, fulltext, display
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	funder
	CCR URI:                	hdl.handle.net—CCR_C-2522_3bdc6af1-bf1b-3f5d-2938-62d99a1980ab

	VLO Facet: 					—
	OLAC (DCMI):				Contributor:sponsor
	DataCite:                	Contributor:contributorType:Funder
	IMDI Element:               		   
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:		

[Back to Top](#blam-collection-repository) | [Back to ProjectInfo](#projectinfo)

#### FunderIdentifier
**Description:** &#x1F4A5; The FunderIdentifier contains an URI that uniquely identifies the funding body according to an established scheme. Best Practice: a FundRefID doi.

	Interface Facet:			yes, fulltext	
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

[Back to Top](#blam-collection-repository) | [Back to ProjectInfo](#projectinfo)

#### GrantIdentifier
**Description:** &#x1F4A5; GrantIdentifier contains an element that uniquely identifies the grant according to an established scheme. Best Practice: funding body specific identifier such as NSF grant number or BMBF Förderkennzeichen.

	Interface Facet:			yes, fulltext
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

[Back to Top](#blam-collection-repository) | [Back to ProjectInfo](#projectinfo)

#### GrantURI
**Description:** &#x1F4A5; The GrantURI contains an URI that uniquely identifies the grant and funding body according to an established scheme.

	Interface Facet:			yes, fulltext	
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

[Back to Top](#blam-collection-repository) | [Back to ProjectInfo](#projectinfo)


### CollectionAdministrativeInfo
*Description:** CollectionAdministrativeInfo contains administrative metadata that will be publicly communicated, especially in regard to metacatalogues and user interfaces.

	Number of occurrences:		1-1

- [CollectionIsIdenticalTo](#collectionisidenticalto) &#x1F4A5;
- [CollectionIsDerivedFrom](#collectionisderivedfrom) &#x1F4A5;
- [Licence](#licence)
	- [LicenceName](#licencename)
	- [LicenceIdentifier](#licenceidentifier) &#x1F4A5;
- [Access](#access) 
- [AvailabilityDate](#availabilitydate)
- [RightsHolder](#rightsholder)
	- [RightsHolderName](#rightsholdername)  &#x1F4A5;
	- [RightsHolderIdentifier](#rightsholderidentifier) &#x1F4A5;

[Back to Top](#blam-collection-repository)

#### CollectionIsIdenticalTo
**Description:** &#x1F4A5; The CollectionIsIdenticalTo element contains an URI that uniquely identifies an identical resource. This element should only be used if it can be ascertained that the identified resource and the current resource will remain identical; else CollectionIsDerivedFrom should be used.

	Interface Facet:			display
	User provided:				yes		

	ValueScheme:				anyURI
	Number of occurrences:  	0-unbound
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	RelatedIdentifier:relationType:IsIdenticalTo
	IMDI Element:               —       
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-collection-repository) | [Back to CollectionAdministrativeInfo](#collectionadministrativeinfo)

#### CollectionIsDerivedFrom
**Description:** &#x1F4A5; The CollectionIsDerivedFrom element contains an URI that uniquely identifies the resource from which the current resource is derived.

	Interface Facet:			display
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

[Back to Top](#blam-collection-repository) | [Back to CollectionAdministrativeInfo](#collectionadministrativeinfo)

#### Licence
**Description:** The Licence component contains information about the licence under which the resource is available.

	Number of occurrences:		1-unbound

[Back to Top](#blam-collection-repository) | [Back to CollectionAdministrativeInfo](#collectionadministrativeinfo)

#### LicenceName
**Description:** &#x1F4CC; The LicenceName element should provide a human readable complete title of a licence and include version information if applicable.

	Interface Facet:			yes, display	
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	license
	CCR URI:                	hdl.handle.net—CCR_C-2457_45bbaa1a-7002-2ecd-ab9d-57a189f694a6 <http://hdl.handle.net/11459/CCR_C-2457_45bbaa1a-7002-2ecd-ab9d-57a189f694a6>

	VLO Facet: 					license
	OLAC (DCMI):				dcterms:license
	DataCite:                	Rights
	IMDI Element:               	 
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionAdministrativeInfo](#collectionadministrativeinfo)

#### LicenceIdentifier
**Description:** &#x1F4A5; &#x1F4CC; The LicenceIdentifier provides the URI of the licence.

	Interface Facet:			display
	User provided:				yes

	ValueScheme:				anyURI
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	licence URL
	CCR URI:                	hdl.handle.net—CCR_C-6586_2c79d86a-5a75-0890-d407-7d9cb86b9beb <http://hdl.handle.net/11459/CCR_C-6586_2c79d86a-5a75-0890-d407-7d9cb86b9beb>

	VLO Facet: 					distributionType
	OLAC (DCMI):				dcterms:license
	DataCite:                	rightsURI
	IMDI Element:               —
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:			—

[Back to Top](#blam-collection-repository) | [Back to CollectionAdministrativeInfo](#collectionadministrativeinfo)

#### Access
**Description:** &#x1F4CC; This element specifies the terms of availability of the resource in plain words. The  technical implementation of these terms depends on the repository

	Interface Facet:			yes, browsing, display	
	User provided:				no		

	ValueScheme:				"open", "registration required", "request required" 
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	availability
	CCR URI:                	hdl.handle.net—CCR_C-2453_1f0c3ea5-7966-ae11-d3c6-448424d4e6e8 <http://hdl.handle.net/11459/CCR_C-2453_1f0c3ea5-7966-ae11-d3c6-448424d4e6e8>

	VLO Facet: 					availability
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               —   
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionAdministrativeInfo](#collectionadministrativeinfo)

#### AvailabilityDate
**Description:** &#x1F4CC; The AvailabilityDate element contains the date at which the bundle became, will become available. The date must be provided conforming to ISO 8601 in the form YYYY-MM-DD.


	Interface Facet:			yes, display	
	User provided:				no	

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	availability start date
	CCR URI:                	hdl.handle.net—CCR_C-6711_135e104e-9f0e-265a-0e6e-4e2325c8751e <http://hdl.handle.net/11459/CCR_C-6711_135e104e-9f0e-265a-0e6e-4e2325c8751e>

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	dateType:Available
	IMDI Element:               —
	ELDP-CMDI Element:          
	IMDI-CMDI Element:			—

[Back to Top](#blam-collection-repository) | [Back to CollectionAdministrativeInfo](#collectionadministrativeinfo)

#### RightsHolder
**Description:** The RightsHolder component contains informatin about the individual or institution owning or managing the rights over the resource. 

	Number of occurrences:		1-unbound

[Back to Top](#blam-collection-repository) | [Back to CollectionAdministrativeInfo](#collectionadministrativeinfo)

#### RightsHolderName
**Description:** &#x1F4A5; &#x1F4CC; The RightsHolderName contains the name of the individual or institution owning or managing the rights over the resource. 

	Interface Facet:			display
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	IPR Holder
	CCR URI:                	hdl.handle.net—CCR_C-6709_cb3572ed-ffd3-04f1-c145-b9c1f26bfc82 <http://hdl.handle.net/11459/CCR_C-6709_cb3572ed-ffd3-04f1-c145-b9c1f26bfc82>

	VLO Facet: 					rightsHolder
	OLAC (DCMI):				dcterms:rightsHolder
	DataCite:                	Contributor:contributorType:RightsHolder
	IMDI Element:               	
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) | [Back to CollectionAdministrativeInfo](#collectionadministrativeinfo)

#### RightsHolderIdentifier
**Description:** &#x1F4A5; The RightsHolderIdentifier contains an URI that uniquely identifies the rights holder. In the case of an individual this should be achieved using an established scheme. Best Practice: ORCID, ISNI If an individual cannot be referenced by an identifier at least an email address should be given.

	Interface Facet:			display
	User provided:				yes

	ValueScheme:				anyURI
	Number of occurrences:  	0-1
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:					Contributor:contributorType:RightsHolder:Identifier
	IMDI Element:               —      
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-collection-repository) | [Back to CollectionAdministrativeInfo](#collectionadministrativeinfo)

### CollectionStructuralInfo
**Description:** CollectionStructuralInfo contains structural metadata that describes the internal structure of the bundle.

	Number of occurrences:		1-1

- [CollectionAdditionalMetadataFile](#collectionadditionalmetadatafile)
	- [FilePID](#filepid) 
	- [MimeType](#mimetype)
	- [IsMetadataOf](#ismetadataof) &#x1F4A5;
	- [FileDescription](#filedescription)  &#x1F4A5;
- [CollectionAdditionalResource](#collectionadditionalresource)
	- [FilePID](#filepid) 
	- [MimeType](#mimetype)
	- [FileDescription](#filedescription)  &#x1F4A5;

[Back to Top](#blam-collection-repository) |  [Back to CollectionStructuralInfo](#collectionstructuralinfo)

#### CollectionAdditionalMetadataFile
**Description:** The CollectionAdditionalMetadataFile component contains metadata about additional metadata files contained in the collection.

	Number of occurrences:		0-unbound

[Back to Top](#blam-collection-repository) |  [Back to CollectionStructuralInfo](#collectionstructuralinfo)

##### FilePID
**Description:** &#x1F4CC; The FileID element contains a PID that uniquely identifies the file described by this component.

	Interface Facet:			full text, display
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

[Back to Top](#blam-collection-repository) |  [Back to CollectionStructuralInfo](#collectionstructuralinfo)

##### MimeType
**Description:** &#x1F4CC; Specification of the mime-type of the resource.

	Interface Facet:			no
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	mime type
	CCR URI:                	hdl.handle.net—CCR_C-2571_2be2e583-e5af-34c2-3673-93359ec1f7df <http://hdl.handle.net/11459/CCR_C-2571_2be2e583-e5af-34c2-3673-93359ec1f7df>

	VLO Facet: 					format
	OLAC (DCMI):				Format
	DataCite:                	Format
	IMDI Element:               	       
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) |  [Back to CollectionStructuralInfo](#collectionstructuralinfo)

##### IsMetadataOf
**Description:** &#x1F4A5; &#x1F4CC; The IsMetadataOf element contains a PID that uniquely identifies the file described by the file described in this component.

	Interface Facet:			no
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

[Back to Top](#blam-collection-repository) |  [Back to CollectionStructuralInfo](#collectionstructuralinfo)

##### FileDescription
**Description:** &#x1F4A5; The FileDescription contains a human readable, file specific description. This element should be used to provide file specific that cannot be added to the bundle description. 

	Interface Facet:			no	
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-1
	Multilingual:           	yes
	CCR prefLabel@en:       	description
	CCR URI:                	hdl.handle.net—CCR_C-2520_9eeedfb4-47d3-ddee-cfcb-99ac634bf1db <http://hdl.handle.net/11459/CCR_C-2520_9eeedfb4-47d3-ddee-cfcb-99ac634bf1db>

	VLO Facet: 					description
	OLAC (DCMI):				purl.org—description <http://purl.org/dc/terms/description>
	DataCite:        			Description
	IMDI Element:               	
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) |  [Back to CollectionStructuralInfo](#collectionstructuralinfo)

#### CollectionAddionalResource
**Description:** The CollectionAddionalResources contains metadata about additional files provided to make the collection more accessible or to provide further information about the collection.

	Number of occurrences:		1-1

[Back to Top](#blam-collection-repository) |  [Back to CollectionStructuralInfo](#collectionstructuralinfo)

##### FilePID
**Description:** &#x1F4CC; The FileID element contains a PID that uniquely identifies the file described by this component.

	Interface Facet:			yes, display
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

[Back to Top](#blam-collection-repository) |  [Back to CollectionStructuralInfo](#collectionstructuralinfo)

##### MimeType
**Description:** &#x1F4CC; Specification of the mime-type of the resource.

	Interface Facet:			yes, browsing
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	mime type
	CCR URI:                	hdl.handle.net—CCR_C-2571_2be2e583-e5af-34c2-3673-93359ec1f7df <http://hdl.handle.net/11459/CCR_C-2571_2be2e583-e5af-34c2-3673-93359ec1f7df>

	VLO Facet: 					format
	OLAC (DCMI):				Format
	DataCite:                	Format
	IMDI Element:               	       
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) |  [Back to CollectionStructuralInfo](#collectionstructuralinfo)

##### FileDescription
**Description:** &#x1F4A5; The FileDescription contains a human readable, file specific description. This element should be used to provide file specific that cannot be added to the bundle description. 

	Interface Facet:			no, full text	
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-1
	Multilingual:           	yes
	CCR prefLabel@en:       	description
	CCR URI:                	hdl.handle.net—CCR_C-2520_9eeedfb4-47d3-ddee-cfcb-99ac634bf1db

	VLO Facet: 					description
	OLAC (DCMI):				purl.org—description <http://purl.org/dc/terms/description>
	DataCite:        			Description
	IMDI Element:               	
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:

[Back to Top](#blam-collection-repository) |  [Back to CollectionStructuralInfo](#collectionstructuralinfo)
