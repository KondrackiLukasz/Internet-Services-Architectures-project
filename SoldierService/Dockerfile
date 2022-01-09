FROM maven:3.8.4-openjdk-17 AS build
WORKDIR /app
COPY /src src
COPY pom.xml .
RUN mvn clean package

FROM gcr.io/distroless/java17-debian11
COPY --from=build /app/target/SoldierService-1.0.0.jar SoldierService-1.0.0.jar
# ENTRYPOINT ["java","-jar","/SoldierService-1.0.0.jar"]
CMD ["/SoldierService-1.0.0.jar"]
