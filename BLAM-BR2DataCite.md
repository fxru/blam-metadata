# Mapping Basic Language Archive Metadata to DataCite

> **Blam** The standard blasty noise. The power of the blam can sometimes be measured by the size of the word when it is written, or by the number of exclamation marks at the end of the word.
>           [urban dictionary](http://www.urbandictionary.com/define.php?term=blam&defid=305474)


## Basic Language Archive Metadata (Bundle Repository)

ID | Status | Occ. | DataCite Name | BLAM
---|--------|------|---------------|------
ID 1 | M | 1 | Identifier | BundleID::identifierType(DOI) 
ID 1.1 | M | 1 | identifierType | BundleID::identifierType
ID 2 | M | 1 | Creator | BundleCreator
ID 2.1 | M | 1 | creatorName | 
ID 2.2 | M | 0-n | nameIdentifier | CreatorNameIdentifier
ID 2.2.1 | M | 1 | nameIdentifierScheme | 
ID 2.2.2 | O | 0-1 | scheme URI | 
ID 2.3 | O | 0-n | affiliation |
ID 3 | M | 1-n | Title |
ID 4 | M | 1 | Publisher |
ID 5 | M |  1 | PublicationYear |
ID 6 | R | 0-n | Subject |
ID 7 | R | 0-n | Contributor | 
ID 8 | R | | Date | 
ID 9 | O | | Language | 
ID 10 | M | 1 | ResourceType |
ID 10.1 | M | 1 |  resourceTypeGeneral | "Audiovisual"
ID 11 | O | | AlternateIdentifier | BundleID::identifierType(Handle)
ID 12 | O | | RelatedIdentifier |
ID 16 | O | | Rights | 
ID 17 | R | | Description | 
ID 18 | R | | GeoLocation |
ID 19 | O | | FundingReference |


## Basic Language Archive Metadata (Collection Repository)


