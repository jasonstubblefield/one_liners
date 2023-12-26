Delete everything

`<delete><query>*:*</query></delete>`

Build the suggest handler

`http://solr.example.com:8983/solr/mySuggestionCollection/suggesthandler?suggest.build=true&suggest.q=pipe`

Geofilter Syntax

`{!geofilt sfield=latlng pt=34.138333,-118.660833 d=100}`

Geofilter query examples

`http://localhost:9999/solr/inspector_geo/select?fq={!geofilt%20sfield=latlng%20pt=34.138333,-118.660833%20d=1000}&rows=1000&wt=csv&q={!func}geodist()&sfield=latlng&pt=34.138333,-118.660833&sort=score+asc&fl=*,score`

`http://localhost:8983/solr/timm/select?fq={!geofilt%20sfield=latlng%20pt=38.9035778,-77.0186828%20d=1000}&rows=1000&wt=csv&q={!func}geodist()&sfield=latlng&pt=38.9035778,-77.0186828&sort=score+asc`

Creating a Solr Collection in cloud mode with the solr api

`http://localhost:8983/solr/admin/cores?action=CREATE&name=testCore&instanceDir=/var/solr/data/testCore&config=solrconfig.xml&dataDir=data&configSet=/opt/solr/server/solr/configsets/_default`