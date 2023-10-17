Dev Log


Start with seeing if there is an existing database to use for searching and end when you can place species near you on a map with an overlay


1. Does the data Exist?

Start by searching the [[GBIF]] API for species based on location and radius to that location with
```
https://api.gbif.org/v1/occurrence/search?decimalLatitude=37&decimalLongitude=-122&radius=10
```

Results Example


```
https://api.gbif.org/v1/occurrence/search?decimalLatitude=${roundedLatitude}&decimalLongitude=${roundedLongitude}&radius=10&limit=20

```


```json
  "results": [
        {
            "key": 4416833921,
            "datasetKey": "50c9509d-22c7-4a22-a47d-8c48425ef4a7",
            "publishingOrgKey": "28eb1a3f-1c15-4a95-931a-4af90ecb574d",
            "installationKey": "997448a8-f762-11e1-a439-00145eb45e9a",
            "hostingOrganizationKey": "28eb1a3f-1c15-4a95-931a-4af90ecb574d",
            "publishingCountry": "US",
            "protocol": "DWC_ARCHIVE",
            "lastCrawled": "2023-10-12T07:21:20.328+00:00",
            "lastParsed": "2023-10-12T19:56:08.812+00:00",
            "crawlId": 402,
            "extensions": {
                "http://rs.gbif.org/terms/1.0/Multimedia": [
                    {
                        "http://rs.tdwg.org/dwc/terms/catalogNumber": "321210828",
                        "http://purl.org/dc/terms/references": "https://www.inaturalist.org/photos/321210828",
                        "http://purl.org/dc/terms/format": "image/jpeg",
                        "http://purl.org/dc/terms/identifier": "https://inaturalist-open-data.s3.amazonaws.com/photos/321210828/original.jpeg",
                        "http://purl.org/dc/terms/rightsHolder": "Gina Barton",
                        "http://purl.org/dc/terms/publisher": "iNaturalist",
                        "http://purl.org/dc/terms/creator": "Gina Barton",
                        "http://purl.org/dc/terms/created": "2023-09-19T18:30:00Z",
                        "http://purl.org/dc/terms/license": "http://creativecommons.org/licenses/by-nc/4.0/",
                        "http://purl.org/dc/terms/type": "StillImage"
                    }
                ]
            },
            "basisOfRecord": "HUMAN_OBSERVATION",
            "occurrenceStatus": "PRESENT",
            "taxonKey": 3906623,
            "kingdomKey": 6,
            "phylumKey": 7707728,
            "classKey": 220,
            "orderKey": 1354,
            "familyKey": 4689,
            "genusKey": 9601650,
            "speciesKey": 3906623,
            "acceptedTaxonKey": 3906623,
            "scientificName": "Notholithocarpus densiflorus (Hook. & Arn.) Manos, Cannon & S.H.Oh",
            "acceptedScientificName": "Notholithocarpus densiflorus (Hook. & Arn.) Manos, Cannon & S.H.Oh",
            "kingdom": "Plantae",
            "phylum": "Tracheophyta",
            "order": "Fagales",
            "family": "Fagaceae",
            "genus": "Notholithocarpus",
            "species": "Notholithocarpus densiflorus",
            "genericName": "Notholithocarpus",
            "specificEpithet": "densiflorus",
            "taxonRank": "SPECIES",
            "taxonomicStatus": "ACCEPTED",
            "iucnRedListCategory": "LC",
            "dateIdentified": "2023-09-20T00:02:02",
            "decimalLatitude": 37.0,
            "decimalLongitude": -122.0,
            "continent": "NORTH_AMERICA",
            "stateProvince": "California",
            "gadm": {
                "level0": {
                    "gid": "USA",
                    "name": "United States"
                },
                "level1": {
                    "gid": "USA.5_1",
                    "name": "California"
                },
                "level2": {
                    "gid": "USA.5.44_1",
                    "name": "Santa Cruz"
                }
            },
            "year": 2023,
            "month": 9,
            "day": 19,
            "eventDate": "2023-09-19T11:30:00",
            "issues": [
                "CONTINENT_DERIVED_FROM_COORDINATES",
                "TAXON_MATCH_TAXON_ID_IGNORED"
            ],
            "modified": "2023-09-20T00:33:44.000+00:00",
            "lastInterpreted": "2023-10-12T19:56:08.812+00:00",
            "references": "https://www.inaturalist.org/observations/184055102",
            "license": "http://creativecommons.org/licenses/by-nc/4.0/legalcode",
            "identifiers": [
                {
                    "identifier": "184055102"
                }
            ],
            "media": [
                {
                    "type": "StillImage",
                    "format": "image/jpeg",
                    "references": "https://www.inaturalist.org/photos/321210828",
                    "created": "2023-09-19T18:30:00.000+00:00",
                    "creator": "Gina Barton",
                    "publisher": "iNaturalist",
                    "license": "http://creativecommons.org/licenses/by-nc/4.0/",
                    "rightsHolder": "Gina Barton",
                    "identifier": "https://inaturalist-open-data.s3.amazonaws.com/photos/321210828/original.jpeg"
                }
            ],
            "facts": [],
            "relations": [],
            "isInCluster": **false**,
            "datasetName": "iNaturalist research-grade observations",
            "recordedBy": "Gina Barton",
            "identifiedBy": "Gina Barton",
            "geodeticDatum": "WGS84",
            "class": "Magnoliopsida",
            "countryCode": "US",
            "recordedByIDs": [],
            "identifiedByIDs": [],
            "country": "United States of America",
            "rightsHolder": "Gina Barton",
            "identifier": "184055102",
            "http://unknown.org/nick": "gina-barton",
            "verbatimEventDate": "2023/09/19 11:30 AM",
            "verbatimLocality": "San Mateo County, CA, USA",
            "gbifID": "4416833921",
            "collectionCode": "Observations",
            "occurrenceID": "https://www.inaturalist.org/observations/184055102",
            "taxonID": "69823",
            "catalogNumber": "184055102",
            "institutionCode": "iNaturalist",
            "eventTime": "11:30:00-07:00",
            "http://unknown.org/captive": "wild",
            "identificationID": "409820966"
        },
```





Can we put evertying on a frontend map interface?
1. Make a map interface which gets your locaiton
2. Pass the lcoation into the API
3. Return the results 
4. Make the UX good
5. 