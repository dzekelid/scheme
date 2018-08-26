{
  "info": {
    "name": "AWS CloudSearch Delete Analysis Scheme",
    "_postman_id": "3a05fb2d-e4a8-4af1-a951-2f7174299894",
    "description": "Deletes an analysis scheme.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analysis Scheme",
      "item": [
        {
          "id": "e199933d-5183-448c-8fb8-ba4eb1eb7a05",
          "name": "DefineAnalysisScheme",
          "request": {
            "url": "http://example.com/api/?Action=DefineAnalysisScheme?AnalysisScheme=AnalysisScheme&DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Configures an analysis scheme that can be applied to a text or text-array field to define language-specific text processing options."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e905da88-89b8-4d27-a77e-6bb022b58918"
            }
          ]
        },
        {
          "id": "9ac52413-26a4-42bb-aff9-f7aaf6de307b",
          "name": "DeleteAnalysisScheme",
          "request": {
            "url": "http://example.com/api/?Action=DeleteAnalysisScheme?AnalysisSchemeName=AnalysisSchemeName&DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an analysis scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e3e0c14f-4fac-42e2-a53a-16e98eb609a8"
            }
          ]
        }
      ]
    }
  ]
}