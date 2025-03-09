FROM maven:3.8.6-openjdk-11 AS build
WORKDIR /app
COPY . .
RUN mvn clean install -DskipTests

FROM openjdk:11.0.10-jre
WORKDIR /app
COPY --from=build /app/target/zuul-0.0.1-SNAPSHOT.jar /app/zuul-0.0.1-SNAPSHOT.jar
EXPOSE 9999
CMD [ "java", "-jar", "/app/zuul-0.0.1-SNAPSHOT.jar"]