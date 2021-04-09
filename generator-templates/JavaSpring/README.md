JavaSpring
==========

## Overview
This directory collects template sets for Java Spring that are initiated with the generator option "-g spring".

### Example:
```
openapi-generator generate \
	-i openapi.yaml \
	-o ./generated \
	-g spring \
    -t openapi-generator-templates/generator-templates/JavaSpring/TEMPLATE_SET
    [--skip-validate-spec]
```

## Current Java Spring Template Sets
* [Spring Boot with Lombok and Actuator](./spring-boot-lombok-actuator/readme.md)
* [Spring Boot Java 11](./java11/readme.md)