---
swagger: "2.0"
x-collection-name: GIG & CROWD
x-complete: 0
info:
  title: GIGANDCROWD Post Place Scheme Placeid
  version: 1.0.0
  description: Post place scheme placeid.
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
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---