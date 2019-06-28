# Detailed Evaluation Report for `GraphQL` paper.

## REST

GET `GAD 7` questionnaire - `RESTful` approach. Response JSON:

```
{
  "data": {
    "Questionnaire": {
      "id": "5cf13f09ced5b613494b54cc",
      "meta": {
        "profile": [
          "http://hl7.org/fhir/StructureDefinition/cqif-questionnaire"
        ]
      },
      "text": {
        "status": "generated",
        "div": "<div xmlns=\"http://www.w3.org/1999/xhtml\">Major Depression Inventory</div>"
      },
      "identifier": [
        {
          "use": "official",
          "value": "depression-mdi"
        }
      ],
      "title": "Major Depression Inventory",
      "version": "1.0.0",
      "status": "active",
      "code": [],
      "subjectType": [
        "Patient"
      ],
      "item": [
        {
          "linkId": "depression-mdi01",
          "type": "choice",
          "required": true,
          "text": "Have you felt low in spirits or sad?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi02",
          "type": "choice",
          "required": true,
          "text": "Have you lost interest in your daily activities?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi03",
          "type": "choice",
          "required": true,
          "text": "Have you felt lacking in energy and strength?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi04",
          "type": "choice",
          "required": true,
          "text": "Have you felt less self-confident?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi05",
          "type": "choice",
          "required": true,
          "text": "Have you had a bad conscience or feelings of guilt?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi06",
          "type": "choice",
          "required": true,
          "text": "Have you felt that life wasn’t worth living?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi07",
          "type": "choice",
          "required": true,
          "text": "Have you had difficulty in concentrating?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi08",
          "type": "choice",
          "required": true,
          "text": "Have you felt very restless?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi09",
          "type": "choice",
          "required": true,
          "text": "Have you felt subdued or slowed down?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi10",
          "type": "choice",
          "required": true,
          "text": "Have you had trouble sleeping at night?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi11",
          "type": "choice",
          "required": true,
          "text": "Have you suffered from reduced appetite?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "linkId": "depression-mdi12",
          "type": "choice",
          "required": true,
          "text": "Have you suffered from increased appetite?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "meta": {
              "versionId": null,
              "lastUpdated": null
            },
            "url": "http://mhof.ml/ValueSet/MHOFVS006",
            "identifier": [
              {
                "system": "urn:ietf:rfc:3986",
                "value": "urn:oid:1.3.6.1.4.1.12009.10.1.158"
              }
            ],
            "version": "Beta.1",
            "name": "MDI",
            "status": "active",
            "publisher": "INTROMAT",
            "copyright": null,
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "code": "MHOFVS006-1",
                      "extension": [
                        {
                          "valueDecimal": 5,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "code": "MHOFVS006-2",
                      "extension": [
                        {
                          "valueDecimal": 4,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "code": "MHOFVS006-3",
                      "extension": [
                        {
                          "valueDecimal": 3,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "code": "MHOFVS006-4",
                      "extension": [
                        {
                          "valueDecimal": 2,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "code": "MHOFVS006-5",
                      "extension": [
                        {
                          "valueDecimal": 1,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "code": "MHOFVS006-6",
                      "extension": [
                        {
                          "valueDecimal": 0,
                          "url": "http://hl7.org/fhir/StructureDefinition/valueset-ordinalValue"
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        }
      ]
    }
  }
}
```

## GraphQL

GET `GAD-7` only required attributes `GraphQL`. Response JSON:

```
{
  "data": {
    "Questionnaire": {
      "title": "Major Depression Inventory",
      "item": [
        {
          "text": "Have you felt low in spirits or sad?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you lost interest in your daily activities?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you felt lacking in energy and strength?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you felt less self-confident?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you had a bad conscience or feelings of guilt?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you felt that life wasn’t worth living?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you had difficulty in concentrating?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you felt very restless?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you felt subdued or slowed down?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you had trouble sleeping at night?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you suffered from reduced appetite?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        },
        {
          "text": "Have you suffered from increased appetite?",
          "answerValueSet": {
            "id": "5cf13f09ced5b613494b54bc",
            "compose": {
              "include": [
                {
                  "concept": [
                    {
                      "display": "All The Time",
                      "extension": [
                        {
                          "valueDecimal": 5
                        }
                      ]
                    },
                    {
                      "display": "Most Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 4
                        }
                      ]
                    },
                    {
                      "display": "Slightly More Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 3
                        }
                      ]
                    },
                    {
                      "display": "Slightly Less Than Half The Time",
                      "extension": [
                        {
                          "valueDecimal": 2
                        }
                      ]
                    },
                    {
                      "display": "Some Of The Time",
                      "extension": [
                        {
                          "valueDecimal": 1
                        }
                      ]
                    },
                    {
                      "display": "At No Time",
                      "extension": [
                        {
                          "valueDecimal": 0
                        }
                      ]
                    }
                  ]
                }
              ]
            }
          }
        }
      ]
    }
  }
}
```
