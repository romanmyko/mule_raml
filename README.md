# mule_raml

Folder
├── datatypes
│   ├── capsulesAllDataType.raml
│   ├── 
│   ├── 
│   ├── 
│   ├──
│   ├── ......
│   └── capsulesAllDataType.raml
├── examples
│   ├── capsuleAll.json
│   └── capsuleAll.json
├── traits
│   ├── commonTraits.raml
│   ├── .......
│   └── errorResponse.raml
spacex-system-api4.raml


traits:
  common: !include traits/commonTraits.raml
  standard-error-response: !include traits/errorResponse.raml

/capsules:
  get:
    is: [ common, standard-error-response ]
    (authRequired): false
    description: Get All Capsules details.
    responses:
      200:
        body:
          application/json:
            type: CapsulesAll[]
            example: !include examples/capsulesAll.json


prod-properties.yaml
dev-properties.yaml
test-properties.yaml
${env}-properties.yaml
