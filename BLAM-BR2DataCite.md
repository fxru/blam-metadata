# Mapping Basic Language Archive Metadata to DataCite

> **Blam** The standard blasty noise. The power of the blam can sometimes be measured by the size of the word when it is written, or by the number of exclamation marks at the end of the word.
>           [urban dictionary](http://www.urbandictionary.com/define.php?term=blam&defid=305474)

This document provides a mapping table between a subset of DataCite metadata data fields (including all mandatory ones) and the equivalent data fields of  BLAM Bundle Repository.

## Basic Language Archive Metadata (Bundle Repository)

ID | Status | Occ. | DataCite Name | BLAM XPATH
---|--------|------|---------------|------
ID 1 | M | 1 | Identifier | /CMD/Components//BundleGeneralInfo/BundleID[@identifierType="DOI"]  
ID 1.1 | M | 1 | identifierType | /CMD/Components//BundleGeneralInfo/BundleID/@identifierType
ID 2 | M | 1 | (Creator) | (BundleCreator)
ID 2.1 | M | 1 | creatorName | /CMD/Components//BundlePublicationInfo/BundleCreators/BundleCreator/CreatorDisplayName
ID 2.2 | M | 0-n | nameIdentifier | /CMD/Components//BundlePublicationInfo/BundleCreators/BundleCreator/CreatorNameIdentifier[@identifierType="ORCID"]
ID 2.2.1 | M | 1 | nameIdentifierScheme | `ORCID`
ID 2.2.2 | O | 0-1 | scheme URI | `http://orcid.org`
ID 2.3 | O | 0-n | affiliation | /CMD/Components//BundlePublicationInfo/BundleCreators/BundleCreator/CreatorAffiliation
ID 3 | M | 1-n | Title | if (/CMD/Components//BundleGeneralInfo/BundleDisplayTitle/@lang='en') then /CMD/Components//BundleGeneralInfo/BundleDisplayTitle[@lang='en'] else /CMD/Components//BundleGeneralInfo/BundleDisplayTitle
ID 4 | M | 1 | Publisher | /CMD/Components//BundlePublicationInfo/BundleDataProvider
ID 5 | M |  1 | PublicationYear | /CMD/Components//BundlePublicationInfo/BundlePublicationYear
ID 6 | R | 0-n | Subject | /CMD/Components//BundleGeneralInfo//BundleKeywords/BundleKeyword
ID 7 | R | 0-n | (Contributor) | (BundleContributor) 
ID 7.1 | | 1 | contributorName | /CMD/Components//BundlePublicationInfo/BundleContributors/BundleContributor/ContributorDisplayName
ID 7.3 | | 0-n | nameIdentifier | /CMD/Components//BundlePublicationInfo/BundleContributors/BundleContributor/ContributorNameIdentifier[@identifierType="ORCID"]
ID 7.3.1 | M | 1 | nameIdentifierScheme | `ORCID`
ID 7.3.2 | O | 0-1 | scheme URI | `http://orcid.org`
ID 7.4 | | 0-n | affiliation | /CMD/Components//BundlePublicationInfo/BundleContributors/BundleContributor/ContributorAffiliation
ID 8 | R | 0-n | Date | /CMD/Components//BundleGeneralInfo/BundleRecordingDate \| /CMD/Components//BundleAdministrativeInfo/AvailabilityDate
ID 8.1 | | 1 | dateType | `Collected` \| `Available`
ID 9 | O | 0-1 | Language | /CMD/Components//BundleGeneralInfo/BundleObjectLanguages/BundleObjectLanguage/ObjectLanguageISO639-3Code
ID 10 | M | 1 | ResourceType | `Bundle with audio-visual resources`
ID 10.1 | M | 1 |  resourceTypeGeneral | `Audiovisual`
ID 11 | O | 0-n | AlternateIdentifier | /CMD/Components//BundleGeneralInfo/BundleID[@identifierType="Handle"]
ID 11.1 | | 1 | alternateIdentifierType | `Handle`
ID 12 | O | 0-n | RelatedIdentifier | /CMD/Components//BundleAdministrativeInfo/BundleIsIdenticalTo \| /CMD/Components//BundleAdministrativeInfo/BundleIsDerivedFrom \| /CMD/Components//BundleStructuralInfo/BundleIsPartOfCollection \| /CMD/Components//BundleStructuralInfo/BundleResources//FilePID
ID 12.1 | | 1 | relatedIdentifierType | `Handle`
ID 12.2 | | 1 | relationType | `IsIdenticalTo` \| `IsDerivedFrom` \| `IsPartOf` \| `HasPart`
ID 16 | O | 0-n | Rights | /CMD/Components//BundleAdministrativeInfo/Licence/LicenceName
ID 16.1 | | 0-1 | rightsURI | /CMD/Components//BundleAdministrativeInfo/Licence/LicenceIdentifier
ID 17 | R | 0-n | Description | if (/CMD/Components//BundleGeneralInfo/BundleDescription/@lang='en') then /CMD/Components//BundleGeneralInfo/BundleDescription[@lang='en'] else /CMD/Components//BundleGeneralInfo/BundleDisplayTitle 
ID 17.1 | | 1 | descriptionType | `abstract`
ID 18 | R | 0-n | (GeoLocation) | (BundleLocation) 
ID 18.1 | | 0‐1 | (geoLocationPoint) | (BundleGeoLocation)
ID 18.1.1 | | 1 | pointLongitude | /CMD/Components//BundleGeneralInfo/BundleLocation/BundleGeoLocation/substring-after(., ' ')
ID 18.1.2 | | 1 | pointLatitude | /CMD/Components//BundleGeneralInfo/BundleLocation/BundleGeoLocation/substring-before(., ' ')
ID 19 | O | 0-n | (FundingReference) | (FunderInfo)
ID 19.1 | | 1 | funderName | /CMD/Components//ProjectInfo/Project/FunderInfos/FunderInfo/FunderName
ID 19.2 | | 0-1 | funderIdentifier | /CMD/Components//ProjectInfo/Project/FunderInfos/FunderInfo/FunderIdentifier/@FunderIdentifier
ID 19.3 | | 0-1 | funderIdentifierType | /CMD/Components//ProjectInfo/Project/FunderInfos/FunderInfo/FunderIdentifier/@FunderIdentifierType
ID 19.3 | | 0-1 | awardNumber | /CMD/Components//ProjectInfo/Project/FunderInfos/FunderInfo/GrantIdentifier
ID 19.3.1 | | 0-1 | awardURI | /CMD/Components//ProjectInfo/Project/FunderInfos/FunderInfo/GrantURI
ID 19.4 | | 0-1 | awardTitle | /CMD/Components//ProjectInfo/Project/ProjectDisplayName
