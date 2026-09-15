# TMDB API — OpenAPI Documentation Project

A portfolio project demonstrating the process of turning a real-world API into a structured, developer-friendly OpenAPI reference.

This project uses **The Movie Database (TMDB) API** to show practical API documentation, API testing, OpenAPI refinement, schema modeling, authentication documentation, and documentation quality assurance.

The project began with API exploration and endpoint testing in **Postman**, then moved to generating an OpenAPI specification from the collection and progressively reviewed and refined the generated YAML in **VS Code**.

The goal was not simply to produce a valid OpenAPI file. The focus was on improving the **accuracy, consistency, maintainability, and developer experience** of the resulting API reference.

## Project overview

The project covers **52 API operations across 51 paths**, organized into the following areas:

* Authentication
* Account
* Certification
* Search
* Discover
* Movies
* Network

The final OpenAPI specification models the API's requests, parameters, authentication requirements, responses, reusable schemas, and examples in a format suitable for OpenAPI-compatible documentation tooling.

## Documentation workflow

The project followed a practical API documentation workflow:

```text
TMDB API
   ↓
Endpoint exploration and testing in Postman
   ↓
Saved response examples and endpoint documentation
   ↓
OpenAPI specification generated from the collection
   ↓
Specification reviewed and refined in VS Code
   ↓
Schema, request, response, authentication, and documentation QA
   ↓
OpenAPI specification prepared for Mintlify
```

This workflow reflects a documentation-as-code approach in which API documentation is treated as a maintained technical artifact rather than static prose.

## What I worked on

### API exploration and testing

I worked with the TMDB API in Postman to:

* Explore API endpoints and request requirements
* Test HTTP methods and endpoint behavior
* Work with query, path, and body parameters
* Test authentication flows
* Investigate successful and error responses
* Save representative response examples
* Organize the API into logical endpoint groups
* Document the API

The collection contains **52 documented operations** spanning authentication, accounts, certifications, search, discovery, movies, and network-related functionality.

### OpenAPI structure

The generated OpenAPI specification was reviewed and refined to improve its machine readability and documentation quality.

This included:

* Standardizing operation IDs
* Reviewing HTTP methods
* Correcting malformed paths
* Verifying path parameter definitions
* Correcting parameter types and required status
* Structuring request bodies
* Defining response objects
* Adding reusable component schemas
* Reviewing internal `$ref` relationships
* Maintaining OpenAPI 3.0 compatibility
* Removing inappropriate Postman-generated artifacts

### Request and response modeling

The specification contains structured definitions for API requests and responses, including reusable schemas for areas such as:

* Movies
* TV shows
* People
* Accounts
* Search results
* Discover results
* Authentication
* Networks
* Collections
* Keywords
* Reviews
* Recommendations
* Videos
* Watch providers
* Pagination
* API errors

Where structures are shared across endpoints, reusable component schemas are used instead of unnecessarily duplicating definitions.

### Authentication and security

Authentication was reviewed as both a technical and documentation concern.

The specification represents:

* Bearer authentication
* API-key authentication
* TMDB session handling
* Guest sessions
* Request-token workflows
* v4 access-token authentication
* Authenticated account operations
* Rating authentication
* Authentication-related error responses

Credential-like values were removed from the specification and replaced with safe placeholders where appropriate.

Particular attention was given to distinguishing application authentication from user-authenticated workflows where the API requires different credentials or tokens.

### Documentation quality

The generated specification was reviewed and refined to produce a clear, consistent, and developer-friendly API reference.

The review focused on:

* Applying consistent TMDB terminology across endpoints
* Correcting terminology, grammar, and typographical errors
* Standardizing operation summaries and endpoint descriptions
* Correcting malformed URLs and paths
* Verifying request and response structures
* Reviewing parameter names, types, and required status
* Defining required request-body fields
* Improving response descriptions and error documentation
* Removing irrelevant or inappropriate captured response artifacts
* Aligning authentication requirements with the documented requests
* Improving consistency across related endpoints and API workflows

The resulting specification is designed to be both machine-readable and useful to developers working with the API.

## Documentation approach

When I generated the OpenAPI specification, I focus on converting this into a reliable, maintainable API reference that developers could use with confidence.

The review include:

* **Accuracy** — ensuring endpoints, parameters, request bodies, responses, and authentication requirements reflect the API behavior
* **Consistency** — applying consistent terminology, structure, naming, and descriptions across the specification
* **Clarity** — making endpoint summaries and supporting descriptions easier for developers to understand
* **Machine readability** — maintaining valid OpenAPI structure and reusable schemas
* **Security** — removing credential-like values and ensuring authentication requirements are represented appropriately
* **Maintainability** — using reusable components and consistent structures that can be updated as the API evolves
* **Developer experience** — providing the information developers need to understand, test, and integrate with the API


## Validation and quality assurance

The final specification was reviewed for both structural correctness and documentation quality.

Key checks included:

| Area                                       |  Result |
| ------------------------------------------ | ------: |
| OpenAPI version                            |   3.0.0 |
| API paths                                  |      51 |
| Operations                                 |      52 |
| Unique operation IDs                       | 52 / 52 |
| Broken local `$ref`s                       |       0 |
| Empty response definitions                 |       0 |
| Missing path parameters                    |       0 |
| Invalid nullable syntax                    |       0 |
| Malformed account paths                    |       0 |
| `softcore` field references                |       0 |
| Broken documentation URL                   |       0 |
| Incorrect account `session_id` requirement |       0 |
| Request bodies missing required fields     |       0 |

The specification was also reviewed for consistency between its machine-readable definitions and the accompanying endpoint documentation.

## Tools and technologies

* **OpenAPI 3.0**
* **YAML**
* **REST APIs**
* **JSON**
* **Git**
* **GitHub**
* **Postman**
* **VS Code**
* **Mintlify**
* OpenAPI schema validation
* Reusable component schemas
* API authentication and security schemes

## Repository structure

```text
tmdb-api-developer-guide/
│
├── openapi/
│   └── tmdb-openapi.yaml
│
├── postman/
│   └── tmdb-api-collection.json
│
├── assets/
│   └── images/
│
├── README.md
└── .gitignore
```

### Main deliverables

**OpenAPI specification**

```text
openapi/tmdb-openapi.yaml
```

The OpenAPI specification is the primary technical artifact and represents the refined API reference.

**Postman collection**

```text
postman/tmdb-api-collection.json
```

The collection provides the API testing and exploration context used during the documentation workflow.

**Assets**

```text
assets/images/
```

Images used to illustrate the documentation can be stored locally in the repository rather than relying on externally hosted assets.

## What this project demonstrates

This project demonstrates practical experience with:

* API reference documentation
* OpenAPI specifications
* REST API concepts
* HTTP methods and status codes
* Request and response modeling
* Authentication documentation
* Security schemes
* API testing
* Postman
* JSON
* YAML
* Reusable schemas
* Error response modeling
* Documentation QA
* Developer experience
* Documentation consistency
* Documentation-as-code workflows
* API documentation tooling

## Why I built this

Modern technical writing for developer-facing products requires more than explaining technical concepts clearly.

As a technical writer, with this project, I demonstrated how documentation connects with:

* API architecture
* HTTP methods and status codes
* Authentication flows
* JSON request and response structures
* OpenAPI specifications
* Schema reuse
* API testing
* Version control
* Documentation tooling

This project was created to show those skills through a practical API documentation workflow using a real-world API.

## Final deliverable

The completed OpenAPI specification provides a structured representation of the documented TMDB API with:

* 51 API paths
* 52 operations
* Reusable component schemas
* Structured request and response definitions
* Representative response examples
* Explicit authentication and security schemes
* Error response modeling
* Pagination models
* Consistent API documentation
* OpenAPI 3.0 compatibility
* Mintlify-oriented documentation readiness

---

**Author:** Victoria Lazarus
**Focus:** Technical Writing · API Documentation · OpenAPI · Developer Documentation

