# Wikidata (wikidata)

Wikidata is a free, collaborative, multilingual knowledge graph hosted by the Wikimedia Foundation. It provides structured linked data for Wikipedia and other Wikimedia projects, as well as a public platform for anyone to read and edit. Wikidata exposes several APIs including a Wikibase REST API for entity read/write operations, the MediaWiki Action API for batch entity retrieval and editing, a SPARQL endpoint for complex graph queries, Linked Data URIs for individual entity access in multiple RDF formats, a real-time Server-Sent Events stream for change monitoring, and full database dumps for bulk data processing.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Knowledge Graph
- Linked Data
- Open Data
- Semantic Web
- SPARQL
- Wikipedia

## Timestamps

- **Created:** 2025-01-01
- **Modified:** 2026-05-19

## APIs

### Wikibase REST API

The Wikibase REST API provides OpenAPI-based read and write operations for Wikidata entities (items and properties), including labels, descriptions, aliases, statements, sitelinks, and patches. Authentication via OAuth2 or MediaWiki session is required for write operations.

- **Human URL:** [https://www.wikidata.org/wiki/Wikidata:REST_API](https://www.wikidata.org/wiki/Wikidata:REST_API)
- **Base URL:** `https://www.wikidata.org/w/rest.php/wikibase/v0`

#### Tags

- Knowledge Graph
- Entities
- Items
- Properties
- Statements
- Linked Data

#### Properties

- [Documentation](https://www.wikidata.org/wiki/Wikidata:REST_API)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/openapi/wikidata-mediawiki-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/json-schema/wikidata-entity-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/json-ld/wikidata-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Postman Collection](collections/wikidata-mediawiki.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wikidata-mediawiki.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### MediaWiki Action API

The MediaWiki Action API provides batch entity retrieval, editing, and search for Wikidata via wbgetentities, wbsearchentities, wbeditentity, and other actions. Supports up to 50 entities per request. Accessible at wikidata.org/w/api.php.

- **Human URL:** [https://www.mediawiki.org/wiki/Wikibase/API](https://www.mediawiki.org/wiki/Wikibase/API)
- **Base URL:** `https://www.wikidata.org/w/api.php`

#### Tags

- MediaWiki
- Batch Operations
- Entity Retrieval
- Search

#### Properties

- [Documentation](https://www.mediawiki.org/wiki/Wikibase/API)
- [SDK](https://pypi.org/project/pywikibot/)
- [SDK](https://www.npmjs.com/package/wikibase-sdk)
- [SDK](https://www.wikidata.org/wiki/Wikidata:Tools/Wikidata_Toolkit)
- [Postman Collection](collections/wikidata-mediawiki.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wikidata-mediawiki.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SPARQL Query Service

The Wikidata Query Service provides a SPARQL 1.1 endpoint at query.wikidata.org for running complex graph queries over the full Wikidata knowledge base. Supports federated queries, GeoSPARQL, and time-aware queries. Data is CC0 licensed.

- **Human URL:** [https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service)
- **Base URL:** `https://query.wikidata.org/sparql`

#### Tags

- SPARQL
- Graph Query
- Linked Data
- Open Data

#### Properties

- [Documentation](https://www.mediawiki.org/wiki/Wikidata_Query_Service/User_Manual)
- [API Reference](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service/queries/examples)
- [Postman Collection](collections/wikidata-mediawiki.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wikidata-mediawiki.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Linked Data Interface

The Wikidata Linked Data Interface provides individual entity data via content negotiation at http://www.wikidata.org/entity/{QID}. Supports JSON, JSON-LD, RDF/XML, Turtle, and N-Triples output formats. No authentication required.

- **Human URL:** [https://www.wikidata.org/wiki/Wikidata:Data_access#Linked_Data_Interface](https://www.wikidata.org/wiki/Wikidata:Data_access#Linked_Data_Interface)
- **Base URL:** `https://www.wikidata.org/entity`

#### Tags

- Linked Data
- RDF
- JSON-LD
- Content Negotiation

#### Properties

- [Documentation](https://www.wikidata.org/wiki/Wikidata:Data_access#Linked_Data_Interface)
- [Postman Collection](collections/wikidata-mediawiki.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wikidata-mediawiki.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Recent Changes Event Stream

The Wikimedia Event Stream provides real-time Server-Sent Events (SSE) for Wikidata changes, revision creations, and page events. Available at stream.wikimedia.org. Ideal for monitoring Wikidata edits in near-real-time.

- **Human URL:** [https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams](https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams)
- **Base URL:** `https://stream.wikimedia.org/v2/stream`

#### Tags

- Event Streaming
- Real-time
- Server-Sent Events
- Change Detection

#### Properties

- [Documentation](https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams)
- [Postman Collection](collections/wikidata-mediawiki.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wikidata-mediawiki.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/wikidata-wf)
- [Website](https://www.wikidata.org/)
- [Portal](https://www.wikidata.org/wiki/Wikidata:Data_access)
- [Documentation](https://www.wikidata.org/wiki/Wikidata:Data_access)
- [GitHub Organization](https://github.com/wikimedia)
- [GitHub Repository](https://github.com/wikimedia/mediawiki)
- [Terms of Service](https://foundation.wikimedia.org/wiki/Terms_of_Use)
- [Privacy Policy](https://foundation.wikimedia.org/wiki/Privacy_policy)
- [Support](https://www.wikidata.org/wiki/Wikidata:Contact_the_development_team)
- [Blog](https://blog.wikimedia.org/)
- [Status Page](https://www.wikimediastatus.net/)
- [Rate Limits](https://www.mediawiki.org/wiki/API:Etiquette)
- [Authentication](https://www.mediawiki.org/wiki/OAuth/For_Developers)
- [Spectral Rules](https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/rules/wikidata-spectral-rules.yml)
- [Vocabulary](https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/vocabulary/wikidata-vocabulary.yaml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
