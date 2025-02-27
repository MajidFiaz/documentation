---
title: REST API Documentation
summary: API Documentation
layout: default
parent: Developer guide @EcoPortal
grand_parent: Users guide
permalink: user_guide/developer_guide/rest_api_documentation/EcoPortal
nav_order: 2
---


## REST API Documentation

This API consists of a set of resources (Ontologies, Classes, etc) and related endpoints (Search, Annotator, Recommender) that are connected together via links, much like webpages. The developer recommends trying to browse the API using a web browser before starting writing code.
For more information, please contact us at semantics@lifewatch.eu.

###	Common Parameters



###	Resource Endpoints

The EcoPortal API endpoints include a dictionary named "links" containing URLs of the available media types within the API along with hypermedia links connecting them. These media types describe the various types of resources available, specifying the HTTP verbs (POST, GET, PUT, DELETE, and PATCH) that can be used with them and outlining the attributes contained within each resource.

#### Available Media Types:

__agents__: https://data.ecoportal.lifewatch.eu/Agents

__categories__: https://data.ecoportal.lifewatch.eu/categories

__groups__: https://data.ecoportal.lifewatch.eu/groups

__Class__: https://data.ecoportal.lifewatch.eu/ontologies/PCO/classes

__documentation__: https://data.ecoportal.lifewatch.eu/documentation

__identifier_requests__: https://data.ecoportal.lifewatch.eu/identifier_requests

__mappings__: https://data.ecoportal.lifewatch.eu/mappings

__metrics__: https://data.ecoportal.lifewatch.eu/metrics

__notes__: https://data.ecoportal.lifewatch.eu/notes

__ontologies__: https://data.ecoportal.lifewatch.eu/ontologies

__ontologies_full__: https://data.ecoportal.lifewatch.eu/ontologies_full

__analytics__: https://data.ecoportal.lifewatch.eu/analytics

__submissions__: https://data.ecoportal.lifewatch.eu/submissions

__projects__: https://data.ecoportal.lifewatch.eu/projects

__provisional_classes__: https://data.ecoportal.lifewatch.eu/provisional_classes

__provisional_relations__: https://data.ecoportal.lifewatch.eu/provisional_relations

__replies__: https://data.ecoportal.lifewatch.eu/replies

__reviews__: https://data.ecoportal.lifewatch.eu/reviews

__slices__: https://data.ecoportal.lifewatch.eu/slices

__submission_metadata__: https://data.ecoportal.lifewatch.eu/submission_metadata

__ontology_metadata__: https://data.ecoportal.lifewatch.eu/ontology_metadata

__users__: https://data.ecoportal.lifewatch.eu/users

#### Agents

Example: https://data.ecoportal.lifewatch.eu/Agents

#### HTTP Methods for Resource

| HTTP Verb | Path             |
|:----------|:-----------------|
| GET       | /agents          | 
| GET       | /agents/:id      | 
| GET       | /Agents          | 
| GET       | /Agents/:id      | 
| PUT       | /agents/:acronym | 
| PUT       | /Agents/:acronym | 
| POST      | /agents          | 
| POST      | /Agents          | 
| PATCH     | /agents/:id      | 
| PATCH     | /Agents/:id      | 
| DELETE    | /agents/:id      | 
| DELETE    | /Agents/:id      | 

#### Resource Description

| Attribute     | Default | Unique | Required | List | Type                                                |
|:--------------|:--------|:-------|:---------|:-----|:----------------------------------------------------|
| agentType     | true    |        | true     |      |                                                     |
| name          | true    |        | true     |      |                                                     |
| homepage      | true    |        |          |      |                                                     |
| acronym       | true    |        |          |      |                                                     |
| email         | true    | true   |          |      |                                                     |
| identifiers   | true    |        |          | true | http://www.w3.org/ns/adms#Identifier                |
| affiliations  | true    |        |          | true | http://xmlns.com/foaf/0.1/Agent                     |
| creator       | true    |        | true     |      | https://data.ecoportal.lifewatch.eu/metadata/users  |

#### Categories

Example: https://data.ecoportal.lifewatch.eu/categories

Example: https://data.ecoportal.lifewatch.eu/categories/Ecology

Example: https://data.ecoportal.lifewatch.eu/ontologies/PCO/categories

#### HTTP Methods for Resource

| HTTP Verb | Path                            |
|:----------|:--------------------------------|
| GET       | /ontologies/:acronym/categories | 
| GET       | /categories                     | 
| GET       | /categories/:acronym            | 
| PUT       | /categories/:acronym            | 
| POST      | /categories                     | 
| PATCH     | /categories/:acronym            | 
| DELETE    | /categories/:acronym            | 



#### Resource Description

| Attribute      | Default | Unique | Required | List | Type                                                    |
|:---------------|:--------|:-------|:---------|:-----|:--------------------------------------------------------|
| acronym        | true    | true   | true     |      |                                                         |
| name           | true    |        | true     |      |                                                         |
| description    | true    |        |          |      |                                                         |
| created        | true    |        |          |      |                                                         |
| parentCategory | true    |        |          |      | https://data.ecoportal.lifewatch.eu/metadata/Categories |
| ontologies     | true    |        |          |      | https://data.ecoportal.lifewatch.eu/metadata/ontology   |

#### Class 

Example: https://data.ecoportal.lifewatch.eu/ontologies/PCO/classes

Example: https://data.ecoportal.lifewatch.eu/ontologies/PCO/classes/roots

Example: https://data.ecoportal.lifewatch.eu/ontologies/PCO/classes/http%3A%2F%2Fpurl.obolibrary.org%2Fobo%2FNCBITaxon_2759

Example: https://data.ecoportal.lifewatch.eu/ontologies/PCO/classes/http%3A%2F%2Fpurl.obolibrary.org%2Fobo%2FNCBITaxon_2759/children


#### HTTP Methods for Resource

| HTTP Verb | Path                                             |
|:----------|:-------------------------------------------------|
| GET       | /ontologies/:ontology/classes                    | 
| GET       | /ontologies/:ontology/classes/roots_paged        | 
| GET       | /ontologies/:ontology/classes/roots              | 
| GET       | /ontologies/:ontology/classes/:cls               | 
| GET       | /ontologies/:ontology/classes/:cls/paths_to_root | 
| GET       | /ontologies/:ontology/classes/:cls/tree          | 
| GET       | /ontologies/:ontology/classes/:cls/ancestors     | 
| GET       | /ontologies/:ontology/classes/:cls/descendants   | 
| GET       | /ontologies/:ontology/classes/:cls/children      | 
| GET       | /ontologies/:ontology/classes/:cls/parents       | 




