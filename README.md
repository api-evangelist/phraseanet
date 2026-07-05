# Phraseanet (phraseanet)

Phraseanet is an open-source (GPL-v3) Digital Asset Management (DAM) platform built in PHP and developed by [Alchemy](https://www.phraseanet.com/). It centralizes photos, videos, documents, and other media with metadata management (Dublin Core mapping), Elasticsearch-powered search, multi-resolution sub-definitions, thesaurus, rights administration, stories, baskets, and feeds. Phraseanet exposes a documented RESTful API (v1 and v2, with a newer v3 published on SwaggerHub) secured with **OAuth2**, covering records, databoxes and collections, metadata, search, stories, baskets, and feeds.

**Access model:** Phraseanet is **self-hosted**. There is no single public shared API endpoint - the API runs on each organization's own Phraseanet instance, and the v1 documentation states plainly that there is no public shared Phraseanet API. The core software and its API are free under GPL-v3; Alchemy sells commercial hosting, setup, training, support, and custom development around the open-source core. Replace `https://your-phraseanet-instance` below with your own installation's host.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/phraseanet/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/phraseanet/refs/heads/main/apis.yml)

## Authentication

Phraseanet uses **OAuth2**. Register an application in Phraseanet to obtain a Client ID and Client Secret, then use the authorization endpoint (`/api/oauthv2/authorize`) and token endpoint (`/api/oauthv2/token`). The access token is sent either in an `Authorization` header or as an `oauth_token` query parameter. All requests must use HTTPS. Responses are wrapped in an object with `meta` and `response` fields, JSON by default.

## Tags

- Digital Asset Management
- DAM
- Media
- Metadata
- Open Source
- Search

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### Phraseanet Records API

Add, retrieve, and manage individual media records (assets) within a databox - get a record, add a record, fetch its caption, embedded sub-definitions and related records, set its collection, and delete it.

- **Human URL:** [https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Records/Record.html](https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Records/Record.html)
- **Base URL:** `https://your-phraseanet-instance/api/v1`

### Phraseanet Databoxes and Collections API

List the databoxes (data repositories) available to the authenticated application and enumerate the collections within each databox, including base_id, collection_id, name, and record counts, plus databox status structure and terms of use.

- **Human URL:** [https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Databox/Collections.html](https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Databox/Collections.html)
- **Base URL:** `https://your-phraseanet-instance/api/v1`

### Phraseanet Metadata API

Read and write descriptive metadata on records - fetch record metadatas and captions, set metadata values against the databox metadata structure, and update record status flags.

- **Human URL:** [https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Records/Metadatas.html](https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Records/Metadatas.html)
- **Base URL:** `https://your-phraseanet-instance/api/v1`

### Phraseanet Search API

Elasticsearch-backed search across records and stories. Submit a query with filters (databox ids, collections, status, record type, date, offset, and per-page limits) and receive matching records with facets and paging metadata.

- **Human URL:** [https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Search.html](https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Search.html)
- **Base URL:** `https://your-phraseanet-instance/api/v1`

### Phraseanet Stories API

Manage stories - records that group other records. Create a story, fetch it and its embedded sub-definitions, add and remove child records, and set the story cover image.

- **Human URL:** [https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Stories/Story.html](https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Stories/Story.html)
- **Base URL:** `https://your-phraseanet-instance/api/v1`

### Phraseanet Baskets API

Create and manage baskets - user-curated working sets of records. List baskets, create a basket, read its content, rename it, change its description, and delete it.

- **Human URL:** [https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Baskets/List.html](https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Baskets/List.html)
- **Base URL:** `https://your-phraseanet-instance/api/v1`

### Phraseanet Feeds API

Read published feeds - list the feeds the authenticated user can see, read the entries of a single feed, and read an aggregated view across all feeds, each entry carrying its records and publication metadata.

- **Human URL:** [https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Feeds/List.html](https://docs.phraseanet.com/4.1/en/Devel/API/V1/Route/Feeds/List.html)
- **Base URL:** `https://your-phraseanet-instance/api/v1`

### Phraseanet Account API

Retrieve the authenticated user (the "me" resource) including profile details, collection access rights, field access, and sub-definition access. Backed by the OAuth2 authorization and token endpoints under `/api/oauthv2/`.

- **Human URL:** [https://docs.phraseanet.com/4.1/en/Devel/API/V1/Authentication.html](https://docs.phraseanet.com/4.1/en/Devel/API/V1/Authentication.html)
- **Base URL:** `https://your-phraseanet-instance/api/v1`

## Common Properties

- [GitHub Organization](https://github.com/alchemy-fr)
- [LinkedIn](https://www.linkedin.com/products/alchemy-sarl-phraseanet/)
- [Website](https://www.phraseanet.com/)
- [Documentation](https://docs.phraseanet.com/)
- [Source Code](https://github.com/alchemy-fr/Phraseanet)
- [Plans](plans/phraseanet-plans-pricing.yml)
- [Rate Limits](rate-limits/phraseanet-rate-limits.yml)
- [Fin Ops](finops/phraseanet-finops.yml)

## Artifacts

- [OpenAPI](openapi/phraseanet-openapi.yml)
- [Postman Collection](collections/phraseanet.postman_collection.json)
- [Open Collection](collections/phraseanet.opencollection.json)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
