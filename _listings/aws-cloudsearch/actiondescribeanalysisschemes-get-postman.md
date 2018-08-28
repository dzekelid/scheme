{
  "info": {
    "name": "AWS CloudSearch Describe Analysis Schemes",
    "_postman_id": "5739345d-e98a-4806-a7ff-28aaa57181ec",
    "description": "Gets the analysis schemes configured for a domain.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analysis Scheme",
      "item": [
        {
          "id": "2ccbaf2e-a807-47d3-b120-80ff63eb1bc2",
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
              "id": "9ba3fcff-447d-4763-9519-88dab29d0309"
            }
          ]
        },
        {
          "id": "fee27ad6-ec4a-4d45-964a-6f655c4b34c8",
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
              "id": "27239f7e-94ad-4f76-8c5b-9b252c7f2119"
            }
          ]
        },
        {
          "id": "ef09fd93-27bb-4ddc-bebc-e56322291018",
          "name": "DescribeAnalysisSchemes",
          "request": {
            "url": "http://example.com/api/?Action=DescribeAnalysisSchemes?AnalysisSchemeNames.member.N=AnalysisSchemeNames.member.N&Deployed=Deployed&DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the analysis schemes configured for a domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b52b0069-a90c-48e8-b667-fd56c147b6c0"
            }
          ]
        }
      ]
    }
  ]
}