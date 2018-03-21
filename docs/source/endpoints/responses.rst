=========
Responses
=========
|

Read Responses from SunCoast RHIO Api
=====================================
|

This endpoint purpose is to provide a list of the responses available from previous submissions made. We only save valid submissions responses from CMS. This responses will be delivered lately to the customer backend through their api.

|

Detailed Specification
----------------------

|

+-----------------------+-------------+----------------------------------------------------+
| Endpoint              | Http Method | Path                                               |
+=======================+=============+====================================================+
|*responses*            | GET         |https://suncoastapi.herokuapp.com/apisc/responses   |
+-----------------------+-------------+----------------------------------------------------+

|

Curl example
''''''''''''
|

This is the correct way to ask for the responses from our Api:
::

    curl -X GET \
        https://suncoastapi.herokuapp.com/apisc/responses \
        -H 'Authorization: Bearer Token_here' \
        -H 'Content-Type: application/json' \


|

Response
''''''''

Success example
...............

Status Code

200

*Json format*
::

    {
        "responses": [
            {
                "data": {
                    "submission": {
                        "createdAt": "2018-03-21T07:17:51Z",
                        "entityId": "",
                        "entityType": "individual",
                        "id": "0249c09f-8a07-4920-aad1-3e2217d486b9",
                        "measurementSets": [
                            {
                                "category": "ia",
                                "createdAt": "2018-03-21T07:17:51Z",
                                "id": "0249c09f-5032-4894-9531-1d620fc35bb3",
                                "measureSet": null,
                                "measurements": [
                                    {
                                        "id": "0249c09f-14b1-43a0-806c-0c978d4f03ec",
                                        "measureId": "IA_EPA_4",
                                        "measurementSetId": "0249c09f-5032-4894-9531-1d620fc35bb3",
                                        "value": true
                                    }
                                ],
                                "performanceEnd": "2017-06-01",
                                "performanceStart": "2017-01-01",
                                "practiceId": "G1234",
                                "programName": "cpcPlus",
                                "submissionId": "0249c09f-8a07-4920-aad1-3e2217d486b9",
                                "submissionMethod": "registry",
                                "submitterId": "1234567",
                                "submitterType": "organization",
                                "updatedAt": "2018-03-21T07:17:51Z"
                            },
                            {
                                "category": "quality",
                                "createdAt": "2018-03-21T07:17:51Z",
                                "id": "0249c0a0-f25d-497a-a060-d919cbc3687a",
                                "measureSet": null,
                                "measurements": [
                                    {
                                        "id": "0249c0a0-46a1-4235-8973-bd8fcd73573c",
                                        "measureId": "093",
                                        "measurementSetId": "0249c0a0-f25d-497a-a060-d919cbc3687a",
                                        "value": {
                                            "eligiblePopulation": 5,
                                            "eligiblePopulationException": 1,
                                            "eligiblePopulationExclusion": 1,
                                            "isEndToEndReported": false,
                                            "performanceMet": 1,
                                            "performanceNotMet": 1,
                                            "performanceRate": 50,
                                            "reportingRate": 80
                                        }
                                    },
                                    {
                                        "id": "0249c0a0-3228-4c46-bcd9-96ba263dce54",
                                        "measureId": "391",
                                        "measurementSetId": "0249c0a0-f25d-497a-a060-d919cbc3687a",
                                        "value": {
                                            "isEndToEndReported": false,
                                            "performanceRate": 66.67,
                                            "reportingRate": 66.67,
                                            "strata": [
                                                {
                                                    "eligiblePopulation": 10,
                                                    "eligiblePopulationException": 1,
                                                    "eligiblePopulationExclusion": 2,
                                                    "id": "0249c0a0-fbf8-4f13-ac10-125f2720dff1",
                                                    "measurementId": "0249c0a0-3228-4c46-bcd9-96ba263dce54",
                                                    "performanceMet": 2,
                                                    "performanceNotMet": 1,
                                                    "stratum": "30days"
                                                },
                                                {
                                                    "eligiblePopulation": 6,
                                                    "eligiblePopulationException": 1,
                                                    "eligiblePopulationExclusion": 0,
                                                    "id": "0249c0a0-03c9-4be7-be2a-03f0c14f14bc",
                                                    "measurementId": "0249c0a0-3228-4c46-bcd9-96ba263dce54",
                                                    "performanceMet": 2,
                                                    "performanceNotMet": 1,
                                                    "stratum": "overall"
                                                }
                                            ]
                                        }
                                    },
                                    {
                                        "id": "0249c0a0-6736-4b9f-8f2e-81914e14a81c",
                                        "measureId": "ACEP32",
                                        "measurementSetId": "0249c0a0-f25d-497a-a060-d919cbc3687a",
                                        "value": {
                                            "denominator": 2.91,
                                            "denominatorException": null,
                                            "isEndToEndReported": false,
                                            "numerator": 1.26,
                                            "numeratorExclusion": null
                                        }
                                    }
                                ],
                                "performanceEnd": "2017-06-01",
                                "performanceStart": "2017-01-01",
                                "practiceId": "G1234",
                                "programName": "cpcPlus",
                                "submissionId": "0249c09f-8a07-4920-aad1-3e2217d486b9",
                                "submissionMethod": "registry",
                                "submitterId": "1234567",
                                "submitterType": "organization",
                                "updatedAt": "2018-03-21T07:17:51Z"
                            },
                            {
                                "category": "aci",
                                "createdAt": "2018-03-21T07:17:51Z",
                                "id": "0249c0a0-dcb7-4814-916b-60bf76985627",
                                "measureSet": null,
                                "measurements": [
                                    {
                                        "id": "0249c0a0-2b25-4763-8365-ffe336db4f6f",
                                        "measureId": "ACI_HIE_3",
                                        "measurementSetId": "0249c0a0-dcb7-4814-916b-60bf76985627",
                                        "value": {
                                            "denominator": 2,
                                            "numerator": 1
                                        }
                                    },
                                    {
                                        "id": "0249c0a0-1020-44eb-a2a9-641a1f2753ed",
                                        "measureId": "ACI_PHCDRR_5",
                                        "measurementSetId": "0249c0a0-dcb7-4814-916b-60bf76985627",
                                        "value": true
                                    }
                                ],
                                "performanceEnd": "2017-06-01",
                                "performanceStart": "2017-01-01",
                                "practiceId": "G1234",
                                "programName": "cpcPlus",
                                "submissionId": "0249c09f-8a07-4920-aad1-3e2217d486b9",
                                "submissionMethod": "registry",
                                "submitterId": "1234567",
                                "submitterType": "organization",
                                "updatedAt": "2018-03-21T07:17:51Z"
                            }
                        ],
                        "nationalProviderIdentifier": "0876543210",
                        "performanceYear": 2017,
                        "taxpayerIdentificationNumber": "000456759",
                        "updatedAt": "2018-03-21T07:17:51Z"
                    }
                }
            },
            {
                "data": {
                    "submission": {
                        "createdAt": "2018-03-21T19:34:16Z",
                        "entityId": "",
                        "entityType": "individual",
                        "id": "024a6d38-50b6-4bbb-9d77-d9b14ba0a174",
                        "measurementSets": [
                            {
                                "category": "ia",
                                "createdAt": "2018-03-21T19:34:16Z",
                                "id": "024a6d38-b692-498b-a128-9e3227590f11",
                                "measureSet": null,
                                "measurements": [
                                    {
                                        "id": "024a6d38-13c5-4f8c-81b6-f3781d8f602a",
                                        "measureId": "IA_EPA_4",
                                        "measurementSetId": "024a6d38-b692-498b-a128-9e3227590f11",
                                        "value": true
                                    }
                                ],
                                "performanceEnd": "2017-06-01",
                                "performanceStart": "2017-01-01",
                                "practiceId": "G1234",
                                "programName": "cpcPlus",
                                "submissionId": "024a6d38-50b6-4bbb-9d77-d9b14ba0a174",
                                "submissionMethod": "registry",
                                "submitterId": "1234567",
                                "submitterType": "organization",
                                "updatedAt": "2018-03-21T19:34:16Z"
                            },
                            {
                                "category": "quality",
                                "createdAt": "2018-03-21T19:34:16Z",
                                "id": "024a6d39-8dd4-4258-9eb8-a43639f240d1",
                                "measureSet": null,
                                "measurements": [
                                    {
                                        "id": "024a6d39-411c-47b5-925d-3813f5af0a1b",
                                        "measureId": "093",
                                        "measurementSetId": "024a6d39-8dd4-4258-9eb8-a43639f240d1",
                                        "value": {
                                            "eligiblePopulation": 5,
                                            "eligiblePopulationException": 1,
                                            "eligiblePopulationExclusion": 1,
                                            "isEndToEndReported": false,
                                            "performanceMet": 1,
                                            "performanceNotMet": 1,
                                            "performanceRate": 50,
                                            "reportingRate": 80
                                        }
                                    },
                                    {
                                        "id": "024a6d39-37b6-4422-9c13-a9f02f0afd7d",
                                        "measureId": "391",
                                        "measurementSetId": "024a6d39-8dd4-4258-9eb8-a43639f240d1",
                                        "value": {
                                            "isEndToEndReported": false,
                                            "performanceRate": 66.67,
                                            "reportingRate": 66.67,
                                            "strata": [
                                                {
                                                    "eligiblePopulation": 10,
                                                    "eligiblePopulationException": 1,
                                                    "eligiblePopulationExclusion": 2,
                                                    "id": "024a6d39-0af6-4ff0-b48f-3b8faa5075ed",
                                                    "measurementId": "024a6d39-37b6-4422-9c13-a9f02f0afd7d",
                                                    "performanceMet": 2,
                                                    "performanceNotMet": 1,
                                                    "stratum": "30days"
                                                },
                                                {
                                                    "eligiblePopulation": 6,
                                                    "eligiblePopulationException": 1,
                                                    "eligiblePopulationExclusion": 0,
                                                    "id": "024a6d39-88b0-4fea-9388-6e0f314333e8",
                                                    "measurementId": "024a6d39-37b6-4422-9c13-a9f02f0afd7d",
                                                    "performanceMet": 2,
                                                    "performanceNotMet": 1,
                                                    "stratum": "overall"
                                                }
                                            ]
                                        }
                                    },
                                    {
                                        "id": "024a6d39-6aa0-4d4c-a7bb-760638c2c691",
                                        "measureId": "ACEP32",
                                        "measurementSetId": "024a6d39-8dd4-4258-9eb8-a43639f240d1",
                                        "value": {
                                            "denominator": 2.91,
                                            "denominatorException": null,
                                            "isEndToEndReported": false,
                                            "numerator": 1.26,
                                            "numeratorExclusion": null
                                        }
                                    }
                                ],
                                "performanceEnd": "2017-06-01",
                                "performanceStart": "2017-01-01",
                                "practiceId": "G1234",
                                "programName": "cpcPlus",
                                "submissionId": "024a6d38-50b6-4bbb-9d77-d9b14ba0a174",
                                "submissionMethod": "registry",
                                "submitterId": "1234567",
                                "submitterType": "organization",
                                "updatedAt": "2018-03-21T19:34:16Z"
                            },
                            {
                                "category": "aci",
                                "createdAt": "2018-03-21T19:34:16Z",
                                "id": "024a6d38-3e75-42b5-99a5-1baf3dddedc0",
                                "measureSet": null,
                                "measurements": [
                                    {
                                        "id": "024a6d38-2194-47d4-8644-2593db9bcb38",
                                        "measureId": "ACI_HIE_3",
                                        "measurementSetId": "024a6d38-3e75-42b5-99a5-1baf3dddedc0",
                                        "value": {
                                            "denominator": 2,
                                            "numerator": 1
                                        }
                                    },
                                    {
                                        "id": "024a6d38-1a7e-4d18-b444-fc92679ca5ea",
                                        "measureId": "ACI_PHCDRR_5",
                                        "measurementSetId": "024a6d38-3e75-42b5-99a5-1baf3dddedc0",
                                        "value": true
                                    }
                                ],
                                "performanceEnd": "2017-06-01",
                                "performanceStart": "2017-01-01",
                                "practiceId": "G1234",
                                "programName": "cpcPlus",
                                "submissionId": "024a6d38-50b6-4bbb-9d77-d9b14ba0a174",
                                "submissionMethod": "registry",
                                "submitterId": "1234567",
                                "submitterType": "organization",
                                "updatedAt": "2018-03-21T19:34:16Z"
                            }
                        ],
                        "nationalProviderIdentifier": "0876543210",
                        "performanceYear": 2017,
                        "taxpayerIdentificationNumber": "000456758",
                        "updatedAt": "2018-03-21T19:34:16Z"
                    }
                }
            }
        ]
    }

|

Error example
...............

Status Code

406

*Json format*
::

    {
        "error": "not acceptable",
        "id": "RN-001",
        "message": "Invalid data provided"
    }