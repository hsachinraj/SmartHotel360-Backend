FROM openjdk:8-jre AS base
WORKDIR /app

FROM openjdk:8-jdk AS maven
WORKDIR ./
COPY . .
RUN chmod +x ./mvnw
RUN sed -i 's/\r$//' mvnw
RUN ./mvnw install

FROM maven as build
WORKDIR ./
RUN ./mvnw package

FROM base as final
WORKDIR /app
COPY --from=build /src/target/reviews-0.0.1-SNAPSHOT.jar .
EXPOSE 8080
ENTRYPOINT exec java -Djava.security.egd=file:/dev/./urandom -jar /app/reviews-0.0.1-SNAPSHOT.jar
