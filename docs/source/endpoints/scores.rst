=========
Scores
=========
|

Read Score from SunCoast RHIO Api
=====================================
|

This endpoint purpose is to get the score from a previous submissions made before it is delivered to the Client through their Api.

|

Detailed Specification
----------------------

|

+-----------------------+-------------+----------------------------------------------------+
| Endpoint              | Http Method | Path                                               |
+=======================+=============+====================================================+
|*score*                | POST        |https://suncoastapi.herokuapp.com/apisc/score       |
+-----------------------+-------------+----------------------------------------------------+

|

Curl example
''''''''''''
|

This is the correct way to ask for the responses from our Api:
::

    curl -X POST \
        https://suncoastapi.herokuapp.com/apisc/score \
        -H 'Authorization: Bearer Token_here' \
        -H 'Content-Type: application/json' \
        -d '{
            "taxpayerIdentificationNumber": "000465970",
            "nationalProviderIdentifier": "0912935270",
            "performanceYear": 2017
        }'



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
        "score": {
            "data": {
                "score": {
                    "detail": "0.36.3",
                    "errors": [],
                    "metadata": {
                        "maxContributionACI": 0,
                        "maxContributionIA": 15,
                        "maxContributionQuality": 85,
                        "maxFinalScore": 100,
                        "maxHighContributionIA": 20,
                        "maxMediumContributionIA": 10,
                        "messages": {}
                    },
                    "name": "total",
                    "parts": [
                        {
                            "detail": "Scoring based on weight of 85%.",
                            "metadata": {
                                "maxContribution": 85,
                                "unroundedScoreValue": 40.48833333333333
                            },
                            "name": "quality",
                            "original": {
                                "detail": "Picked the highest scoring measurement set registry",
                                "name": "quality",
                                "parts": [
                                    {
                                        "detail": "registry",
                                        "metadata": {
                                            "denominator": 60,
                                            "e2eBonusScore": 0,
                                            "maxContribution": 100,
                                            "maxMeasurementsAllowed": 6,
                                            "measurementSetId": "780d562d-d2ee-4889-9484-80d849a376ef",
                                            "measurementSetPicked": true,
                                            "measuresPicked": [
                                                "331",
                                                "317",
                                                "326",
                                                "415",
                                                "419",
                                                "332"
                                            ],
                                            "messages": {
                                                "denominator": "At least 1 high or outcome or patient experience measure available. So denominator is 60",
                                                "totalBonusPoints": "Sum of individual measurement bonus points",
                                                "totalMeasurementPoints": "Sum of applicable individual measurement points."
                                            },
                                            "reweightedScore": 28.6,
                                            "totalBonusPoints": 2,
                                            "totalMeasurementPoints": 28.6,
                                            "unroundedScoreValue": 28.58
                                        },
                                        "name": "quality",
                                        "parts": [
                                            {
                                                "detail": "Contributing 3",
                                                "metadata": {
                                                    "benchmarkType": "registry",
                                                    "decile": -1,
                                                    "decileScore": 3,
                                                    "deciles": null,
                                                    "eMeasureId": null,
                                                    "eligiblePopulation": 3,
                                                    "endToEndBonus": 0,
                                                    "endToEndBonusEligible": false,
                                                    "highPriorityBonus": 0,
                                                    "highPriorityBonusEligible": true,
                                                    "highPriorityBonusIgnored": true,
                                                    "measureClass": "Class 2",
                                                    "measureTitle": "Adult Sinusitis: Antibiotic Prescribed for Acute Sinusitis (Overuse)",
                                                    "measurementId": "ce19e632-41ce-487c-93d4-6e716b452188",
                                                    "measurementSetId": "780d562d-d2ee-4889-9484-80d849a376ef",
                                                    "messages": {
                                                        "decileScore": "Applied maximum points for Class 2 measure",
                                                        "e2eBonusScore": "Default E2E bonus score",
                                                        "highPriorityBonus": "Measure having highest decile score is not eligible for high priority bonus",
                                                        "measurementClass": "Measure has a benchmark but eligible population is less than 20 or has a reporting rate of less than 50%",
                                                        "measurementPicker": "Picked at 1",
                                                        "totalMeasurementPoints": "Measurement points for PICKED measure include decile score with all bonus points"
                                                    },
                                                    "noBenchmarks": false,
                                                    "outcomeOrPatientExperienceBonus": 0,
                                                    "partialDecileScore": null,
                                                    "partialPoints": 0,
                                                    "performanceDenominator": 3,
                                                    "performanceNumerator": 1,
                                                    "performanceRate": 33.33,
                                                    "processingStatus": "PICKED",
                                                    "reportingRate": 100,
                                                    "toppedOut": true,
                                                    "totalBonusPoints": 0,
                                                    "totalMeasurementPoints": 3,
                                                    "unroundedScoreValue": 3
                                                },
                                                "name": "331",
                                                "value": 3
                                            },
                                            {
                                                "detail": "Contributing 9.1",
                                                "metadata": {
                                                    "benchmarkType": "registry",
                                                    "decile": 9,
                                                    "decileScore": 9.12,
                                                    "deciles": [
                                                        0,
                                                        24.74,
                                                        35.48,
                                                        47.88,
                                                        62.15,
                                                        71.65,
                                                        79.37,
                                                        88.86,
                                                        98.88
                                                    ],
                                                    "eMeasureId": "CMS22v5",
                                                    "eligiblePopulation": 1185,
                                                    "endToEndBonus": 0,
                                                    "endToEndBonusEligible": false,
                                                    "highPriorityBonus": 0,
                                                    "highPriorityBonusEligible": false,
                                                    "measureClass": "Class 1",
                                                    "measureTitle": "Preventive Care and Screening: Screening for High Blood Pressure and Follow-Up Documented",
                                                    "measurementId": "0d9d0adf-4b90-4632-a94e-57355d3d1910",
                                                    "measurementSetId": "780d562d-d2ee-4889-9484-80d849a376ef",
                                                    "messages": {
                                                        "e2eBonusScore": "Default E2E bonus score",
                                                        "measurementClass": "Eligible population is greater than or equal to 20, reporting rate is greater than 50% and has benchmarks",
                                                        "measurementPicker": "Picked at 2",
                                                        "totalMeasurementPoints": "Measurement points for PICKED measure include decile score with all bonus points"
                                                    },
                                                    "noBenchmarks": false,
                                                    "outcomeOrPatientExperienceBonus": 0,
                                                    "partialDecileScore": 0.1,
                                                    "partialPoints": 1.17,
                                                    "performanceDenominator": 1184,
                                                    "performanceNumerator": 1066,
                                                    "performanceRate": 90.03,
                                                    "processingStatus": "PICKED",
                                                    "reportingRate": 99.92,
                                                    "toppedOut": false,
                                                    "totalBonusPoints": 0,
                                                    "totalMeasurementPoints": 9.12,
                                                    "unroundedScoreValue": 9.12
                                                },
                                                "name": "317",
                                                "value": 9.1
                                            },
                                            {
                                                "detail": "Contributing 5.5",
                                                "metadata": {
                                                    "benchmarkType": "registry",
                                                    "decile": 5,
                                                    "decileScore": 5.46,
                                                    "deciles": [
                                                        0,
                                                        20,
                                                        39.19,
                                                        52.34,
                                                        69.57,
                                                        76.19,
                                                        82.5,
                                                        94.34,
                                                        100
                                                    ],
                                                    "eMeasureId": null,
                                                    "eligiblePopulation": 73,
                                                    "endToEndBonus": 0,
                                                    "endToEndBonusEligible": false,
                                                    "highPriorityBonus": 0,
                                                    "highPriorityBonusEligible": false,
                                                    "measureClass": "Class 1",
                                                    "measureTitle": "Atrial Fibrillation and Atrial Flutter: Chronic Anticoagulation Therapy",
                                                    "measurementId": "87910ebf-4738-4146-8372-89f10406f403",
                                                    "measurementSetId": "780d562d-d2ee-4889-9484-80d849a376ef",
                                                    "messages": {
                                                        "e2eBonusScore": "Default E2E bonus score",
                                                        "measurementClass": "Eligible population is greater than or equal to 20, reporting rate is greater than 50% and has benchmarks",
                                                        "measurementPicker": "Picked at 3",
                                                        "totalMeasurementPoints": "Measurement points for PICKED measure include decile score with all bonus points"
                                                    },
                                                    "noBenchmarks": false,
                                                    "outcomeOrPatientExperienceBonus": 0,
                                                    "partialDecileScore": 0.5,
                                                    "partialPoints": 7.93,
                                                    "performanceDenominator": 73,
                                                    "performanceNumerator": 44,
                                                    "performanceRate": 60.27,
                                                    "processingStatus": "PICKED",
                                                    "reportingRate": 100,
                                                    "toppedOut": false,
                                                    "totalBonusPoints": 0,
                                                    "totalMeasurementPoints": 5.46,
                                                    "unroundedScoreValue": 5.46
                                                },
                                                "name": "326",
                                                "value": 5.5
                                            },
                                            {
                                                "detail": "Contributing 4",
                                                "metadata": {
                                                    "benchmarkType": null,
                                                    "decile": -1,
                                                    "decileScore": 3,
                                                    "deciles": null,
                                                    "eMeasureId": null,
                                                    "eligiblePopulation": 32,
                                                    "endToEndBonus": 0,
                                                    "endToEndBonusEligible": false,
                                                    "highPriorityBonus": 1,
                                                    "highPriorityBonusEligible": true,
                                                    "measureClass": "Class 2",
                                                    "measureTitle": "Emergency Medicine: Emergency Department Utilization of CT for Minor Blunt Head Trauma for Patients Aged 18 Years and Older",
                                                    "measurementId": "626ab835-453d-4713-a2e6-deaa2f70976f",
                                                    "measurementSetId": "780d562d-d2ee-4889-9484-80d849a376ef",
                                                    "messages": {
                                                        "decileScore": "Applied maximum points for Class 2 measure",
                                                        "e2eBonusScore": "Default E2E bonus score",
                                                        "highPriorityBonus": "Allotting 1 point to high priority bonus for measure type 'efficiency'",
                                                        "measurementClass": "Measurement has no benchmarks",
                                                        "measurementPicker": "Picked at 4",
                                                        "totalMeasurementPoints": "Measurement points for PICKED measure include decile score with all bonus points"
                                                    },
                                                    "noBenchmarks": true,
                                                    "outcomeOrPatientExperienceBonus": 0,
                                                    "partialDecileScore": null,
                                                    "partialPoints": 0,
                                                    "performanceDenominator": 32,
                                                    "performanceNumerator": 21,
                                                    "performanceRate": 65.62,
                                                    "processingStatus": "PICKED",
                                                    "reportingRate": 100,
                                                    "toppedOut": null,
                                                    "totalBonusPoints": 1,
                                                    "totalMeasurementPoints": 4,
                                                    "unroundedScoreValue": 4
                                                },
                                                "name": "415",
                                                "value": 4
                                            },
                                            {
                                                "detail": "Contributing 4",
                                                "metadata": {
                                                    "benchmarkType": null,
                                                    "decile": -1,
                                                    "decileScore": 3,
                                                    "deciles": null,
                                                    "eMeasureId": null,
                                                    "eligiblePopulation": 36,
                                                    "endToEndBonus": 0,
                                                    "endToEndBonusEligible": false,
                                                    "highPriorityBonus": 1,
                                                    "highPriorityBonusEligible": true,
                                                    "measureClass": "Class 2",
                                                    "measureTitle": "Overuse Of Neuroimaging For Patients With Primary Headache And A Normal Neurological Examination",
                                                    "measurementId": "2657e9ec-4ae3-4f04-b226-c98a4685f4f2",
                                                    "measurementSetId": "780d562d-d2ee-4889-9484-80d849a376ef",
                                                    "messages": {
                                                        "decileScore": "Applied maximum points for Class 2 measure",
                                                        "e2eBonusScore": "Default E2E bonus score",
                                                        "highPriorityBonus": "Allotting 1 point to high priority bonus for measure type 'efficiency'",
                                                        "measurementClass": "Measurement has no benchmarks",
                                                        "measurementPicker": "Picked at 5",
                                                        "totalMeasurementPoints": "Measurement points for PICKED measure include decile score with all bonus points"
                                                    },
                                                    "noBenchmarks": true,
                                                    "outcomeOrPatientExperienceBonus": 0,
                                                    "partialDecileScore": null,
                                                    "partialPoints": 0,
                                                    "performanceDenominator": 30,
                                                    "performanceNumerator": 27,
                                                    "performanceRate": 90,
                                                    "processingStatus": "PICKED",
                                                    "reportingRate": 83.33,
                                                    "toppedOut": null,
                                                    "totalBonusPoints": 1,
                                                    "totalMeasurementPoints": 4,
                                                    "unroundedScoreValue": 4
                                                },
                                                "name": "419",
                                                "value": 4
                                            },
                                            {
                                                "detail": "Contributing 3",
                                                "metadata": {
                                                    "benchmarkType": "registry",
                                                    "decile": -1,
                                                    "decileScore": 3,
                                                    "deciles": null,
                                                    "eMeasureId": null,
                                                    "eligiblePopulation": 2,
                                                    "endToEndBonus": 0,
                                                    "endToEndBonusEligible": false,
                                                    "highPriorityBonus": 0,
                                                    "highPriorityBonusEligible": false,
                                                    "measureClass": "Class 2",
                                                    "measureTitle": "Adult Sinusitis: Appropriate Choice of Antibiotic: Amoxicillin With or Without Clavulanate Prescribed for Patients with Acute Bacterial Sinusitis (Appropriate Use)",
                                                    "measurementId": "82378195-46ee-4c7e-8b69-95b375c48222",
                                                    "measurementSetId": "780d562d-d2ee-4889-9484-80d849a376ef",
                                                    "messages": {
                                                        "decileScore": "Applied maximum points for Class 2 measure",
                                                        "e2eBonusScore": "Default E2E bonus score",
                                                        "measurementClass": "Measure has a benchmark but eligible population is less than 20 or has a reporting rate of less than 50%",
                                                        "measurementPicker": "Picked at 6",
                                                        "totalMeasurementPoints": "Measurement points for PICKED measure include decile score with all bonus points"
                                                    },
                                                    "noBenchmarks": false,
                                                    "outcomeOrPatientExperienceBonus": 0,
                                                    "partialDecileScore": null,
                                                    "partialPoints": 0,
                                                    "performanceDenominator": 2,
                                                    "performanceNumerator": 1,
                                                    "performanceRate": 50,
                                                    "processingStatus": "PICKED",
                                                    "reportingRate": 100,
                                                    "toppedOut": false,
                                                    "totalBonusPoints": 0,
                                                    "totalMeasurementPoints": 3,
                                                    "unroundedScoreValue": 3
                                                },
                                                "name": "332",
                                                "value": 3
                                            }
                                        ],
                                        "value": 47.6
                                    }
                                ],
                                "value": 47.6
                            },
                            "title": "QUALITY component of final score",
                            "value": 40.49
                        },
                        {
                            "name": "feedback-quality",
                            "parts": [
                                {
                                    "detail": "Focus on improving measure 331",
                                    "name": "331"
                                },
                                {
                                    "detail": "Focus on improving measure 332",
                                    "name": "332"
                                },
                                {
                                    "detail": "Focus on improving measure 415",
                                    "name": "415"
                                }
                            ]
                        }
                    ],
                    "title": "Total Score",
                    "value": 40.49,
                    "warnings": [
                        "Disclaimer: Scoring is subject to change, based on periodic policy updates, eligibility reviews, and technical integration developments."
                    ]
                }
            }
        },
        "submissionId": "01e38cda-fb16-4a92-abd0-bfac25f1fbd3"
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
        "id": "CS-004",
        "message": "Submission identification data is not valid"
    }