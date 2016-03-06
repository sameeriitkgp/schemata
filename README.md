# README
This repository will contain all JSON reference schemata for the Green Navigation project

## Schemata

Are discussed in detail [here](https://github.com/Greennav/schemata/blob/master/SCHEMATA.md)

## Validation

Since GreenNavigation uses TDD, all responses must be testable. This can be ensured using one of the various schema validating libraries like [this one](https://github.com/xeipuuv/gojsonschema) written in Go.https://github.com/xeipuuv/gojsonschema

## Example

There is an JSON Schema Generator [here](http://jsonschema.net/index.html#/).

As an example, we will take the mockup response from the routing service [see here](https://raw.githubusercontent.com/Greennav/service-routing/master/mockup-response.json):

```JSON
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "id": "https://raw.githubusercontent.com/Greennav/service-routing/master/mockup-response.json",
  "type": "object",
  "properties": {
    "address": {
      "id": "https://raw.githubusercontent.com/Greennav/service-routing/master/mockup-response.json/address",
      "type": "object",
      "properties": {
        "streetAddress": {
          "id": "https://raw.githubusercontent.com/Greennav/service-routing/master/mockup-response.json/address/streetAddress",
          "type": "string"
        },
        "city": {
          "id": "https://raw.githubusercontent.com/Greennav/service-routing/master/mockup-response.json/address/city",
          "type": "string"
        }
      },
      "required": [
        "streetAddress",
        "city"
      ]
    },
    "phoneNumber": {
      "id": "https://raw.githubusercontent.com/Greennav/service-routing/master/mockup-response.json/phoneNumber",
      "type": "array",
      "items": {
        "id": "https://raw.githubusercontent.com/Greennav/service-routing/master/mockup-response.json/phoneNumber/0",
        "type": "object",
        "properties": {
          "location": {
            "id": "https://raw.githubusercontent.com/Greennav/service-routing/master/mockup-response.json/phoneNumber/0/location",
            "type": "string"
          },
          "code": {
            "id": "https://raw.githubusercontent.com/Greennav/service-routing/master/mockup-response.json/phoneNumber/0/code",
            "type": "integer"
          }
        }
      }
    }
  },
  "required": [
    "address",
    "phoneNumber"
  ]
}
```
