===========
Submissions
===========
|

Send Submissions to SunCoast RHIO Api
=====================================
|

This endpoint purpose is to receive valid submissions from our client, validate the data and attempt to insert the submission to CMS. Then store the response from CMS or return if there was an error within the data provided.

|

Detailed Specification
----------------------

|

+-----------------------+-------------+----------------------------------------------------+
| Endpoint              | Http Method | Path                                               |
+=======================+=============+====================================================+
|*processqpp*           | POST        |https://suncoastapi.herokuapp.com/apisc/processqpp  |
+-----------------------+-------------+----------------------------------------------------+

|

Curl example
''''''''''''
|

This is the correct way to send a valid JSON data to be processed within our Api:
::

    curl -X POST \
        https://suncoastapi.herokuapp.com/apisc/processqpp \
        -H 'Authorization: Bearer Token_here' \
        -H 'Content-Type: application/json' \
        -d '{
              "entityType": "individual",
              "taxpayerIdentificationNumber": "000456758",
              "nationalProviderIdentifier": "0876543210",
              "performanceYear": 2017,
              "measurementSets": [
                {
                  "measurements": [
                    {
                      "measureId": "IA_EPA_4",
                      "value": true
                    }
                  ],
                  "category": "ia",
                  "submissionMethod": "registry",
                  "performanceStart": "2017-01-01",
                  "performanceEnd": "2017-06-01",
                  "programName": "cpcPlus",
                  "practiceId": "G1234"
                },
                {
                  "category": "aci",
                  "submissionMethod": "registry",
                  "performanceStart": "2017-01-01",
                  "performanceEnd": "2017-06-01",
                  "programName": "cpcPlus",
                  "practiceId": "G1234",
                  "measurements": [
                    {
                      "measureId": "ACI_HIE_3",
                      "value": {
                        "numerator": 1,
                        "denominator": 2
                      }
                    },
                    {
                      "measureId": "ACI_PHCDRR_5",
                      "value": true
                    }
                  ]
                },
                {
                  "category": "quality",
                  "submissionMethod": "registry",
                  "performanceStart": "2017-01-01",
                  "performanceEnd": "2017-06-01",
                  "programName": "cpcPlus",
                  "practiceId": "G1234",
                  "measurements": [
                    {
                      "measureId": "391",
                      "value": {
                        "isEndToEndReported": false,
                        "strata": [
                          {
                            "performanceMet": 2,
                            "performanceNotMet": 1,
                            "eligiblePopulation": 10,
                            "eligiblePopulationException": 1,
                            "eligiblePopulationExclusion": 2,
                            "stratum": "30days"
                          },
                          {
                            "performanceMet": 2,
                            "performanceNotMet": 1,
                            "eligiblePopulation": 6,
                            "eligiblePopulationException": 1,
                            "eligiblePopulationExclusion": 0,
                            "stratum": "overall"
                          }
                        ]
                      }
                    },
                    {
                      "measureId": "093",
                      "value": {
                        "isEndToEndReported": false,
                        "performanceMet": 1,
                        "performanceNotMet": 1,
                        "eligiblePopulation": 5,
                        "eligiblePopulationExclusion": 1,
                        "eligiblePopulationException": 1
                      }
                    },
                    {
                      "measureId": "ACEP32",
                      "value": {
                        "numerator": 1.26,
                        "denominator": 2.91,
                        "isEndToEndReported": false
                      }
                    }
                  ]
                }
              ]
            }'

|

Response
''''''''

Success example
...............

Status

201

*Json format*
::

    {
        "response": "OK"
    }


Error example
...............

Status

422

*Json format*
::

    {
        "errors": [
            {
                "detail": {
                    "error": {
                        "details": [
                            {
                                "submissionId": "024a6d38-50b6-4bbb-9d77-d9b14ba0a174"
                            }
                        ],
                        "message": "Duplicate entry for key submission_category_method_submitter_type_program_name_practice",
                        "type": "DuplicateEntryError"
                    }
                },
                "id": "CMS-Error",
                "status": 422,
                "title": "error"
            }
        ]
    }