# Language Archive Metadata V 0.1

The Language Archive Core and Language Archive Core (Repository) profiles aim to provide a basic metadata profile for language repositories. The profiles cover fundamental domain specific, but project independent, descriptive metadata as well as depositor input to administrative and structural metadata.

The design goal is a set of metadata categories that can be used  across different research projects as well as across different repositories and institutional contexts. 

Separate profiles for administrative and structural metadata are in development, but different institutions are likely have different requirements, so that a consensus on a single administrative profile and a general structural profile across different institutional settings is unrealistic.

The design of the Language Archive Core focuses on discoverability via the archive interface and search portals such as OLAC and VLO. The Language Archive Core (Repository) profile adds automatically generated and system internal metadata. Defining and resleasing a subset of Language Archive Repository as a separate CMDI profile ensures that users can provide valid XML files and makes metadata validation and quality control during the ingest easier.

Projects are encouraged to provide and archive further, project-specific metadata through project specific metadata profiles (or formats) or different general CMDI profiles.

---------------------------------------

[Profiles], [Components], [Elements]

---------------------------------------


## Profiles

* [LangArchCore Collection]
* [LangArchCore Collection (Repository)]
* [LangArchCore Bundle] 
* [LangArchCore Bundle (Repository)]
* LangArchCore Admninstrative (external link)

### LangArchCore Collection ###

**Description:**

**Components:**

* [CollectionGeneralInfo] `Component` `Number of occurrences: 1-1`
* [Legal] `Component` `Number of occurrences: 1-1`
* [ObjectLanguage] `Component` `Number of occurrences: 1-unbounded`
* [Location] `Component` `Number of occurrences: 1-1`

### LangArchCore Collection  (Repository) ###

**Description:**

**Components:**

* [CollectionGeneralInfo] `Component` `Number of occurrences: 1-1`
* [Legal] `Component` `Number of occurrences: 1-1`
* [ObjectLanguage] `Component` `Number of occurrences: 1-unbounded`
* [Location] `Component` `Number of occurrences: 1-1`
* [Project] `Component` `Repository only` `Number of occurrences: 0-1`


### LangArchCore Bundle ###

**Description:**

**Components:**

* [BundleGeneralInfo] `Component` `Number of occurrences: 1-1`
* [ObjectLanguage] `Component` `Number of occurrences: 1-unbounded`
* [Location] `Component` `Number of occurrences: 1-1`
* [Persons] `Component` `Number of occurrences: 1-unbounded`
* [Files] `Component`

### LangArchCore Bundle  (Repository) ###

**Description:**

**Components:**

* [BundleGeneralInfo] `Component` `Number of occurrences: 1-1`
* [ObjectLanguage] `Component` `Number of occurrences: 1-unbounded`
* [Location] `Component` `Number of occurrences: 1-1`
* [Persons] `Component` `Number of occurrences: 1-unbounded`
* [Files] `Component` `Number of occurrences: 1-unbounded`

---------------------------------------

## Components

### CollectionGeneralInfo
* [CollectionID] `Element` `Repository only`
* [CollectionDisplayName] `Element`
* [CollectionDescription] `Element`
* [CollectionKeywords] `Element`

### BundleGeneralInfo
* [BundleID] `Element` `Repository only`
* [BundleDisplayName] `Element`
* [BundleDescription] `Element`
* [BundleKeywords] `Element`

### ProjectGeneralInfo
* [ProjectID] `Element` `Repository only`
* [ProjectDisplayName] `Element`
* [ProjectDescription] `Element`
* [ProjectKeywords] `Element`

**Comment:**
	https://catalog.clarin.eu/ds/ComponentRegistry#/?itemId=clarin.eu%3Acr1%3Ac_1422885449330&registrySpace=public

### Legal
* [ResponsiblePerson] `Component` `Number of occurrences: 1-1`
	- [Contact] `Component` `Number of occurrences: 1-unbounded`
* [Licence] `Element`

### ObjectLanguage
* [Language] `Component` `Number of occurrences: 1-unbounded`

### Location
* [GeoCoordinates] `Element`
* [LocationDisplayName] `Element`
* [AdministrativeSubdivision] `Element`
* [CountryDisplayName] `Element`
* [ContinentDisplayName] `Element`

### Persons
* [Participant] `Component` `Number of occurrences: 1-unbounded`

### Participant
* [PersonName] `Element`
* [SortbyName] `Element`
* [Gender] `Element`
* [DateOfBirth] `Element`
* L1 `Component` `Number of occurrences: 1-unbounded`
	- [Language] `Component` `Number of occurrences: 1-unbounded`
* L2 `Component` `Number of occurrences: 0-unbounded`
	- [Language] `Component` `Number of occurrences: 1-unbounded`
* [Role] `Element`


### Language
* [ISO 639-3] `Element`
* [Glottolog] `Element`
* [LanguageDisplayname] `Element`

### ResponsiblePerson
* [Contact] `Component` `Number of occurrences: 1-unbounded`

### Contact
* [Name] `Element`
* [PostalAdress] `Element`
* [Email] `Element`


### Files
* [File Name] `Element`
* [File Hash] `Element` `Repository only`
* [File PID] `Element` `Repository only`
* [MimeType] `Element`

## Repository Components

### Project
* [ProjectGeneralInfo] `Component` `Number of occurrences: 1-1`

---------------------------------------

## Elements

### Elements: CollectionGeneralInfo

#### CollectionID

**Description:** The CollectionID element contains an identifier that consistently and uniquely identifies the entity described in the particular metadata token (collection, bundle, or project). The identifier should be a PID and is usually generated by the repository during the ingest process.

	ValueScheme: 			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		resource name
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2544_3626545e-a21d-058c-ebfd-241c0464e7e5
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### CollectionDisplayName

**Description:** The CollectionDisplayName element provides a human readable name of the collection. It should contain a meaningful and recognisable title for the collection. The content of the CollectionDisplayName element will be used as the humanreadable identifier in interfaces. Data providers can provide CollectionDisplayName values for multiple interface languages.

	ValueScheme: 			string
	Number of occurrences: 	1-1
	Multilingual:			yes
	CCR prefLabel@en:		resource title
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2545_d873f2ab-2a2f-29d6-a9ab-260cde57f227
	VLO Facet: 				name
	OLAC (DCMI):			http://purl.org/dc/terms/title
	ELDP-CMDI Element:		
	IMDI-CMDI Element:

#### CollectionDescription

**Description:** The CollectionDescription element provides a human readable description of the collection. It should contain q description of the content of the collection. The content of the CollectionDescription element will be used as the humanreadable description in interfaces. Its content can be queried by repositories for free-text metadata search. Data providers can provide CollectionDescription values for multiple interface languages.

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			yes
	CCR prefLabel@en:		description
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2520_9eeedfb4-47d3-ddee-cfcb-99ac634bf1db
	VLO Facet: 				description
	OLAC (DCMI):			http://purl.org/dc/terms/description
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### CollectionKeywords

**Description:** CollectionKeywords should be used to describe the content and nature of data to enhance the discoverability and facilitate a finer granularity of searches and browsing of the data. Repositories can use keyword metadata to define meaningful subsets of the data and provide a better browsing experience.

**Examples:** `elicited` `dialogue` `ritual speech` `kinship` `creation myth` `planned discourse`

	ValueScheme: 			string
	Number of occurrences: 	0-unbounded
	Multilingual:			yes
	CCR prefLabel@en:		metadata tag
	CCR URI:				http://hdl.handle.net/11459/CCR_C-5436_6ab57c2c-5f8d-3561-6db6-d75da23d2637
	VLO Facet: 				keywords
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:


### Elements: BundleGeneralInfo

#### BundleID

**Description:** The BundleID element contains an identifier that consistently and uniquely identifies the bundle described in the particular metadata token. The identifier should be a PID and is usually generated by the repository during the ingest process.

	ValueScheme: 			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		resource name
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2544_3626545e-a21d-058c-ebfd-241c0464e7e5
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### BundleDisplayName

**Description:** The BundleDisplayName element provides a human readable name of the bundle. It should contain a meaningful and recognisable title for the bundle. The content of the CollectionDisplayName element will be used as the humanreadable identifier in interfaces. Data providers can provide BundleDisplayName values for multiple interface languages.

	ValueScheme: 			string
	Number of occurrences: 	1-1
	Multilingual:			yes
	CCR prefLabel@en:		resource title
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2545_d873f2ab-2a2f-29d6-a9ab-260cde57f227
	VLO Facet: 				name
	OLAC (DCMI):			http://purl.org/dc/terms/title
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### BundleDescription

**Description:** The BundleDescription element provides a human readable description of the bundle. It should contain a description of the content of the collection. The content of the BundleDescription element will be used as the humanreadable description in interfaces. Its content can be queried by repositories for free-text metadata search. Data providers can provide BundleDescription values for multiple interface languages.

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			yes
	CCR prefLabel@en:		description
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2520_9eeedfb4-47d3-ddee-cfcb-99ac634bf1db
	VLO Facet: 				description
	OLAC (DCMI):			http://purl.org/dc/terms/description
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### BundleKeywords

**Description:** BundleKeywords should be used to describe the content and nature of data to enhance the discoverability and facilitate a finer granularity of searches and browsing of the data. Repositories can use 

**Examples:** `elicited` `dialogue` `ritual speech` `kinship` `creation myth` `planned discourse`

	ValueScheme: 			string
	Number of occurrences: 	0-unbounded
	Multilingual:			yes
	CCR prefLabel@en:		metadata tag
	CCR URI:				http://hdl.handle.net/11459/CCR_C-5436_6ab57c2c-5f8d-3561-6db6-d75da23d2637
	VLO Facet: 				keywords
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

### Elements: ProjectGeneralInfo

#### ProjectID

**Description:** The ProjectID element contains an identifier that consistently and uniquely identifies the project described in the particular metadata token. The identifier should be a PID and is usually generated by the repository during the ingest process.

	ValueScheme: 			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		project name
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2536_13fc5f10-c14a-1f64-a669-32736f6d3ef5
	VLO Facet: 				projectName
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### ProjectDisplayName

**Description:** The ProjectDisplayName element provides a human readable name of the project. It should contain official name of the project. The content of the ProjectDisplayName element will be used as the humanreadable identifier in interfaces. Data providers can provide ProjectDisplayName values for multiple interface languages.

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			yes
	CCR prefLabel@en:		project title
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2537_fa206273-223a-f4fa-dde3-ba59b965701f
	VLO Facet: 				projectName
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### ProjectDescription

**Description:** The ProjectDescription element provides a human readable description of the project. It should contain a description of the project. The content of the ProjectDescription element will be used as the humanreadable description in interfaces. Data providers can provide ProjectDescription values for multiple interface languages. 

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			yes
	CCR prefLabel@en:		description
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2520_9eeedfb4-47d3-ddee-cfcb-99ac634bf1db
	VLO Facet: 				description
	OLAC (DCMI):			http://purl.org/dc/terms/description
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### ProjectKeywords ???

**Description:** 

	ValueScheme:
	Number of occurrences: 	
	Multilingual:			
	CCR prefLabel@en:		
	CCR URI:				
	VLO Facet: 
	OLAC (DCMI):			
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

### Legal

### Licence 

**Description:** The Licence element contains a reference to a licence, ideally a PID, but URIs are also accepted. Repositories are free to provide a list of acceptable values for this element. 

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		availability
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2453_1f0c3ea5-7966-ae11-d3c6-448424d4e6e8
	VLO Facet: 				license
	OLAC (DCMI):			http://purl.org/dc/terms/license
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

### Language

#### ISO 639-3

**Description:** The ISO639-3 element contains a ISO 639-3 language code.


	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		Language ID
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2482_08eded24-4086-7e3f-88e5-e0807fb01e17
	VLO Facet: 				languageCode
	OLAC (DCMI):			http://purl.org/dc/terms/language
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### Glottolog

**Description:** The Glottolog element contains a Glottolog language code.

	ValueScheme: 			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		—	
	CCR URI:				—
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:		—	
	IMDI-CMDI Element:		—

#### LanguageDisplayname

**Description:** The LanguageDisplayName element contains the name of a language in the version recommended by the data producer. Repositories should tread the name provided by this element as the primary language name when displaying the metadata in relation to this particular data set (e.g. collection or bundle).The repository may use alternative names provided by services such as Glottolog or Ethnologue to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no language name is given for a particular interface language. Data providers can provide LanguageDisplayName values for multiple interface languages. 

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			yes
	CCR prefLabel@en:		Language Name
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2484_669684e7-cb9e-ea96-59cb-a25fe89b9b9d
	VLO Facet: 				languageCode
	OLAC (DCMI):			http://purl.org/dc/terms/language
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

### Location

#### GeoCoordinates

**Description:** The GeoCoordinate element contains a geocoordinate conforming to ISO 6709. 

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		geographical coordinates
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2523_283c7b54-06ed-3d6c-4bb0-c8a79a8236fd
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### LocationDisplayName

**Description:** The LocationDisplayName element contains the name of a location in the version recommended by the data producer. Repositories should tread the name provided by this element as the primary location name when displaying the metadata in relation to this particular data set (e.g. collection or bundle).The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no LocationDisplayName name is given for a particular interface language. Data providers can provide LocationDisplayName values for multiple interface languages. 

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			yes
	CCR prefLabel@en:		place name
	CCR URI:				http://hdl.handle.net/11459/CCR_C-5580_03e458f2-f873-8645-76eb-40e001b6c1ac
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### AdministrativeSubdivision

**Description:** The AdministrativeSubdivision element optionally contains the name of a administrative subdevision such as state or province in the version recommended by the data producer. The data producer can decided which level of subdivision is relevant and will improve discoverability. Repositories should tread the name provided by this element as the primary location name when displaying the metadata in relation to this particular data set (e.g. collection or bundle). The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no AdministrativeSubdivision name is given for a particular interface language. Data providers can provide AdministrativeSubdivision values for multiple interface languages.

**Examples:** `Alaska` `Kerala` `Kent` 


	ValueScheme:			string
	Number of occurrences: 	0-1
	Multilingual:			yes
	CCR prefLabel@en:		location region
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2533_fa6e1812-e29b-3cf6-e15a-50aa34b9be68
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### CountryDisplayName

**Description:** The CountryDisplayName element contains the name of the country to which the location belongs in the version recommended by the data producer. Repositories should tread the name provided by this element as the primary country name when displaying the metadata in relation to this particular data set (e.g. collection or bundle). The repository may use alternative names provided by services such as GeoNames to improve discoverability and to enhance browsing and search experience. The repository may also translate the name into other languages if no CountryDisplayName name is given for a particular interface language. Data providers can provide CountryDisplayName values for multiple interface languages.  

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			yes
	CCR prefLabel@en:		location country
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2532_d004b0a6-fd1d-3ca3-abf1-1e6aeb3e37b2
	VLO Facet: 				country
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### ContinentDisplayName ???

**Description:**  

	ValueScheme:
	Number of occurrences: 	
	Multilingual:			
	CCR prefLabel@en:		
	CCR URI:				
	VLO Facet: 
	OLAC (DCMI):			
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

### Participant
#### PersonName

**Description:** The PersonName element contains the name of a person. The data provider determines what is the proper form of a name to reference a participant. If the name contains more than one name (e.g. given name and surname,) the culturally adequate order of names should be used.

**Examples:** `George W. Bush` `Alexander von Humboldt` `Mao Zedong` 

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		participant full name
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2556_d852af6c-c978-30ab-45aa-31cb9eaf11c4
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### SortbyName

**Description:** The SortByName element contains the name of a person in a form that lends itself to alphabetical sorting. The data provider determines what is the proper order of names for an alphabetically sorted list.

**Examples:** `Bush, George W.` `Humboldt, Alexander von` `Mao Zedong`

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		—
	CCR URI:				—
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### Gender

**Description:** The Gender element contains a term for the gender identification of the participant.  

**Examples:** `male` `female` `hijra` 

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		participant sex
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2560_ebb466e1-2b6b-6701-4e64-94618b4b455b
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### DateOfBirth

**Description:** The DateOfBirth component contains the date of birth of the person. The date must be provided conforming to ISO 8601. 

**Examples: `2016-03-19` `1970-01-01` 

	ValueScheme:			string
	Number of occurrences: 	1-1
	Multilingual:			no
	CCR prefLabel@en:		participant birthdate
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2551_6a3c9287-a92d-89e5-e537-9d0ff14bbdc2
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### Role

**Description:** The Role element specifies the role the person had in relation to the bundle. The repository and tools are encouraged to supply a list of recommended vocabulary.

**Examples:** `speaker` `researcher` `transcriber` `translator` `recorder` `curator`

	ValueScheme:			string
	Number of occurrences: 	1-unbounded
	Multilingual:			no
	CCR prefLabel@en:		participant role
	CCR URI:				http://hdl.handle.net/11459/CCR_C-2559_edfe42c0-c0e0-9bf9-671d-60e3d075be81
	VLO Facet: 				—
	OLAC (DCMI):			—
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

### Contact
#### Name

	Description: 

	ValueScheme:
	Number of occurrences: 	
	Multilingual:			
	CCR prefLabel@en:		
	CCR URI:				
	VLO Facet: 
	OLAC (DCMI):			
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### PostalAdress

	Description: 

	ValueScheme:
	Number of occurrences: 	
	Multilingual:			
	CCR prefLabel@en:		
	CCR URI:				
	VLO Facet: 
	OLAC (DCMI):			
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### Email

	Description: 

	ValueScheme:
	Number of occurrences: 	
	Multilingual:			
	CCR prefLabel@en:		
	CCR URI:				
	VLO Facet: 
	OLAC (DCMI):			
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

### File
#### File Name

	Description: 

	ValueScheme:
	Number of occurrences: 	
	Multilingual:			
	CCR prefLabel@en:		
	CCR URI:				
	VLO Facet: 
	OLAC (DCMI):			
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### File Hash

	Description: 

	ValueScheme:
	Number of occurrences: 	
	Multilingual:			
	CCR prefLabel@en:		
	CCR URI:				
	VLO Facet: 
	OLAC (DCMI):			
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### File PID

	Description: 

	ValueScheme:
	Number of occurrences: 	
	Multilingual:			
	CCR prefLabel@en:		
	CCR URI:				
	VLO Facet: 
	OLAC (DCMI):			
	ELDP-CMDI Element:			
	IMDI-CMDI Element:

#### MimeType

	Description: 

	ValueScheme:
	Number of occurrences: 	
	Multilingual:			
	CCR prefLabel@en:		
	CCR URI:				
	VLO Facet: 
	OLAC (DCMI):			
	ELDP-CMDI Element:			
	IMDI-CMDI Element:
