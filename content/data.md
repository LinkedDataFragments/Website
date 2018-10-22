---
title: Data
order: 4
---

## Access datasets as Triple Pattern Fragments
[Triple Pattern Fragments](/concept/#tpf)
provide triple-pattern-based access to a dataset.
This enables **client-side querying** of live data with **high availability** at **low cost**.
You can access the datasets below as Triple Pattern Fragments,
and even perform [federated querying](http://client.linkeddatafragments.org/#datasources=http%3A%2F%2Ffragments.dbpedia.org%2F2014%2Fen;http%3A%2F%2Fdata.linkeddatafragments.org%2Fviaf;http%3A%2F%2Fdata.linkeddatafragments.org%2Fharvard&query=SELECT%20%3Fperson%20%3Fname%20%3Fbook%20%3Ftitle%20%7B%0A%20%20%20%20%3Fperson%20dc%3Asubject%20dbpedia%3ACategory%3ASwedish_Nobel_laureates.%0A%20%20%20%20%3FviafID%20schema%3AsameAs%20%3Fperson%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20schema%3Aname%20%3Fname.%0A%20%20%20%20%3Fbook%20dc%3Acontributor%20%5B%20foaf%3Aname%20%3Fname%20%5D%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20dc%3Atitle%20%3Ftitle.%0A%7D) over them.

### Triple Pattern Fragments hosted by [DBpedia](http://fragments.dbpedia.org/)
  - **[DBpedia](http://fragments.dbpedia.org/2014/en)**, the Linked Data version of Wikipedia
    _([query these fragments](http://fragments.dbpedia.org/))_

### Triple Pattern Fragments hosted by [Wikidata](https://www.wikidata.org/)
  - **[Wikidata](https://query.wikidata.org/bigdata/ldf)**, the free knowledge base
    _([query these fragments](http://ldfclient.wmflabs.org/))_

### Triple Pattern Fragments hosted by [LOD Laundromat](http://lodlaundromat.org/wardrobe/)
  - **[Dataset index](http://lodlaundromat.org/wardrobe/)**,
    more than 650,000 datasets from across the Web.

### Triple Pattern Fragments hosted for [DataSalon](http://www.datasalon.com/)
  - **[OrgRef](http://ldf-vivo.herokuapp.com/orgref)**,
    data about organizations (universities, colleges, schools, hospitals)

### Triple Pattern Fragments hosted by the [EWI project](http://ewi.mmlab.be/)

  - **[Contact details of cities in Flanders](http://ewi.mmlab.be/cd/all)**
    _([query these fragments](http://ewi.mmlab.be/query/#startFragment=http%3A%2F%2Fewi.mmlab.be%2Fcd%2Fall))_
  - **[Flemish company register](http://ewi.mmlab.be/ba/all)**
    _([query these fragments](http://ewi.mmlab.be/query/#startFragment=http%3A%2F%2Fewi.mmlab.be%2Fba%2Fall))_

### Triple Pattern Fragments hosted by [Between Our Worlds](https://betweenourworlds.org/)
  - **[The Between Our Worlds dataset](https://data.betweenourworlds.org)** provides Linked Open Data about anime series and movies.


### Triple Pattern Fragments hosted by us at [data.linkeddatafragments.org](http://data.linkeddatafragments.org/)

  - **[DBpedia](http://data.linkeddatafragments.org/dbpedia)**, the Linked Data version of Wikipedia
    _([query these fragments](http://client.linkeddatafragments.org/))_
  - **[GeoNames](http://data.linkeddatafragments.org/geonames)**, a dataset of countries and over 8 million placenames
  - **[LinkedGeoData](http://data.linkeddatafragments.org/linkedgeodata)**, OpenStreetMap as Linked Data
  - **[Wiktionary](http://data.linkeddatafragments.org/wiktionary)**, a dictionary of the English language
  - **[DBLP](http://data.linkeddatafragments.org/dblp)**, the Computer Science Bibliography
  - **[YAGO2s](http://data.linkeddatafragments.org/yago2s)**, a huge semantic knowledge base
  - **[EventMedia](http://data.linkeddatafragments.org/eventmedia?object=http%3A%2F%2Flinkedevents.org%2Fontology%2FEvent)**, an events data source from EURECOM
  - **[Ookaboo](http://data.linkeddatafragments.org/ookaboo)**, public domain and Creative Commons images, linked to DBpedia
  - …
  - **Your dataset?** [Contact us](mailto:ruben.verborgh@ugent.be?subject=Host%20my%20dataset) and we will add it for you!

## Query public datasets using Triple Pattern Fragments

You can execute SPARQL queries over these datasets with a [Triple Pattern Fragments client](/software/).

Clients are available as _standalone applications_, _libraries_, and as _Web applications_.
<br>
[Try the online Triple Pattern Fragments client](http://client.linkeddatafragments.org/)
and execute your own queries!

## Publish your own Triple Pattern Fragments
**You can host your dataset** in a queryable way at low cost and with high availability
using [a free server](/software/#server).
<br>
Deploy your own server easily on top of an existing dataset.
[Download your server.](/software/#server)

**Do you already publish Triple Pattern Fragments?**
<br>
[Let us know](mailto:ruben.verborgh@ugent.be?subject=I%20publish%20Linked%20Data%20Fragments), we'll add you to the list on this page!

**Do you want us to publish your dataset?**
<br>
Even though Triple Pattern Fragments only requires a light server,
we can [host your dataset for you](mailto:ruben.verborgh@ugent.be?subject=Host%20my%20dataset).
