# Streamtools for Open Data, MozFest 2014: Resources

Want to explore the world of open government & civic data without having to write parsers? Or perhaps you don't know how to code? Bring your laptop to this session and learn how to work with data in realtime with the Streamtools GUI! 


Here are data sources and streamtools patterns for the session.

## Vote with your phone

This is just fun.

* vote at http://vote.nytlabs.com/
* [results](http://vote.nytlabs.com/results.html)

## Open Data

* Crisis.net: reporting on ebola, syria, etc
* Wikipedia Edits: monitor changes to a single page or overall (list users, etc)
* FDA: Food Recalls
* CDC: Vaccine Reactions
* TFL: Barclay's Bikes
* UK: Police Data
* UK: Traffic Accidents
* UK: Restaurant Ratings

## Crisis.net

* **Endpoint** http://api.crisis.net/item
* **Examples** 
  * [ebola](http://api.crisis.net/item?tags=ebola&apikey=535a9fa06a2165d01fabc678)
  * [syria](http://api.crisis.net/item?placeName=Syria&apikey=535a9fa06a2165d01fabc678)
* **Patterns**
  * [ebola](https://gist.github.com/jacqui/65a50358eddc450d72e6)
  * [syria](https://gist.github.com/jacqui/1da5bfe59ea91f6893e7)

## Wikipedia Edits

Connects to Wikipedia's websocket endpoint and monitors edits. Concepts: websocket, filtering, histogram/bucketed counts, masking/keeping what you want in the data.

* **Endpoint** ws://wikimon.hatnote.com:80/en
* **API Key** n/a
* **Pattern** [builds histogram of non-robot/anon uses](https://gist.github.com/jacqui/4ea7b086d8da688b7385)

### FDA: Food Recalls

* **data** https://api.fda.gov/food/enforcement.json?api_key=JwWMMFxvcd95fmcGmahxmUbis3te4cYPEozY81eP&limit=25
* **pattern**

### CDC: Vaccine Reactions

* [data](https://api.enigma.io/v2/data/2d7e8330098f1146ff192effbdb03f71/us.gov.cdc.vaers.symptoms.2014?conjunction=and)
* [pattern](https://gist.github.com/jacqui/dc91d8de272a2f00f742)

## UK: Police Data

Crimes reported near MozFest!

* [data](http://data.police.uk/api/crimes-street/all-crime?lat=51.5017355&lng=0.0055388000000675675&date=2014-08) [cached copy](https://raw.githubusercontent.com/jacqui/mozfest_open_data/master/data.police.uk/crime_data_mozfest.json)
* [pattern](https://raw.githubusercontent.com/jacqui/mozfest_open_data/master/data.police.uk/pattern_crime_data_mozfest.json)

## UK: Barclay's Bikes

* [data](http://www.tfl.gov.uk/tfl/syndication/feeds/cycle-hire/livecyclehireupdates.xml) [cached copy](https://raw.githubusercontent.com/jacqui/mozfest_open_data/master/tfl.gov.uk/bch/availability.xml)

## UK: Traffic Accidents

* [data](http://hatrafficinfo.dft.gov.uk/feeds/datex/England/UnplannedEvent/content.xml) [cached copy](https://raw.githubusercontent.com/jacqui/mozfest_open_data/master/data.gov.uk/traffic/content1.xml)
* [pattern](https://gist.github.com/jacqui/5c3cb20c6a95b0ef48e7)

## UK: Restaurant Ratings (Greenwich)

* [data/xml](http://ratings.food.gov.uk/OpenDataFiles/FHRS511en-GB.xml) [cached copy](https://raw.githubusercontent.com/jacqui/mozfest_open_data/master/data.gov.uk/ratings/greenwich.xml)
* [pattern/xml](https://gist.github.com/jacqui/1336a99d2b534591d2ea)

* [data/json](http://api.ratings.food.gov.uk/Help/Api/GET-Establishments_name_address_longitude_latitude_maxDistanceLimit_businessTypeId_schemeTypeKey_ratingKey_ratingOperatorKey_localAuthorityId_countryId_sortOptionKey_pageNumber_pageSize)
* [pattern/json](https://gist.github.com/jacqui/7b125e3b7c4b24e2a23f)
