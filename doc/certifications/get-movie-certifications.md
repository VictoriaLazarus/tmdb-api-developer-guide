# Get Movie Certifications

## Overview

Returns movie certification ratings grouped by country.

## Endpoint

GET /certification/movie/list

## Authentication

Bearer Token

## cURL Request

```bash
curl --request GET \
  --url 'https://api.themoviedb.org/3/certification/movie/list' \
  --header 'Authorization: Bearer YOUR_ACCESS_TOKEN'
```