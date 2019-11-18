Spring Boot with Lombok and Actuator
=======================================

These templates allow for use of Lombok in generated models and Actuator 
Health and Info endpoint inclusion.

This template set relies on the additional properties

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
	-t openapi-generator-templates/generator-templates/JavaSpring/spring-boot-lombok-actuator \
	-p useActuator=true,useLombok=true,actuatorPath=/actuator
```

