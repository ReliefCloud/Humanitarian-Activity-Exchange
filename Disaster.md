
|Field|	Description|
|---|---|
|url	|Canonical URL of entry.|
|name|	Name assigned to the disaster based on ReliefWeb disaster naming convention.|
|glide|	GLobal IDEntifier number (GLIDE) of the disaster.|
|current	|Deprecated, use "status" instead Boolean flag to indicate if the disaster is active or inactive.
|featured	|Boolean flag to indicate if the disaster is featured on the ReliefWeb home page.
description	Description of the disaster in Markdown format.
description-html	Description of the disaster in HTML format.
date	Date when the event occurred (ISO 8601).
date.created	Date when the entry was created on ReliefWeb (ISO 8601)
primary_country	Container for primary country fields. Primary country is the single country most relevant to the entry.
primary_country.id	Unique identifier of the primary country.
primary_country.name	Name of the primary country in English. See list of taxonomy terms.
primary_country.shortname	Short name of the primary country. See list of taxonomy terms.
primary_country.iso3	ISO 3166-1 alpha-3 code of the primary country.
country	Container for country fields.
country.id	Unique identifier of the country.
country.primary	Boolean flag to indicate if the country is a primary country.
country.name	Name of the country in English. See list of taxonomy terms.
country.shortname	Short name of the source, typically a well-known acronym e.g. "UNICEF"
country.iso3	ISO 3166-1 alpha-3 code of the country.
primary_type	Containter for primary disaster type assigned to the disaster.
primary_type.id	Unique identifier of the primary disaster type of the disaster.
primary_type.name	Name of the primary disaster type assigned to the entry.
status	Status of the disaster (current, alert or past)
type	Containter for disaster types assigned to the disaster.
type.id	Unique identifier of the disaster type of the disaster. See list of taxonomy terms.
type.primary	Primary disaster type assigned to the disaster assigned to entry. See list of taxonomy terms.
type.name	Name of the disaster type assigned to the entry. See list of taxonomy terms.

 {
    "id": 11880,
    "name": "Zimbabwe: Floods - Jan 2013",
    "description": "Heavy rains starting on 7 Jan 2013 have affected an estimated 8,490 people across Zimbabwe, out of which 4,615 require humanitarian assistance in the form of emergency shelter and/or non-food items (blankets, clothes, cooking utensils, hygiene packs). The heavy downpours have also caused major damage to agricultural lands, destroying maize crops (the main staple), as well as disrupting public services such as road transportation and education. The main provinces requiring humanitarian response are in Matebeleland South, Matebeleland North, Manicaland, Mashonaland Central, Masvingo and Midlands. ([OCHA, 25 Jan 2013](http://reliefweb.int/node/552634))\r\n\r\nBy February, the meteorological department reported that the country had received the peak of rainfall for the season and that while more rains are expected, they should not cause major flooding incidents ([OCHA, 8 Feb 2013](http://reliefweb.int/node/556868)).\r\n\r\n###Useful Links\r\n- [Zimbabawe Humanitarian Response](http://zw.humanitarianresponse.info/)",
    "status": "past",
      "date": {
          "created": "2013-01-18T00:00:00+00:00"
      },
    "glide": "FL-2013-000011-ZWE",
    "featured": false,
    "primary_country": {
          "href": "http://api.rwlabs.org/v1/countries/257",
          "id": 257,
          "name": "Zimbabwe",
          "iso3": "zwe",
          "location": [
              29.94,
              -19.19
          ]
          },
    "primary_type": {
          "id": 4611,
          "name": "Flood",
          "code": "FL"
            },
          "country": [
               {
                        "href": "http://api.rwlabs.org/v1/countries/257",
                        "id": 257,
                        "name": "Zimbabwe",
                        "iso3": "zwe",
                        "location": [
                            29.94,
                            -19.19
                        ],
                        "primary": true
                    }
                ],
                "type": [
                    {
                        "id": 4624,
                        "name": "Flash Flood",
                        "code": "FF"
                    },
                    {
                        "id": 4611,
                        "name": "Flood",
                        "code": "FL",
                        "primary": true
                    }
                ],
                "url": "http://reliefweb.int/taxonomy/term/11880",
                "description-html": "<p>Heavy rains starting on 7 Jan 2013 have affected an estimated 8,490 people across Zimbabwe, out of which 4,615 require humanitarian assistance in the form of emergency shelter and/or non-food items (blankets, clothes, cooking utensils, hygiene packs). The heavy downpours have also caused major damage to agricultural lands, destroying maize crops (the main staple), as well as disrupting public services such as road transportation and education. The main provinces requiring humanitarian response are in Matebeleland South, Matebeleland North, Manicaland, Mashonaland Central, Masvingo and Midlands. (<a href=\"http://reliefweb.int/node/552634\">OCHA, 25 Jan 2013</a>)</p>\n\n<p>By February, the meteorological department reported that the country had received the peak of rainfall for the season and that while more rains are expected, they should not cause major flooding incidents (<a href=\"http://reliefweb.int/node/556868\">OCHA, 8 Feb 2013</a>).</p>\n\n<h3>Useful Links</h3>\n\n<ul>\n<li><a href=\"http://zw.humanitarianresponse.info/\">Zimbabawe Humanitarian Response</a></li>\n</ul>\n",
                "current": false
            },
