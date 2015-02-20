|Field|	Description|
|---|----|
|url|	Canonical URL of entry.|
|title|	Title of entry.|
|body	|Body of entry in Markdown format.|
|body-html	|Body of entry in HTML format.|
|how_to_apply	|Application instructions for the job.
|how_to_apply-html	Application instructions for the job in HTML format.
|date	Container for date fields.
|date.created	Date when the entry was created on ReliefWeb (ISO 8601)
|date.changed	Date when the entry was last modified on ReliefWeb (ISO 8601).
|date.closing	Date when the Job will close to applicants (ISO 8601).
|language	Container for language fields. Defaults to language.common.
|language.id	Unique identifier of the language the entry is written in.
|language.name	Language the entry is written in. See list of taxonomy terms.
|language.code	ISO 639-1 code of the language the entry is written in.
|country	Container for country fields.
country.id	Unique identifier of the country.
country.primary	Boolean flag to indicate if the country is a primary country.
country.name	Name of the country in English. See list of taxonomy terms.
country.shortname	Short name of the country in English. See list of taxonomy terms.
country.iso3	ISO 3166-1 alpha-3 code of the country.
city	Container for city fields.
city.id	Unique identifier of the city.
city.name	Name of the city in English.
source	Container for source fields.
source.id	Unique identifier of the source of the entry.
source.name	Name of the source in frequently-used form.
source.shortname	Short name of the source, typically a well-known acronym e.g. "UNICEF"
source.longname	Official full name of the source if different from source.name.
source.homepage	URL of the source's home page on primary website.
source.type	Container for source type fields. Defaults to source.type.common.
source.type.id	Unique identifier of the source type. See list of taxonomy terms.
source.type.name	Organization type of source. See list of taxonomy terms.
theme.id	Unique identifier of theme assigned to entry. See list of taxonomy terms.
theme.name	Theme assigned to entry. See list of taxonomy terms.
type.id	Unique identifier of job type. See list of taxonomy terms.
type.name	Name of the job type in English.
experience.id	Unique identifier for the number of years of experience required for the job. See list of taxonomy terms.
experience.name	Number of years of experience required for the job. See list of taxonomy terms.
career_categories	Container for career cateories field. Defaults to career_categories.common.
career_categories.id	Unique identifier for the career category. See list of taxonomy terms.
career_categories.name	Name of the career category in English. See list of taxonomy terms.
file.id	Unique identifier of the file attachment.
file.mimetype	MIME type of the file attachment.
file.filename	File name of the attachment.
file.description	Description of the file attachment.
file.url	URL of the file attachment.
