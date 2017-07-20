# Basic Language Archive Metadata (Bundle Repository)

> **Blam** The standard blasty noise. The power of the blam can sometimes be measured by the size of the word when it is written, or by the number of exclamation marks at the end of the word.
> 			[urban dictionary](http://www.urbandictionary.com/define.php?term=blam&defid=305474)

Basic Language Archive Metadata (BLAM) is designed to provide basic metadata for language repositories. The metadata scheme maximises discoverability and user oriented information without a proliferation of data fields or work for the data producer. Basic Language Archive Metadata is a suite of [CMDI](https://www.clarin.eu/content/component-metadata) profiles and currently consist of two pairs of profiles: 

* BLAM Bundle Repository: described in this document [below](#blam-bundle-repository)
* BLAM Bundle User: [documentation](https://github.com/fxru/blam-metadata/blob/master/BLAMBundleUser.md)
* BLAM Collection Repository: [documentation](https://github.com/fxru/blam-metadata/blob/master/BLAMCollectionRepository.md)

BLAM Bundle Repository contains information about bundles as provided by the repository. Data producers are asked to submit a subset of this information during ingest. The BLAM Bundle User profile defines this subset of 40 data fields. The separate definition of the BLAM Bundle User profile enhances the usability for data producers and can be validated independently from the more comprehensive BLAM Bundle Repository profile. The Basic Language Archive Metadata Bundle User profile is intended to be the primary source of user input for BLAM Bundle Repository. However, BLAM Bundle Repository is designed to allow automatic import of information from other metadata formats. The formats actively considered are: 

* IMDI Metadata Format: [ISLE Meta Data Initative, Version 3.0.4 (2003)](https://tla.mpi.nl/imdi-metadata/)
* CMDI imdi-session-profile: [clarin.eu:cr1:p_1271859438204](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1271859438204&registrySpace=public)
* CMDI ELDP_Bundle: [clarin.eu:cr1:p_1407745711992](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1407745711992&registrySpace=public)
* CMDI lat-session: [clarin.eu:cr1:p_1407745712035](https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ap_1407745712035&registrySpace=public)  

The data fields that are transferred from BLAM Bundle User input are marked by &#x1F4A5; in this document.

BLAM Bundle Repository is designed with a focus on discoverability and display. Data producers can submit additional metadata information to document their data and their research. The preferred format are other CMDI profiles or comparably standardized metadata formats.

The data fields of BLAM Bundle Repository were defined to facilitate interoperability with metacatalogues, in particular [DataCite](https://search.datacite.org/), [OLAC](http://search.language-archives.org/), and [VLO](https://vlo.clarin.eu/).

* OLAC metadata: [specifications](http://www.language-archives.org/OLAC/metadata.html), [usage](http://www.language-archives.org/NOTE/usage.html)
* DataCite Metadata: [Schema 4.0](https://schema.datacite.org/meta/kernel-4.0/)
* CLARIN VLO facets: [facets mapping](https://lux17.mpi.nl/isocat/clarin/vlo/mapping/index.html)

Recommended tools to create BLAM metadata are [CMDI Maker](http://cmdi-maker.uni-koeln.de/), [COMEDI](http://clarino.uib.no/comedi/), and [Arbil](https://tla.mpi.nl/tools/tla-tools/arbil/).

BLAM! &#x1F4A5; That’s it, enjoy documenting your data!

## BLAM-Bundle-Repository

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

- [BundleID](#bundleid)
- [BundleDisplayTitle](#bundledisplaytitle) &#x1F4A5;
- [BundleDescription](#bundledescription) &#x1F4A5;
- [BundleKeywords](#bundlekeywords)
	- [BundleKeyword](#bundlekeyword) &#x1F4A5;
- [BundleObjectLanguages](#bundleobjectlanguages)
	- [BundleObjectLanguage](#bundleobjectlanguage)
		- [ObjectLanguageDisplayName](#objectlanguagedisplayname) &#x1F4A5;
		- [ObjectLanguageName](#objectlanguagename)
		- [ObjectLanguageISO639-3Code](#objectlanguageiso639-3code)
		- [ObjectLanguageGlottologCode](#objectlanguageglottologcode) &#x1F4A5;
		- [ObjectLanguageAlternativeNames](#objectlanguagealternativenames)
			+ [ObjectLanguageAlternativeName](#objectlanguagealternativename)
		- [ObjectLanguageTaxonomy](#objectlanguagetaxonomy)
			+ [ObjectLanguageLanguageFamily](#objectlanguagelanguagefamily)
- [BundleRecordingDate](#bundlerecordingdate) &#x1F4A5;
- [BundleLocation](#bundlelocation)
	- [BundleGeoLocation](#bundlegeolocation) &#x1F4A5;
	- [BundleLocationDisplayName](#bundlelocationdisplayname) &#x1F4A5;
	- [BundleLocationName](#bundlelocationname)
	- [BundleRegionDisplayName](#bundleregiondisplayname) &#x1F4A5;
	- [BundleRegionName](#bundleregionname) 
	- [BundleCountryDisplayName](#bundlecountrydisplayname)  &#x1F4A5;
	- [BundleCountryName](#bundlecountryname)
	- [BundleCountryCode](#bundlecountrycode) 

[Back to Top](#blam-bundle-repository)

#### BundleID
**Description:** The BundleID element contains an identifier that consistently and uniquely identifies the bundle described in the particular metadata token. The identifier should be generated by the repository during the ingest process.

**Attribute:** *identifierType* **Values:** *DOI, Handle, URN, Other* The identifierType attribute determines the identifier type used. Recommended practice is to have a DOI and a Handle for each bundle.

	Discovery:					no
	Display:					no
	User provided:				no

	ValueScheme: 				anyURI
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	resource name
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2573_ae7c2548-8a86-ab6e-7099-e28b7697d1a2
	
	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:               	Identifier 
	IMDI Element:				/METATRANSCRIPT/@ArchiveHandle
	ELDP-CMDI Element:      	—
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleDisplayTitle 
**Description:** &#x1F4A5; The BundleDisplayTitle element provides a human readable name of the bundle. It should contain a meaningful and recognisable title for the bundle. The content of the BundleDisplayTitle element will be used as the human readable identifier in interfaces. This field will be used as the human readable identifier for the bundle in citation and interfaces.

	Discovery:					searchable
	Display:					page, list
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
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
**Description:** &#x1F4A5; The BundleDescription element provides a human readable description of the bundle. It should contain a description of the content of the bundle. The content of the BundleDescription element will be used as the human readable description in interfaces. Its content can be queried by repositories for free-text metadata search.

	Discovery:					searchable
	Display:					page, list (snippet)
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
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
**Description:** &#x1F4A5; The ObjectLanguageDisplayName element contains the name of the object language in the version recommended by the data producer. Repositories should treat the name provided by this element as the primary language name when displaying the metadata in relation to this particular data set (e.g. collection or bundle). The repository may use alternative names provided by services such as Glottolog or Ethnologue to improve discoverability and to enhance browsing and search experience.

	Discovery:					searchable, browsing facet
	Display:					page, list
	User provided:				yes		

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	Language Name
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d

	VLO Facet: 					
	OLAC (DCMI):				http://purl.org/dc/terms/language
	DataCite:        			
	IMDI Element:               //Session/MDGroup/Content/Languages/Language/Name
	ELDP-CMDI Element:          
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### ObjectLanguageName
**Description:** The ObjectLanguageName element contains the name of the object language in the version as provided by services such as Glottolog or Ethnologue. 

	Discovery:					searchable, browsing facet
	Display:					page
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	Language Name
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d

	VLO Facet: 					languageCode
	OLAC (DCMI):				http://purl.org/dc/terms/language
	DataCite:        			
	IMDI Element:               
	ELDP-CMDI Element:          
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### ObjectLanguageISO639-3Code
**Description:**  The ObjectLanguageISO639-3 element contains an ISO 639-3 language code for the object language.

	Discovery:					no
	Display:					page
	User provided:				no

	ValueScheme:				[a-z]{3}
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	Language ID
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2482_08eded24-4086-7e3f-88e5-e0807fb01e17

	VLO Facet: 					languageCode
	OLAC (DCMI):				http://purl.org/dc/terms/language
	DataCite:        			Language
	IMDI Element:               //Session/MDGroup/Content/Languages/Language/Id
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

#### ObjectLanguageAlternativeNames
**Description:** The ObjectLanguageAlternativeNames component contains elements with alternative names for the object language as provided by services such as Glottolog or Ethnologue. 

	Number of occurrences:  	0-1

#### ObjectLanguageAlternativeName
**Description:** The ObjectLanguageAlternativeName element contains an alternative name of the object language as provided by services such as Glottolog or Ethnologue.

	Discovery:					searchable
	Display:					no
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
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

#### ObjectLanguageTaxonomy

**Description** The ObjectLanguageTaxonomy component contains elements with the name of the language family and sub-families or sub-groups the object language belongs to. The values are taken from Glottolog and given in the version as provided by this service. 

	Number of occurrences:  	0-1

#### ObjectLanguageLanguageFamily
**Description:** The ObjectLanguageLanguageFamily element contains the name of the language family and sub-families or sub-groups the object language belongs to. The values are taken from Glottolog and given in the version as provided by this service. 

	Discovery:					searchable, browsing facet
	Display:					no
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	Language Name
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d

	VLO Facet: 					
	OLAC (DCMI):				
	DataCite:        			
	IMDI Element:               
	ELDP-CMDI Element:          
	IMDI-CMDI Element:
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

#### BundleRecordingDate
**Description:** &#x1F4A5; The BundleRecordingDate element contains the date at which a recording occured. The date must be provided conforming to ISO 8601 in the form YYYY-MM-DD.

	Discovery:					searchable, browsing facet (collection)
	Display:					page
	User provided:				yes		

	ValueScheme:				date
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
**Description:** BundleLocation contains information about the most relevant or salient location in relation to the data contained in the bundle. The default location would be the location of recording. However, any other location regarded as the most relevant or salient location to the data can be set as the BundleLocation. The information provided in the component is intended for discoverability in map based browsing and keyword search as well as general display purposes. Detailed documentation of geographic information should be outsourced into an additional metadata file.

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
**Description:** &#x1F4A5; The BundleLocationDisplayName element contains the name of a location in the version recommended by the data producer. Repositories should treat the name provided by this element as the primary location name when displaying the metadata in relation to this particular data set (e.g. collection or bundle). The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance the browsing and search experience. The repository may also translate the name into other languages if no BundleLocationDisplayName name is given for a particular interface language. 

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

#### BundleLocationName
**Description:** The BundleLocationName element contains the name of a location provided by services such as GeoNames. This name is used to improve discoverability and to enhance the browsing and search experience. GeoNames field: *name* (or *toponymName*).

	Discovery:					searchable
	Display:					no
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	place name
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-5580_03e458f2-f873-8645-76eb-40e001b6c1ac

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        
	IMDI Element:				//Session/MDGroup/Location/Address
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

#### BundleRegionName
**Description:** The BundleRegionName element contains the name of an administrative subdivision provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. GeoNames field: *adminName1* 

	Discovery:					searchable, browsing facet
	Display:					no
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
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
**Description:** &#x1F4A5; The BundleCountryDisplayName element contains the name of the country to which the location belongs in the version recommended by the data producer. Repositories should treat the name provided by this element as the primary country name when displaying the metadata in relation to this particular data set (e.g. collection or bundle). The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no BundleCountryDisplayName name is given for a particular interface language.  

	Discovery:					searchable
	Display:					page
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	0-1
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

#### BundleCountryName
**Description:** The BundleCountryName element contains the name of the country as provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. GeoNames field: *countryName*

	Discovery:					searchable, browsing facet
	Display:					no
	User provided:				no	

	ValueScheme:				string
	Number of occurrences:  	1-1
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

#### BundleCountryCode
**Description:** The CountryCode element contains the ISO 3166-1 alpha 2 code of the country of the location as provided by services such as GeoNames GeoNames field: *countryCode*

	Discovery:					no
	Display:					no
	User provided:				no

	ValueScheme:				[A-Z]{2}
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	country coding
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2092_36cd7ca8-e412-9f29-7ea7-4a3ba4ba2c91

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			—
	IMDI Element:               —
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—
	lat-session:				

[Back to Top](#blam-bundle-repository) | [Back to BundleGeneralInfo](#bundlegeneralinfo)

### BundlePublicationInfo
**Description:** The BundlePublicationInfo component contains metadata pertaining the publication of the resource. The information provided in this component is used for display and in particular to generate bibliographical references to the resource.

	Number of occurrences:		1-1

- [BundleCreators](#bundlecreators) 
	- [BundleCreator](#bundlecreator)
		- [CreatorName](#creatorname)
			+ [CreatorFamilyName](#creatorfamilyname) &#x1F4A5;
			+ [CreatorGivenName](#creatorgivenname) &#x1F4A5;
		- [CreatorNameIdentifier](#creatornameidentifier) &#x1F4A5;
		- [CreatorAffiliation](#creatoraffiliation) &#x1F4A5;
- [BundlePublicationYear](#bundlepublicationyear) &#x1F4A5;
- [BundleDataProvider](#bundledataprovider)
- [BundleContributors](#bundlecontributors)
	- [BundleContributor](#bundlecontributor)
		- [ContributorName](#contributorname)
			+ [ContributorFamilyName](#contributorfamilyname) &#x1F4A5;
			+ [ContributorGivenName](#contributorgivenname) &#x1F4A5;
		- [ContributorNameIdentifier](#contributornameidentifier) &#x1F4A5;
		- [ContributorAffiliation](#contributoraffiliation) &#x1F4A5;
		- [ContributorRole] (#contributorrole) &#x1F4A5;

[Back to Top](#blam-bundle-repository)

#### BundleCreators
**Description:** The BundleCreator component contains information about the creator or creators of the resource. BundleCreators are treated as creators of the resource and thus similar to authors in respect to quotation, references, and metadata display. Other individuals involved in the production or processing of the resource should be added as [BundleContributors](bundlecontributors).

	Number of occurrences:		1-1

[Back to Top](#blam-bundle-repository) | [Back to BundlePublicationInfo](#bundlepublicationinfo)

##### BundleCreator
**Description:** The BundleCreator component contains information about the creator of the resource. 

	Number of occurrences:		1-unbounded

[Back to Top](#blam-bundle-repository) | [Back to BundlePublicationInfo](#bundlepublicationinfo)

###### CreatorName
**Description:** The CreatorName component contains the name of the creator. The value of this field can be used to generate a bibliographical citation reference for the resource. This usage should guide the formatting.

	CCR prefLabel@en:       	creator
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-6836_d35e73a8-ec72-d3c4-e39a-4b0fefd32cdc

[Back to Top](#blam-bundle-repository) |  [Back to BundlePublicationInfo](#bundlepublicationinfo)

###### CreatorFamilyName
**Description:** &#x1F4A5; The CreatorFamilyName element contains the part of the name of the creator that should be treated as the family name when generating a citation for the resource. This usage should guide the decision which part belongs into this field.

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

###### CreatorGivenName
**Description:** &#x1F4A5; The CreatorGivenName element contains the part of the name of the creator that should be treated as the given name when generating a citation for the resource. This usage should guide the decision.

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
	Number of occurrences:  	0-unbounded
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
**Description:** &#x1F4A5; BundlePublicationYear contains the year of publication in the form YYYY conforming to ISO 8601. The default value is the ingest date into the repository unless an embargo has been set for the resource. In that case, the end year of the embargo is taken as the year of publication. For legacy data, the  value of BundlePublicationDate can be set to a point before the ingest. The value of this field should be used to generate a bibliographical citation reference for the resource. 

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

#### BundleDataProvider
**Description:** BundleDataProvider contain the name of the data providing entity. The default value would be the name of the repository or its holding institution. The value of this field can be used to generate a bibliographical citation reference for the resource. 
			
	Discovery:					no
	Display:					citation
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	publisher
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-6134_72c22724-2615-fd70-2eff-8cd3cb59e91d

	VLO Facet: 					—
	OLAC (DCMI):				Publisher
	DataCite:        			Publisher
	IMDI Element:               —
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) |  [Back to BundlePublicationInfo](#bundlepublicationinfo)

#### BundleContributors
**Description:** The BundleContributors component contains information about contributors to the resource. BundleContributors are not treated as authors in respect to quotation, references, and metadata display.

	Number of occurrences:		0-1

[Back to Top](#blam-bundle-repository) | [Back to BundlePublicationInfo](#bundlepublicationinfo)

##### BundleContributor
**Description:** The BundleContributor component contains information about a contributor to the resource. 

	Number of occurrences:		1-unbounded

[Back to Top](#blam-bundle-repository) | [Back to BundlePublicationInfo](#bundlepublicationinfo)

###### ContributorName
**Description:** The ContributorName component contains the name of the creator. The value of this field may be used to generate a bibliographical citation reference for the resource. This usage should guide the formatting.

[Back to Top](#blam-bundle-repository) |  [Back to BundlePublicationInfo](#bundlepublicationinfo)

###### ContributorFamilyName
**Description:** &#x1F4A5; The ContributorFamilyName element contains the part of the name of the contributor that should be treated as the family name when generating a citation for the resource. This usage should guide the decision.

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

###### ContributorGivenName
**Description:** &#x1F4A5; The ContributorGivenName element contains the part of the name of the contributor that should be treated as the given name when generating a citation for the resource. This usage should guide the decision.

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
	Number of occurrences:  	0-unbounded
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

###### ContributorRole
**Description:** &#x1F4A5; The ContributorRole contains the organisational or institutional affiliation of the contributor as provided by the depositor.

	Discovery:					—
	Display:					page
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:        			Creator:contributorType
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
	Number of occurrences:  	1-1
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
**Description:** &#x1F4A5; The ProjectDescription element provides a human readable description of the project including full project name. It should contain a description of the project’s objective or activity. The content of the ProjectDescription element will be used as the human readable description in interfaces. Its content can be queried by repositories for free-text metadata search.

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	1-1
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

	ValueScheme:				anyURI
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
		- [TranslationLanguageName](#translationlanguagename)
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

#### TranslationLanguageName
**Description:** The TranslationLanguageName element describes the annotation of the type translation. It contains the name of the language used in the translation. Data with no Translation metadata will be treated as not translated by the repository. Data with several Translation elements will be treated as having several translations.

	Discovery:					searchable, browsing facet
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
	IMDI Element:               —   
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

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
	- [LicenseName](#licensename)
	- [LicenseIdentifier](#licenseidentifier) &#x1F4A5;
- [Access](#access) 
- [AvailabilityDate](#availabilitydate)
- [RightsHolder](#rightsholder)
	- [RightsHolderName](#rightsholdername)  &#x1F4A5;
	- [RightsHolderIdentifier](#rightsholderidentifier) &#x1F4A5;

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

#### LicenseName
**Description:** The LicenseName element should provide the complete human readable name of a license and include version information if applicable.

	Discovery:					searchable, browsing facet
	Display:					page	
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	license
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2457_45bbaa1a-7002-2ecd-ab9d-57a189f694a6

	VLO Facet: 					license
	OLAC (DCMI):				dcterms:license
	DataCite:                	Rights
	IMDI Element:               	 
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

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

#### Access
**Description:** This element specifies the terms of availability of the resource in plain words. The  technical implementation of these terms depends on the repository.

	Discovery:					searchable, browsing facet
	Display:					page, list	
	User provided:				no		

	ValueScheme:				"open", "registration required", "request required" 
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	availability
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2453_1f0c3ea5-7966-ae11-d3c6-448424d4e6e8

	VLO Facet: 					availability
	OLAC (DCMI):				—
	DataCite:                	—
	IMDI Element:               —   
	ELDP-CMDI Element:          	
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) | [Back to BundleAdministrativeInfo](#bundleadministrativeinfo)

#### AvailabilityDate
**Description:** The AvailabilityDate element contains the date at which the bundle became or will become available. The date must be provided conforming to ISO 8601 in the form YYYY-MM-DD.


	Discovery:					no
	Display:					page	
	User provided:				no	

	ValueScheme:				date
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	availability start date
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-6711_135e104e-9f0e-265a-0e6e-4e2325c8751e

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:                	dateType:Available
	IMDI Element:               —
	ELDP-CMDI Element:          
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to BundleAdministrativeInfo](#bundleadministrativeinfo)

#### RightsHolder
**Description:** The RightsHolder component contains information about the individual or institution owning or managing the rights in regard to the resource. 

	Number of occurrences:		1-unbounded

[Back to Top](#blam-bundle-repository) | [Back to BundleAdministrativeInfo](#bundleadministrativeinfo)

#### RightsHolderName
**Description:** &#x1F4A5; The RightsHolderName contains the name of the individual or institution owning or managing the rights over the resource. 

	Discovery:					searchable
	Display:					page
	User provided:				yes	

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	IPR Holder
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-6709_cb3572ed-ffd3-04f1-c145-b9c1f26bfc82

	VLO Facet: 					rightsHolder
	OLAC (DCMI):				dcterms:rightsHolder
	DataCite:                	Contributor:contributorType:RightsHolder
	IMDI Element:               	
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) | [Back to BundleAdministrativeInfo](#bundleadministrativeinfo)

#### RightsHolderIdentifier
**Description:** &#x1F4A5; The RightsHolderIdentifier contains a URI that uniquely identifies the rights holder. In the case of an individual, this should be achieved by using an established scheme. Best Practice: ORCID, ISNI If an individual cannot be referenced by an identifier an email address should be given (in the form of a mailto URI).

**Attribute** *identifierType*: ORCID and ISNI are considered best practices. An email address in the form of a mailto URI is the recommended fallback. *Values*: ORCID, ISNI, Email, Other

	Discovery:					searchable
	Display:					page
	User provided:				yes

	ValueScheme:				anyURI
	Number of occurrences:  	0-unbounded
	Multilingual:           	no
	CCR prefLabel@en:       	—
	CCR URI:                	—

	VLO Facet: 					—
	OLAC (DCMI):				—
	DataCite:					Contributor:contributorType:RightsHolder:Identifier
	IMDI Element:               —      
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) | [Back to BundleAdministrativeInfo](#bundleadministrativeinfo)

### BundleStructuralInfo
**Description:** BundleStructuralInfo contains structural metadata that describes the internal structure of the bundle.

	Number of occurrences:		1-1

- [BundleIsPartOfCollection](#bundleispartofcollection) 
- [BundleAdditionalMetadataFile](#bundleadditionalmetadatafile)
	- [FileName](#filename-metadatafile) &#x1F4A5; 
	- [FilePID](#filepid-metadatafile) 
	- [MimeType](#mimetype-metadatafile)
	- [IsMetadataOf](#ismetadataof-metadatafile) &#x1F4A5;
	- [FileDescription](#filedescription-metadatafile)  &#x1F4A5;
- [BundleResources](#bundleresources)
	- [MediaResource](#mediaresource)
		- [FileName](#filename-mediaresource) &#x1F4A5;
		- [FilePID](#filepid-mediaresource) 
		- [MimeType](#mimetype-mediaresource)
		- [FileLength](#filelength-mediaresource)
		- [FileDescription](#filedescription-mediaresource)  &#x1F4A5;
	- [WrittenResource](#writtenresource)
		- [FileName](#filename-writtenresource) &#x1F4A5;
		- [FilePID](#filepid-writtenresource) 
		- [MimeType](#mimetype-writtenresource)
		- [IsAnnotationOf](#isannotationof-writtenresource) &#x1F4A5;
		- [FileDescription](#filedescription-writtenresource)  &#x1F4A5; 
	- [OtherResource](#otherresource)
		- [FileName](#filename-otherresource) &#x1F4A5;
		- [FilePID](#filepid-otherresource) 
		- [MimeType](#mimetype-otherresource)
		- [FileDescription](#filedescription-otherresource)  &#x1F4A5;

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

#### BundleIsPartOfCollection
**Description:** The BundleIsIPartOfCollection element contains a PID or DOI that uniquely identifies the collection the resource is part of.

**Attribute:** *IdentifierType* **Values:** *DOI, Handle* The IdentifierType attribute determines the identifier type used.

	Discovery:					no
	Display:					page
	User provided:				no

	ValueScheme:				anyURI
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	relation role
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-6570_90018537-4ab9-0cfe-c878-257b9b311993

	VLO Facet: 					—
	OLAC (DCMI):				Relation:dcterms:isPartOf
	DataCite:                	RelatedIdentifier:relationType:IsIPartOf
	IMDI Element:               —       
	ELDP-CMDI Element:          —
	IMDI-CMDI Element:			—

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

#### BundleAdditionalMetadataFile
**Description:** The BundleAdditionalMetadataFile component contains metadata about additional metadata files contained in the bundle.

	Number of occurrences:		0-unbounded

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

##### FileName (MetadataFile)
**Description:** &#x1F4A5; The FileName element contains the name of the file as provided by the depositor.

	Discovery:					no
	Display:					page
	User provided:				yes		

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

##### FilePID (MetadataFile)
**Description:** The FileID element contains a PID that uniquely identifies the file described by this component.

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

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

##### MimeType (MetadataFile)
**Description:** Specification of the mime-type of the resource.

	Discovery:					searchable, browsing facet
	Display:					page, list
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	mime type
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2571_2be2e583-e5af-34c2-3673-93359ec1f7df

	VLO Facet: 					format
	OLAC (DCMI):				Format
	DataCite:                	Format
	IMDI Element:               	       
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

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
	Number of occurrences:  	0-1
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
	User provided:				yes		

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

###### FilePID (MediaResource)
**Description:** The FileID element contains a PID that uniquely identifies the file described by this component.

	Discovery:					no
	Display:					page
	User provided:				no		

	ValueScheme:				anyURI
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

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

###### MimeType (MediaResource)
**Description:** Specification of the mime-type of the resource.

	Discovery:					searchable, browsing facet
	Display:					page, list
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	mime type
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2571_2be2e583-e5af-34c2-3673-93359ec1f7df

	VLO Facet: 					format
	OLAC (DCMI):				Format
	DataCite:                	Format
	IMDI Element:               	       
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

###### FileLength (MediaResource)
**Description:** The FileLength element contains the length of a media file.

	Discovery:					browsing facet
	Display:					page, list
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	duration
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2567_8e616d60-5708-c3d4-320b-661399ccda43

	VLO Facet: 					—
	OLAC (DCMI):				Format:dcterms:extent
	DataCite:                	—
	IMDI Element:               	       
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

###### FileDescription (MediaResource)
**Description:** &#x1F4A5; The FileDescription contains a human readable, file specific description. This element should be used to provide file specific that cannot be added to the bundle description. Any information applicable to the whole bundle should be added to the BundleDescription element.

	Discovery:					searchable
	Display:					page	
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-1
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
	User provided:				yes		

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

###### FilePID (WrittenResource)
**Description:** The FileID element contains a PID that uniquely identifies the file described by this component.

	Discovery:					no
	Display:					page
	User provided:				no		

	ValueScheme:				anyURI
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

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

###### MimeType (WrittenResource)
**Description:** Specification of the mime-type of the resource.

	Discovery:					searchable, browsing facet
	Display:					page, list
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	mime type
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2571_2be2e583-e5af-34c2-3673-93359ec1f7df

	VLO Facet: 					format
	OLAC (DCMI):				Format
	DataCite:                	Format
	IMDI Element:               	       
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

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
	Number of occurrences:  	0-1
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
	User provided:				yes		

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

###### FilePID (OtherResource)
**Description:** The FileID element contains a PID that uniquely identifies the file described by this component.

	Discovery:					no
	Display:					page
	User provided:				no		

	ValueScheme:				anyURI
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

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

###### MimeType (OtherResource)
**Description:** Specification of the mime-type of the resource.

	Discovery:					searchable, facet
	Display:					page, list
	User provided:				no

	ValueScheme:				string
	Number of occurrences:  	1-1
	Multilingual:           	no
	CCR prefLabel@en:       	mime type
	CCR URI:                	http://hdl.handle.net/11459/CCR_C-2571_2be2e583-e5af-34c2-3673-93359ec1f7df

	VLO Facet: 					format
	OLAC (DCMI):				Format
	DataCite:                	Format
	IMDI Element:               	       
	ELDP-CMDI Element:          
	IMDI-CMDI Element:

[Back to Top](#blam-bundle-repository) |  [Back to BundleStructuralInfo](#bundlestructuralinfo)

###### FileDescription (OtherResource)
**Description:** &#x1F4A5; The FileDescription contains a human readable, file specific description. This element should be used to provide file specific that cannot be added to the bundle description. Any information applicable to the whole bundle should be added to the BundleDescription element.

	Discovery:					searchable
	Display:					page	
	User provided:				yes

	ValueScheme:				string
	Number of occurrences:  	0-1
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
