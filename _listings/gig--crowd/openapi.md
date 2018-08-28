swagger: "2.0"
x-collection-name: GIG & CROWD
x-complete: 1
info:
  title: GIG & Crowd
  version: 1.0.0
host: gigandcrowd.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/place/scheme/{placeId}:
    post:
      summary: Post Place Scheme Placeid
      description: Post place scheme placeid.
      operationId: postApiV1PlaceSchemePlace
      x-api-path-slug: apiv1placeschemeplaceid-post
      parameters:
      - in: header
        name: Authorization
      - in: query
        name: file
      responses:
        200:
          description: OK
      tags:
      - Place
      - Scheme
      - Placeid