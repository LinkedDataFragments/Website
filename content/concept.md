---
title: Concept
order: 3
---

## Linked Data Fragments: a uniform view on all Linked Data interfaces
Today's Web offers three common ways to access Linked Data:

- A **data dump** contains all triples in an entire dataset
  _([example](https://downloads.dbpedia.org/3.9/en/))_.
- A **subject page** contains triples about a specific subject in a dataset
  _([example](https://dbpedia.org/page/Linked_data))_.
- A **SPARQL result** contains triples that correspond to a [SPARQL CONSTRUCT](https://www.w3.org/TR/sparql11-query/#construct) query
  _([example](https://dbpedia.org/sparql?query=PREFIX+dbpedia-owl%3A+%3Chttp%3A%2F%2Fdbpedia.org%2Fontology%2F%3E%0D%0A%0D%0ACONSTRUCT+%7B+%3Fp+a+dbpedia-owl%3AArtist+%7D%0D%0AWHERE+%7B+%3Fp+a+dbpedia-owl%3AArtist+%7D&format=text%2Fturtle))_.

Linked Data Fragments is a conceptual framework that provides a uniform view on all possible interfaces to RDF,
by observing that each interface partitions a dataset into its own specific kind of _fragments_.
<br>
A [**Linked Data Fragment**](/in-depth/#ldf) (LDF) is characterized
by a specific **selector** _(subject URI, SPARQL query, …)_,
**metadata** _(variable names, counts, …)_,
and **controls** _(links or URIs to other fragments)_.

While the above options are the most common ways to offer datasets,
we could think of many others.
<br>
Our goal is to explore those other ways,
in order to optimize the balance between server and client effort.



## The axis of Linked Data Fragments types
The Linked Data Fragments vision
allows us to visualize different HTTP interfaces for Linked Data _together_.

<svg height="115" class="alternate">
  <marker id="rightArrow" markerWidth="10" markerHeight="10" refx="10" refy="5">
    <polyline points="0,0 10,5 0,10"  fill="none" stroke="black" />
  </marker>
  <marker id="leftArrow" markerWidth="10" markerHeight="10" refx="0" refy="5">
    <polyline points="10,0 0,5 10,10" fill="none" stroke="black" />
  </marker>

  <line x1="0" y1="74" x2="100%" y2="74"
        style="marker-start: url(#leftArrow); marker-end: url(#rightArrow);"/>

  <text x="0.5%" y="25" class="caption left">high client cost</text>
  <text x="0.5%" y="42" class="caption left">high availability</text>
  <text x="0.5%" y="59" class="caption left">high bandwidth</text>

  <text x="99.5%" y="25" class="caption right">high server cost</text>
  <text x="99.5%" y="42" class="caption right">low availability</text>
  <text x="99.5%" y="59" class="caption right">low bandwidth</text>

  <line x1="5%"  x2="5%"  y1="69" y2="80" />
  <line x1="20%" x2="20%" y1="69" y2="80" />
  <line x1="43%" x2="43%" y1="69" y2="80" />
  <line x1="95%" x2="95%" y1="69" y2="80" />
  <text  x="2%"   y="95"  class="label left">data dump</text>
  <text  x="22%"  y="95"  class="label">subject page</text>
  <text  x="43%"  y="95"  class="label"><a xlink:href="#tpf">Triple Pattern Fragment</a></text>
  <text  x="98%"  y="95"  class="label right">SPARQL query result</text>
</svg>

**SPARQL endpoints** are easy for clients,
as they allow highly specific fragment selection.
However, they also have the highest server cost
which makes it expensive to host them with [decent availability](http://sw.deri.org/~aidanh/docs/epmonitorISWC.pdf).
If you don't want to depend on such an endpoint,
you download a **data dump**,
but then you're querying a local source instead of the Web.
With **subject pages**, servers do minimal effort,
but clients need to [work hard](https://squin.sourceforge.net/) to solve simple queries.

Can we **minimize server resource usage**
while still enabling clients to **query data sources efficiently**?
<br>
Such solutions can be found along the above axis
by defining new Linked Data Fragment types.

## New fragment types enable high-availability querying at low cost {#tpf}
We develop fragment types that require minimal server effort
and enable efficient client-side querying.
One such type is called a **Triple Pattern Fragment**
(or **_basic_ Linked Data Fragment**).
It consists of:

- **data** that corresponds to a triple pattern
  _([example](https://data.linkeddatafragments.org/dbpedia?subject=&predicate=rdf%3Atype&object=dbpedia-owl%3ARestaurant))_.
- **metadata** that consists of the (approximate) total triple count
  _([example](https://data.linkeddatafragments.org/dbpedia?subject=&predicate=rdf%3Atype&object=))_.
- **controls** that lead to all other fragments of the same dataset
  _([example](https://data.linkeddatafragments.org/dbpedia?subject=&predicate=&object=%22John%22%40en))_.

Servers that offer such fragments are called
[**_Triple Pattern Fragments_ servers**](/software/#server).
<br>
[**_Triple Pattern Fragments_ clients**](/software/#client)
can solve many SPARQL queries efficiently.
