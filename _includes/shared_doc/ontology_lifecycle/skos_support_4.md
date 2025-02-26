### Metrics data for SKOS vocabularies

EcoPortal employs the [OWL API](https://owlcs.github.io/owlapi/) to parse all ontology and vocabulary submissions, including the computation of metric data. The OWL API interprets SKOS vocabularies as RDF files that encompass classes and instances. Following the SKOS Reference, concepts are identified as instances of owl:Class, consequently, they are counted as instances, also referred to as "individuals".
When examining [metric tables]({{ site.baseurl }}{% link docs/users-guide-docs/documentation/ecoportal/platform_overview/ontology_details.md %}) within the EcoPortal user interface, the "Number Of Individuals" value aligns with the count of concepts within a given SKOS vocabulary.
