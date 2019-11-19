Spring Boot with Lombok and Actuator
=======================================

## Overview
This template set allow for use of Lombok in generated models and Actuator 
Health and Info endpoint inclusion.  They are not enabled by default, but 
are enabled with "additional-properties"

## Additional Properties
This template set relies on the additional properties listed in this table

| Name         | Data Type | Description                                |
|--------------|-----------|--------------------------------------------|
| useLombok    | Boolean   | Enables Lombok for models                  |
| useActuator  | Boolean   | Enables Actuator Health and Info           |
| actuatorPath | String    | Sets path for Actuator (default: basePath) |

## Use
```
openapi-generator generate \
-i openapi.yaml \
-o ./generated \
-g spring \
-t ../openapi-generator-templates/generator-templates/JavaSpring/spring-boot-lombok-actuator \
-p useActuator=true,useLombok=true,actuatorPath=/actuator
```

## Other files
* The openapi.yaml file in this directory defines an example service that only exposes the actuator endpoints.
* The .openapi-generator-ignore in this directory can be used to NOT generate models and controllers for the actuator endpoints.

## Notes
The default basePath for the actuatorPath property is the basepath that is 
defined in the OpenApi spec, not the literal word "basepath"

The Actuator Info endpoint is configured in the application.properties file to
automatically use data from the info section of the OpenApi spec to return a response 
like

```
{
  "title": "Echo",
  "description": "This is an echo service",
  "version": "1.0.0",
  "termsOfService": "https://api.antbytes.com/echo/files/tos.html",
  "contact": {
    "name": "Deviant Lycan",
    "email": "deviantlycan@antbytes.com",
    "url": "https://antbytes.com/devs/deviantlycan"
  }
}
```


