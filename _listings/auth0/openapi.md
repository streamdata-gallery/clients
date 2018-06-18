---
swagger: "2.0"
x-collection-name: Auth0
x-complete: 1
info:
  title: Auth0
  version: 1.0.0
host: login.auth0.com
basePath: /clients
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v2/clients:
    get:
      summary: Get Clients
      description: Get clients.
      operationId: get_clients
      x-api-path-slug: apiv2clients-get
      parameters:
      - in: query
        name: exclude_fields
        description: true if the fields specified are to be excluded from the result,
          false otherwise
      - in: query
        name: fields
        description: A comma separated list of fields to include or exclude (depending
          on exclude_fields) from the result
      responses:
        200:
          description: OK
      tags:
      - Clients
    post:
      summary: Post Clients
      description: Post clients.
      operationId: post_clients
      x-api-path-slug: apiv2clients-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Clients
  /api/v2/clients/{id}:
    delete:
      summary: Delete Clients
      description: Delete clients.
      operationId: delete_clients_by_id
      x-api-path-slug: apiv2clientsid-delete
      parameters:
      - in: path
        name: id
        description: The client_id of the client to delete
      responses:
        200:
          description: OK
      tags:
      - Clients
    get:
      summary: Get Clients
      description: Get clients.
      operationId: get_clients_by_id
      x-api-path-slug: apiv2clientsid-get
      parameters:
      - in: query
        name: exclude_fields
        description: true if the fields specified are to be excluded from the result,
          false otherwise
      - in: query
        name: fields
        description: A comma separated list of fields to include or exclude (depending
          on exclude_fields) from the result
      - in: path
        name: id
        description: The client_id of the client to retrieve
      responses:
        200:
          description: OK
      tags:
      - Clients
    patch:
      summary: Patch Clients
      description: Patch clients.
      operationId: patch_clients_by_id
      x-api-path-slug: apiv2clientsid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: The client_id of the client to retrieve
      responses:
        200:
          description: OK
      tags:
      - Clients
---