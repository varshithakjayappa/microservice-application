FROM  maven:3.8.6-openjdk-11 AS build
WORKDIR /app
COPY . .
RUN mvn clean install -DskipTests

FROM openjdk:11.0.10-jre
WORKDIR /app
COPY --from=build /app/target/shoes-0.0.1-SNAPSHOT.jar /app/shoes-0.0.1-SNAPSHOT.jar
EXPOSE 1002
CMD [ "java" , "jar" ,"shoes-0.0.1-SNAPSHOT.jar" ]