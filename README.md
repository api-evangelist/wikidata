# Wikidata (wikidata)
Wikidata is a free, collaborative, multilingual knowledge graph hosted by the Wikimedia Foundation. It provides structured linked data for Wikipedia and other Wikimedia projects, as well as a public platform for anyone to read and edit. Wikidata exposes several APIs including a Wikibase REST API for entity read/write operations, the MediaWiki Action API for batch entity retrieval and editing, a SPARQL endpoint for complex graph queries, Linked Data URIs for individual entity access in multiple RDF formats, a real-time Server-Sent Events stream for change monitoring, and full database dumps for bulk data processing.

**URL:** [https://www.wikidata.org/wiki/Wikidata:Data_access](https://www.wikidata.org/wiki/Wikidata:Data_access)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Knowledge Graph, Linked Data, Open Data, Semantic Web, SPARQL, Wikipedia

## Timestamps

- **Created:** 2025-01-01
- **Modified:** 2026-05-03

## APIs

### Wikibase REST API
The Wikibase REST API provides OpenAPI-based read and write operations for Wikidata entities (items and properties), including labels, descriptions, aliases, statements, sitelinks, and patches. Authentication via OAuth2 or MediaWiki session is required for write operations.

**Human URL:** [https://www.wikidata.org/wiki/Wikidata:REST_API](https://www.wikidata.org/wiki/Wikidata:REST_API)

#### Tags:

 - Knowledge Graph, Entities, Items, Properties, Statements, Linked Data

#### Properties

- [Documentation](https://www.wikidata.org/wiki/Wikidata:REST_API)
- [OpenAPI](openapi/wikidata-mediawiki-openapi.yml)
- [JSONSchema](json-schema/wikidata-entity-schema.json)
- [JSON-LD](json-ld/wikidata-context.jsonld)

### MediaWiki Action API
The MediaWiki Action API provides batch entity retrieval, editing, and search for Wikidata via wbgetentities, wbsearchentities, wbeditentity, and other actions. Supports up to 50 entities per request.

**Human URL:** [https://www.mediawiki.org/wiki/Wikibase/API](https://www.mediawiki.org/wiki/Wikibase/API)

#### Tags:

 - MediaWiki, Batch Operations, Entity Retrieval, Search

#### Properties

- [Documentation](https://www.mediawiki.org/wiki/Wikibase/API)
- [SDK - Pywikibot (Python)](https://pypi.org/project/pywikibot/)
- [SDK - wikibase-sdk (JavaScript)](https://www.npmjs.com/package/wikibase-sdk)
- [SDK - Wikidata Toolkit (Java)](https://www.wikidata.org/wiki/Wikidata:Tools/Wikidata_Toolkit)

### SPARQL Query Service
The Wikidata Query Service provides a SPARQL 1.1 endpoint at query.wikidata.org for running complex graph queries over the full Wikidata knowledge base. Supports federated queries, GeoSPARQL, and time-aware queries.

**Human URL:** [https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service)

#### Tags:

 - SPARQL, Graph Query, Linked Data, Open Data

#### Properties

- [Documentation](https://www.mediawiki.org/wiki/Wikidata_Query_Service/User_Manual)
- [APIReference](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service/queries/examples)

### Linked Data Interface
The Wikidata Linked Data Interface provides individual entity data via content negotiation. Supports JSON, JSON-LD, RDF/XML, Turtle, and N-Triples output formats. No authentication required.

**Human URL:** [https://www.wikidata.org/wiki/Wikidata:Data_access#Linked_Data_Interface](https://www.wikidata.org/wiki/Wikidata:Data_access#Linked_Data_Interface)

#### Tags:

 - Linked Data, RDF, JSON-LD, Content Negotiation

#### Properties

- [Documentation](https://www.wikidata.org/wiki/Wikidata:Data_access#Linked_Data_Interface)

### Recent Changes Event Stream
The Wikimedia Event Stream provides real-time Server-Sent Events (SSE) for Wikidata changes. Available at stream.wikimedia.org. Ideal for monitoring Wikidata edits in near-real-time.

**Human URL:** [https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams](https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams)

#### Tags:

 - Event Streaming, Real-time, Server-Sent Events, Change Detection

#### Properties

- [Documentation](https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams)

## Common Properties

- [Website](https://www.wikidata.org/)
- [Portal](https://www.wikidata.org/wiki/Wikidata:Data_access)
- [Documentation](https://www.wikidata.org/wiki/Wikidata:Data_access)
- [GitHubOrganization](https://github.com/wikimedia)
- [GitHubRepository](https://github.com/wikimedia/mediawiki)
- [TermsOfService](https://foundation.wikimedia.org/wiki/Terms_of_Use)
- [PrivacyPolicy](https://foundation.wikimedia.org/wiki/Privacy_policy)
- [Support](https://www.wikidata.org/wiki/Wikidata:Contact_the_development_team)
- [Blog](https://blog.wikimedia.org/)
- [StatusPage](https://www.wikimediastatus.net/)
- [RateLimits](https://www.mediawiki.org/wiki/API:Etiquette)
- [Authentication](https://www.mediawiki.org/wiki/OAuth/For_Developers)

## Features

| Name | Description |
|------|-------------|
| Multilingual Support | All entities support labels, descriptions, and aliases in hundreds of languages via BCP 47 language codes. |
| Structured Statements | Every claim is modeled as a statement with property, value, rank, qualifiers, and references for full provenance. |
| Open License | All Wikidata content is released under CC0 1.0 Universal (Public Domain) — no attribution required. |
| SPARQL Graph Queries | Complex multi-hop queries over 100M+ entities via SPARQL 1.1 at query.wikidata.org with GeoSPARQL and time extensions. |
| Real-Time Event Streaming | Server-Sent Events at stream.wikimedia.org deliver real-time change notifications for Wikidata edits. |
| Multiple Serialization Formats | Entities available as JSON, JSON-LD, RDF/XML, Turtle, and N-Triples via content negotiation on Linked Data URIs. |
| Wikibase Federation | Wikidata is an instance of Wikibase; federated SPARQL queries can cross Wikibase instances including Wikimedia Commons. |
| Database Dumps | Full JSON and RDF/TTL database dumps refreshed weekly at dumps.wikimedia.org for local bulk processing. |

## Use Cases

| Name | Description |
|------|-------------|
| Knowledge Graph Augmentation | Enrich private datasets with structured Wikidata facts — entities, dates, relationships — via item and SPARQL queries. |
| Fact-Checking and Verification | Retrieve canonical statements with references to verify biographical, geographic, or scientific claims in text. |
| Wikipedia Infobox Data | Power Wikipedia infoboxes and sister-project templates with live Wikidata entity data via the MediaWiki Action API. |
| NLP Entity Linking | Resolve named entities from natural language to Wikidata Q-IDs using wbsearchentities and SPARQL label lookups. |
| Semantic Search | Build ontology-aware search systems using Wikidata's P31 (instance of) and P279 (subclass of) property hierarchies. |
| Change Monitoring | Track real-time edits to Wikidata entities relevant to a domain using the SSE event stream. |
| Linked Open Data Publishing | Publish organizational data as Linked Open Data by aligning custom schemas to Wikidata properties and Q-IDs. |

## Integrations

| Name | Description |
|------|-------------|
| Wikipedia | Wikidata powers structured data for all Wikipedia language editions via Lua modules and infobox templates. |
| Wikimedia Commons | Media files on Wikimedia Commons are described using Wikidata items via structured data on Commons. |
| OpenStreetMap | OSM features are linked to Wikidata via the wikidata=* tag, enabling geographic entity cross-referencing. |
| Scholia | Scholia is a Wikidata-based scholarly profile service that visualizes publications, authors, and institutions. |
| Reasonator | Reasonator renders human-readable pages for Wikidata items, integrating maps, timelines, and media. |
| Mix'n'match | Mix'n'match links Wikidata items to external databases (VIAF, ORCID, GND, etc.) for authority control. |
| OpenRefine | OpenRefine has a Wikidata reconciliation service and can batch-upload tabular data as Wikidata statements. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Wikidata REST API & MediaWiki API](openapi/wikidata-mediawiki-openapi.yml)

### JSON Schema

- [Wikidata Entity Schema](json-schema/wikidata-entity-schema.json)
- [Wikidata Item Schema](json-schema/wikidata-item-schema.json)
- [Wikidata Property Schema](json-schema/wikidata-property-schema.json)
- [Wikidata Statement Schema](json-schema/wikidata-statement-schema.json)
- [Wikidata Statement Create Schema](json-schema/wikidata-statement--create-schema.json)
- [Wikidata Data Value Schema](json-schema/wikidata-data--value-schema.json)
- [Wikidata Sitelink Schema](json-schema/wikidata-sitelink-schema.json)
- [Wikidata Patch Request Schema](json-schema/wikidata-patch--request-schema.json)
- [Wikidata Item Create Schema](json-schema/wikidata-item--create-schema.json)

### JSON Structure

- [Wikidata Item Structure](json-structure/wikidata-item-structure.json)
- [Wikidata Property Structure](json-structure/wikidata-property-structure.json)
- [Wikidata Statement Structure](json-structure/wikidata-statement-structure.json)
- [Wikidata Data Value Structure](json-structure/wikidata-data--value-structure.json)
- [Wikidata Sitelink Structure](json-structure/wikidata-sitelink-structure.json)

### JSON-LD

- [Wikidata Context](json-ld/wikidata-context.jsonld)

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [Wikibase REST API](capabilities/shared/wikibase-rest-api.yaml) — 10 operations for entity read/write access

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Knowledge Graph Access](capabilities/knowledge-graph-access.yaml) | Wikibase REST API | 7 | Data Engineer, Knowledge Graph Analyst, AI/ML Pipeline |

## Vocabulary

- [Wikidata Vocabulary](vocabulary/wikidata-vocabulary.yaml) — Unified taxonomy mapping 6 resources, 7 actions, 1 workflow, and 3 personas across operational (OpenAPI) and capability (Naftiko) dimensions

## Rules

- [Wikidata Spectral Rules](rules/wikidata-spectral-rules.yml) — 30 rules across 10 categories enforcing Wikidata API conventions

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
