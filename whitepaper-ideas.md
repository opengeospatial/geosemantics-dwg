# Ideas for a White Paper 

At the most recent GeoSematics DWG, September 2019 in Banff, there was a discussion about newly submitted change requests for GeoSPARQL. In order to create momentum and interest for a GeoSPARQL 2.0 working group with active members, some more marketing is needed. The proposal at the DWG was to do this in the form of a White Paper. 

The White Paper should show that there is indeed practical value in graph representations of some spatial data using Linked Data with strong(er) semantics. 

## How to contribute
Users and implementers are very much invited to collaborate on this White Paper! First, let's gather some ideas on what to put into the paper. Add some content either to this page (i.e ideas for topics, questions, text snippets you already have laying around), or to a new page in this repository. Or start a discussion by creating an [issue](https://github.com/opengeospatial/geosemantics-dwg/issues). We will setup the structure of the White Paper and start filling it properly as a later step. 

## Topics
(examples)
- Business reasons for Linked Data / knowledge graphs.
- Identified user communities of Linked geo Data.
- Real world examples / success stories of Linked geo Data.
- Geospatial support in triplestores, including treatments of levels of GeoSPARQL support, and things GeoSPARQL is lacking.
- Existing implementations of geospatial extensions exceeding GeoSPARQL capabilities.
- Overview and discussion of GeoSPARQL change requests.
- Further modularization of GeoSPARQL.
- The need for a cross-domain model for spatial data and the options for GeoSPARQL becoming that model, or contributing to it.
- The need for making GeoSPARQL more web-friendly.

## Questions to treat in the white paper
(examples)

- Could some form of GeoSPARQL become as widely adopted as SF-SQL or really become a key element of the Linked Data Web?
- Would coordination with GraphQL be a good idea?
- Should GeoSPARQL move towards an ontology of space positions, regions, and relations, rather than being rooted in the General Feature Model?
- Could GeoSPARQL offer basic datatypes necessary for storing and processing general spatial data, regardless of the Semweb/RDF?
- How great is the need for cross-domain interoperability (e.g. using bits of (geo)spatial data in information systems that do not emphasise spatial information)?
- Is it possible to develop or endorse a web model for Coordinate Reference Systems to go with GeoSPARQL?
- Is it possible to define common ground for vector and coverage data within GeoSPARQL?
- Is there a need to seek collaboration with non-OGC parties for further development of GeoSPARQL?

## Why OGC should update GeoSPARQL
(example text snippet; source: Frans Knibbe)

Linked Data and, by extension, GeoSPARQL is not widely used by OGC members (or the geospatial domain).

Indeed the more one is involved with geospatial data only, the less need there is to use GeoSPARQL. I have worked with people from the geospatial domain and people that primarily work with Linked Data or the semantic web. Of the first group, few people had even heard of GeoSPARQL. But I would like to argue that if the OGC chooses to improve GeoSPARQL, it should be done just because parties on the fringes of the geospatial domain depend on it, and do use it. At the moment, GeoSPARQL is the only more or less stable and standardised way of using geographical data on the web. So people use it, whether it is good or not. I think the OGC has an obligation towards the many people that do work with geospatial data, but have a core business outside of that domain. 

For example, developers of data storage systems (SQL databases, triple stores, ….) need GeoSPARQL for data types and functions. API developers need to mimic standard functionality  Web developers need to make data insightful to uses. Data publishers need to make difficult modelling decisions. Data modellers outside of the geospatial domain may have to deal with bits of geospatial information in their models. I would like to speak out for these (and other) groups of people who may not have had sufficient voice in making the decision to update GeoSPARQL or not.

## Linked Data and the geospatial community
One of the strengths of using Linked Data is the fact that it can help to eleviate heterogeneity issues. Heterogeneous geospatial data can be converted to RDF (using a Semantic Uplift process) and subsequently, the results of a geospatial query can be downlifted to the respective heterogeneous data formats. Moreover, Linked Data can be used to access a variety of data from other knowledge domains which can be useful in particular to enrich gesopatial data extracted from e.g. OGC webservices. These data do not have to be stored locally, no schema has to be developed to import them into the own database and they are often free and easily accessible. Since the definition of GeoSPARQL, the geospatial semantic web has grown by a large extent, especially after the emergence of the LinkedGeoData ontology, allowing OpenStreetMap to be exposed as Linked Data. Since then, more and more Linked Data repositories such as DBPedia and Wikidata have been adding support for geospatial data. (Huxhold 1991) states, that 80% of all information is directly or indirectly related to a geospatial aspect, so a proper support for geospatial functions in the semantic web seems to be of interest by looking at the available datasources alone.
However, the geospatial community has not adopted Linked Data to a large extent. 

I can see the following reasons for that:

* A lack of software support: Neither QGIS, ArcGIS or any other major software package includes options to access a triple store
* A lack of awareness of Linked Data and its benefits
* A lack of proper geospatial query capabilities: GeoSPARQL only allows to relate geometries to each other but does not allow
geometry modifications, raster data processing and algebra and further tasks which are common in state of the art SQL databases
* A lack of connectivity to other OGC webservices: Why not allow OGC webservices with a Linked Data backend?

Taking into account this aspect I would argue that providing these query capabilities and developing plugins for major platforms such as QGIS would enable the geospatial community to use linked data in a proper way. Unless the geospatial community can use Linked Data in a way they use traditional geospatial webservices, Linked Data will remain unattractive. However, by defining a new GeoSPARQL standard, these prerequisites can be fulfilled and can lead to implementations such as plugins, triple store backends to OGC webservices and therefore to a greater interest in the geospatial community.
