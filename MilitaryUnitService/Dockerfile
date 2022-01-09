FROM maven:3.8.4-openjdk-17 AS build
WORKDIR /app
COPY /src src
COPY pom.xml .
RUN mvn clean package  -D maven.test.skip

FROM gcr.io/distroless/java17-debian11
COPY --from=build /app/target/MilitaryUnitService-1.0.0.jar military-unit-service-1.0.0.jar
CMD ["/military-unit-service-1.0.0.jar"]

