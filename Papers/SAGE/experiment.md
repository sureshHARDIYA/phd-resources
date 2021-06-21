## Experiments

This section outlines the background, methods and results of the experiments carried out during this study. Once the architecture was setup, and prototype was developed, we carried out experiment on local computer to keep result homogeneous.

## Experimental environment

All the software application components were running on Predator Acer Triton 500 with 32 GB of RAM, 1 TB SDD, 2070 RTX GPU with Ubuntu Linux distribution. Mobile application was installed on Apple iPhone 7 Plus. All the communication happened over HTTPS.

## Methods

This paper advocates a method for communicating between heterogeneous EHR systems. Communication over Internet involves HTTP requests and response that includes reading resources (Read), creating resources (Create), updating resources (Update), and deleting resources (Delete). To test those, we created following queries to test CRUD and measured their average response and throughput. The associated GraphQL queries for each of them are listed below:

### Q1: Read all patients resource

```
query PatientList {
  PatientList {
    entry {
      resource {
        ...on Patient {
          id
          resourceType
          name { family }
        }
      }
    }
  }
}
```

### Q2: Read a single patient resource

```
query Person {
    Patient(_id: "5dcaa7f02eb0b70e90761396"){
        name {
            use
            text
            family
        }
        birthDate
        gender
        active
        address {
            line
        }
    }
}
```

### Q3: Read all Encounter resource

```
query EncounterList {
  EncounterList {
    entry {
      resource {
        ...on Encounter {
          id
          resourceType
          status
        }
      }
    }
  }
}
```

### Q4: Read a single Encounter resource

```
query Encounter{

    Encounter(_id: "5dcd0b739f814f507c1cb86e"){
        id
        status
    }
}

```

### Q5: Read all Location resource

```
query LocationList {
  LocationList {
    entry {
      resource {
        ...on Location {
          id
          resourceType
          status
        }
      }
    }
  }
}

```

### Q6: Read a single Location resource

```
query Location{

    Location(_id: "5dcbfe529f0ecb264c1790ef"){
        id
        name
    }

}
```

### Q7: Read all observations resource

```
query ObservationList {
  ObservationList {
    entry {
      resource {
        ...on Observation {
          id
          resourceType
        }
      }
    }
  }
}
```

### Q8: Read a single observation resource

```
query Observation {
    Observation(_id: "5dcc0734d39e0045d82b6eae") {
        id
        status
    }
}
```

### Q9: Create a patient resource

```
mutation PatientCreate {
  PatientCreate(resource: {
      resourceType: Patient
      name: [
        {
          use: "official",
          family: "Chalmers",
          given: [
            "Peter",
            "James"
          ]
        },
        {
          use: "usual",
          given: [
            "Jim"
          ]
        },
        {
          use: "maiden",
          family: "Windsor",
          given: [
            "Peter",
            "James"
          ],
          period: {
            end: "2002"
          }
        }
      ]
      gender: "male"
    contact: [
    {

      name: {
        text: "mr. F. de Hond"
      },
      telecom: [
        {
          system: "phone",
          value: "022-655 7654"
        },
        {
          system: "email",
          value: "KNO@burgersumc.nl"
        },
        {
          system: "fax",
          value: "022-655 0998"
        }
      ],
      address: {
        line: [
          "West Wing, floor 5"
        ]
      }
    }
  ]
      telecom: [
      {
        use: "home"
      },
      {
        system: "phone",
        value: "(03) 5555 6473",
        use: "work",
        rank: "1"
      },
      {
        system: "phone",
        value: "(03) 3410 5613",
        use: "mobile",
        rank: "2"
      },
      {
        system: "phone",
        value: "(03) 5555 8834",
        use: "old",
        period: {
          end: "2014"
        }
      }
    ]
    active: true
      address: [
        {
          type: "postal"
          line: ["3300 Washtenaw Avenue, Suite 227"]
          city: "Ann Arbor"
          state: "MI"
          postalCode: "48104"
          country: "USA"
        }
      ],
    identifier: [
      {
        use: "usual",
        type: {
          coding: [
            {
              system: "http://terminology.hl7.org/CodeSystem/v2-0203",
              code: "MR"
            }
          ]
        },
        system: "urn:oid:1.2.36.146.595.217.0.1",
        value: "12345",
        period: {
          start: "2001-05-06"
        },
        assigner: {
          display: "Acme Healthcare"
        }
      }
    ],
    }
  ) {
    id
    resourceType
    name { family }
    address {
      id
      line
      type
    }
    identifier {
      use,
      assigner {
        display
      }
    }
    identifier {
      use,
      assigner {
        display
      }
    }
  }
}
```

### Q10: Update an Encounter resource

```
mutation EncounterUpdate{
    EncounterUpdate( id: "5dcd0b739f814f507c1cb86e", resource: {
  resourceType: Encounter,
  status: "arrived",
  class: {
    system: "http://terminology.hl7.org/CodeSystem/v3-ActCode",
    code: "IMP",
    display: "inpatient encounter",
  },
  }
)
  {
    id
    status
  }
}

```

### Q11: Delete an Encounter resource

```
mutation EncounterRemove{
    EncounterRemove( id: "60c75d3db794ab67ed828458"){

    id
    }
}
```

- Query by Mobile Client GraphQL based Resource Server (C1)
- Query by Mobile Client to OpenMRS (C2)
- Query by Mobile client to OpenMRS and then write to Resource Server (C3)

### Results

The response time and responsize size by each of these queires are tabulated in [Excel file]().
