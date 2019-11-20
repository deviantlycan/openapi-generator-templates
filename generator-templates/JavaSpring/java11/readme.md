Spring Boot Java 11
=======================================

## Overview
This template set allows for generating a Spring Boot Java 11 service.
If java11 is used, updated dependencies are used in the generated POM file.

| Name                         | Version       | 
|------------------------------|---------------|
| Spring                       | 2.2.1.RELEASE | 
| Springfox                    | 2.9.2         | 
| jaxb api                     | 2.3.1         |
| Webjars swagger-ui           | 3.24.3        | 
| swagger-annotations          | 2.0.10        |
| jackson-datatype-threetenbp  | 2.10.0        |
| jackson-databind-nullable    | 0.2.0         |
| virtualan-plugin             | 1.2.6         | 
| hsqldb                       | 2.5.0         |

This template set is based on the [Spring Boot - Lombok and Actuator](../spring-boot-lombok-actuator/readme.md)
template set and includes all features of that template set.

## Additional Properties
This template set includes all additional properties in the [Spring Boot - Lombok and Actuator](../spring-boot-lombok-actuator/readme.md)
template set, but also adds the additional properties in this table

| Name         | Data Type | Description                                |
|--------------|-----------|--------------------------------------------|
| java11       | Boolean   | Enables Java 11 and updated dependencies   |

> Note that this currently requires the regular java8 option to be set to true.
> It may work fine without it, but it has not been tested.

## Use

### Build the code
```
openapi-generator generate \
-i openapi.yaml \
-o ./generated \
-g spring \
-t generator-templates/JavaSpring/java11 \
-p useActuator=true,useLombok=true,actuatorPath=/actuator,java8=true,java11=true
```

### Run the application
```
cd generated
mvn spring-boot:run
```
