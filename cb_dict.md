# Data dictionary: CrunchBase companies in the UK

## Source

CrunchBase

## Provenance

The raw data are tables capturing various dimensions of an organision in the CrunchBase dataset.
This [https://github.com/nestauk/cb_jiawen](repo) documents how the data have been merged and enriched

## Last update

TA

## Enrichment

The data has been enriched in the following ways:

* We have aggregated categories into a smaller number of sectors through a community detection in the network of category co-occurrences
* We have created a very crude flag for whether a company is 'AI' or not by searching for relevant terms in the long description.

This is all documented in the [https://github.com/nestauk/cb_jiawen](project repo.)

## Known issues

TBA


|name|type|observations|
|----|----|----|
|id|<class 'str'>|  Entity id |
|company_name|<class 'str'>|  Entity name |
|roles|<class 'str'>|  Entity role  - we have filtered out any entity without a company role |
|homepage_url|<class 'str'>|  Company website |
|country|<class 'str'>|  Country |
|state_code|<class 'NoneType'>| Country ISO code  |
|region|<class 'str'>|  Region |
|city|<class 'str'>|  City |
|location_id|<class 'str'>|  id for the location |
|address|<class 'str'>| Address  |
|status|<class 'str'>|  Is the company active |
|short_description|<class 'str'>|  Short (<140 character) description of company activities |
|funding_rounds|<class 'numpy.int64'>|  How many rounds has the company received |
|funding_total_usd|<class 'numpy.float64'>|  Amount of funding |
|founded_on|<class 'pandas._libs.tslib.Timestamp'>|  When was the company founded |
|last_funding_on|<class 'pandas._libs.tslib.NaTType'>| When did the company receive its latest funding  |
|closed_on|<class 'pandas._libs.tslib.NaTType'>|   |
|employee_count|<class 'str'>| Number of employees  |
|cb_url|<class 'str'>|  Link in CrunchBase |
|twitter_url|<class 'NoneType'>|  Link in Twitter |
|aliases|<class 'NoneType'>|  Other names |
|created_at|<class 'pandas._libs.tslib.Timestamp'>|  When was the data collected |
|updated_at|<class 'pandas._libs.tslib.Timestamp'>|  When was the data updated |
|primary_role|<class 'str'>|  Primary role (almost always company) |
|type|<class 'str'>|  Type of entity (always an organisation) |
|long_description|<class 'float'>|  Longer description |
|category_name|<class 'list'>|  Categories (sectors or areas of activity that the company has been labelled with) |
|ai_text_n|<class 'numpy.float64'>| How many times do AI related terms appear in the text  |
|ai_cats|<class 'numpy.bool_'>|  Does AI appear in the categories |
|ai_flag|<class 'numpy.bool_'>|  Positive if AI related terms appear in the description at least once |
|founded_year|<class 'numpy.float64'>|  Year when it was founded |
|sector_list|<class 'list'>|  List of aggregated sectors that the company is related with |