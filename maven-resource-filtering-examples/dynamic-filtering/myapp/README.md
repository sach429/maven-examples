# dynamic-filtering

Here a file called application.properties is located under src/main/resources has a placeholder for server.port. The actual value is present in dev.properties and prod.properties which gets substituted

While running maven for example mvn clean package we may dynamically choose whether the value gets picked from dev or prod.properties by one of the following ways

1. Set environment variable "env" as "dev" or "prod" eg. export env=dev
2. Pass system property "env" as "prod" or "dev" eg. mvn clean package -Denv=prod

This way we can have multiple property files defined for each env with the real values for eg. sit.properties, uat.properties etc. and pass the env value as shown above to ensure the final artifact has the correct configuration
