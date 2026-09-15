# TMDB API — OpenAPI Documentation Project

A portfolio project demonstrating practical API documentation, testing, OpenAPI modeling, and documentation QA using **The Movie Database (TMDB) API**.

The project takes a real-world REST API from endpoint exploration and testing in **Postman** through OpenAPI generation, technical review, refinement, and preparation for developer-facing documentation.

The focus was on creating an API reference that is **accurate, consistent, maintainable, and useful to developers**.

## Project overview

The project documents **52 API operations across 51 paths**, covering:

* Authentication
* Account
* Certification
* Search
* Discover
* Movies
* Network

The final OpenAPI specification defines API operations, parameters, request bodies, responses, authentication requirements, reusable schemas, and representative examples.

## Documentation workflow

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
Request, response, schema, authentication, and documentation QA
   ↓
OpenAPI specification prepared for Mintlify
```

This workflow combines API testing with a documentation-as-code approach, with the OpenAPI specification maintained as a version-controlled technical artifact.

## What I worked on

### API exploration and testing

I used Postman to explore and test the TMDB API before refining the resulting documentation.

This included:

* Testing API endpoints and HTTP methods
* Working with path, query, and request-body parameters
* Testing authentication and session workflows
* Investigating successful and error responses
* Saving representative response examples
* Organizing endpoints into logical API groups
* Documenting request requirements and endpoint behavior

The Postman collection contains **52 documented operations** across authentication, account, certification, search, discover, movie, and network functionality.

### OpenAPI structure and refinement

The generated OpenAPI specification was reviewed extensively rather than used as-is.

I:

* Standardized operation IDs and endpoint structure
* Corrected malformed paths and URLs
* Verified path parameter definitions
* Reviewed parameter types and required status
* Structured and validated request bodies
* Defined response objects and status codes
* Added and refined reusable component schemas
* Reviewed internal `$ref` relationships
* Maintained OpenAPI 3.0 compatibility
* Removed inappropriate generated artifacts
* Corrected inconsistencies between the generated specification and the documented API behavior

### Request and response modeling

The specification uses reusable schemas to model common API structures across multiple endpoints.

These include schemas for:

* Movies and TV shows
* People
* Accounts
* Search and discover results
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

Where response structures are shared across endpoints, reusable component schemas are used to improve consistency and maintainability.

### Authentication and security

Authentication was reviewed as part of both the API implementation and the documentation.

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

I also reviewed authentication requirements against individual endpoint workflows to distinguish application authentication from user-authenticated operations where different credentials or token types are required.

Credential-like values were removed from the project artifacts and replaced with safe placeholders where appropriate.

### Documentation quality

The specification was reviewed as a developer-facing API reference, with attention to both technical accuracy and usability.

The review included:

* Consistent TMDB terminology
* Corrected terminology, grammar, and typographical errors
* Standardized endpoint summaries and descriptions
* Corrected malformed URLs and paths
* Verified request and response structures
* Reviewed parameter names, types, and required status
* Defined required request-body fields
* Improved response and error descriptions
* Removed irrelevant captured response artifacts
* Aligned authentication requirements with documented requests
* Improved consistency across related endpoints and API workflows

The result is a specification designed to work both as machine-readable API metadata and as a foundation for developer-facing reference documentation.

## Validation and quality assurance

The completed specification was reviewed for structural correctness, consistency, and documentation quality.

| Check                                  |  Result |
| -------------------------------------- | ------: |
| OpenAPI version                        |   3.0.0 |
| API paths                              |      51 |
| Operations                             |      52 |
| Unique operation IDs                   | 52 / 52 |
| Broken local `$ref`s                   |       0 |
| Empty response definitions             |       0 |
| Missing path parameters                |       0 |
| Invalid nullable syntax                |       0 |
| Malformed account paths                |       0 |
| Invalid `softcore` references          |       0 |
| Broken documentation URLs              |       0 |
| Incorrect `session_id` requirement     |       0 |
| Request bodies missing required fields |       0 |

The specification was also reviewed for consistency between its machine-readable definitions and the accompanying endpoint documentation.

## Tools and technologies

* Postman
* OpenAPI 3.0
* YAML
* REST APIs
* JSON
* VS Code
* Git
* GitHub
* Swagger Editor
* Mintlify

## Repository structure

```text
tmdb-api-developer-guide/
├── openapi/
│   └── tmdb-openapi.yaml
├── postman/
│   └── tmdb-api-collection.json
├── assets/
│   └── images/
├── README.md
└── .gitignore
```

### Main deliverables

**OpenAPI specification**

```text
openapi/tmdb-openapi.yaml
```

The primary technical artifact containing the refined API reference, request and response models, authentication schemes, reusable schemas, and documentation metadata.

**Postman collection**

```text
postman/tmdb-api-collection.json
```

The testing and exploration artifact used to investigate endpoint behavior, authentication flows, request requirements, and representative responses.

## Why I built this

I built this project to demonstrate the practical side of developer-focused technical writing: working with APIs, testing requests, understanding authentication flows, structuring OpenAPI specifications, and refining technical information for developer use.

Rather than documenting an API only as prose, I wanted the project to demonstrate how a technical writer can work across **API tooling, structured specifications, testing, version control, and documentation quality**.

## Author

**Victoria Lazarus**

Technical Writing · API Documentation · OpenAPI · Developer Documentation
