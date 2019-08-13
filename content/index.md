---
order: 0
title: Home
header: false
menu: false
---

<div id="billboard" markdown="1">
# Linked Data Fragments

[![[Linked Data Fragments logo]](/images/logo.svg){:.logo}
Query the Web of data on _Web-scale_ by
<br>
moving intelligence from servers to clients.](/concept/)
{:.slogan}
[Watch this talk](http://videolectures.net/iswc2014_verborgh_querying_datasets/ "Ruben Verborgh at ISWC2014: Querying Datasets on the Web with High Availability")
to learn the foundations of Linked Data Fragments.

Try [Comunica](https://comunica.linkeddatafragments.org/), a new Web framework to query Linked Data Fragments.
</div>

**A huge amount of Linked Data is available on the Web.**
But can live applications use it?
<br>
**SPARQL endpoints** are expensive for the server, and not always available for all datasets.
<br>
**Downloadable dumps** are expensive for clients, and do not allow live querying on the Web.

With **Linked Data Fragments**, and specifically the **Triple Pattern Fragments** interface,
we aim to explore what happens when we redistribute the load between clients and servers.
We then measure the impact of such interfaces on clients, servers, and caches.

<svg height="100">
  <marker id="rightArrow" markerWidth="10" markerHeight="10" refx="10" refy="5">
    <polyline points="0,0 10,5 0,10"  fill="none" stroke="black" />
  </marker>
  <marker id="leftArrow" markerWidth="10" markerHeight="10" refx="0" refy="5">
    <polyline points="10,0 0,5 10,10" fill="none" stroke="black" />
  </marker>

  <line x1="0" y1="74" x2="100%" y2="74"
        style="marker-start: url(#leftArrow); marker-end: url(#rightArrow);"/>

  <text x="0.5%" y="13" class="caption left">high client cost</text>
  <text x="0.5%" y="36" class="caption left">high availability</text>
  <text x="0.5%" y="59" class="caption left">high bandwidth</text>

  <text x="99.5%" y="13" class="caption right">high server cost</text>
  <text x="99.5%" y="36" class="caption right">low availability</text>
  <text x="99.5%" y="59" class="caption right">low bandwidth</text>

  <text x="50%" y="13" class="accent">Have we explored</text>
  <text x="50%" y="36" class="accent">all options in-between?</text>

  <line x1="5%"  x2="5%"  y1="69" y2="80" />
  <line x1="30%" x2="30%" y1="69" y2="80" class="accent" />
  <line x1="43%" x2="43%" y1="69" y2="80" class="accent" />
  <line x1="51%" x2="51%" y1="69" y2="80" class="accent" />
  <line x1="63%" x2="63%" y1="69" y2="80" class="accent" />
  <line x1="73%" x2="73%" y1="69" y2="80" class="accent" />
  <line x1="95%" x2="95%" y1="69" y2="80" />
  <text  x="2%"   y="95"  class="label left">data dump</text>
  <text  x="98%"  y="95"  class="label right">SPARQL endpoint</text>
</svg>

Such solutions allow you to reliably [execute queries against live Linked Data on the Web](http://client.linkeddatafragments.org/).
<br>
You can even perform [federated querying](http://bit.ly/swedish-nobel-harvard)—all in your browser.

These are just a few examples of what the Semantic Web can become
if we build intelligent _clients_ instead of intelligent _servers_.
[Learn more](/concept/).

You can start publishing such lightweight Linked Data right now:
[install the server](/software/).
<br>
Or view some of the 650,000+ datasets out there:
[browse datasets online](/data/).
<br>
See how clients solve SPARQL queries on your data:
[try a Linked Data Fragments client](https://comunica.linkeddatafragments.org/).
