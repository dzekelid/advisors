---
swagger: "2.0"
x-collection-name: Vestorly
x-complete: 1
info:
  title: Vestorly
  description: vestorly-developers-api
  termsOfService: http://www.vestorly.com/terms/
  contact:
    name: Vestorly Team
  version: 1.0.0
host: staging.vestorly.com
basePath: /api/v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /advisors/{id}:
    get:
      summary: Get Advisors
      description: Returns a single advisor given their ID
      operationId: findAdvisorByID
      x-api-path-slug: advisorsid-get
      parameters:
      - in: query
        name: access_token
        description: OAuth Token
      - in: path
        name: id
        description: Advisor Id to fetch
      - in: query
        name: vestorly-auth
        description: Vestorly Auth Token
      - in: query
        name: vestorly_auth
        description: Vestorly Auth Token
      responses:
        200:
          description: OK
      tags:
      - Advisors
---