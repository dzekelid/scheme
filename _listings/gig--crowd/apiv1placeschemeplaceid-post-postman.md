{
  "info": {
    "name": "GIGANDCROWD Post Place Scheme Placeid",
    "_postman_id": "ba50f0dc-5e71-4f19-a82b-e14896724fe7",
    "description": "Post place scheme placeid.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Place",
      "item": [
        {
          "id": "546999c8-40fc-41a1-81b1-6d2f124f8166",
          "name": "postApiV1PlaceSchemePlace",
          "request": {
            "url": {
              "protocol": "http",
              "host": "gigandcrowd.com",
              "path": [
                "api/v1/place/scheme/:placeId"
              ],
              "query": [
                {
                  "key": "file",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "placeId",
                  "value": "placeId",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Post place scheme placeid."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "76715fed-0cf9-4f42-b6d6-e08ff8589ab4"
            }
          ]
        }
      ]
    }
  ]
}