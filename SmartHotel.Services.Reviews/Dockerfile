FROM openjdk:8-jre AS base
WORKDIR /app

ENV sql_server_url=jdbc:postgresql://reviews-data:5432/reviewsdb
ENV sql_user_name=admin
ENV sql_user_password=Passw0rd!
ENV APPLICATION_INSIGHTS_IKEY=19cf42a1-9fa1-45dc-bd89-2f41c862ff6e
ENV PATH_BASE=/

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
COPY --from=build /target/reviews-0.0.1-SNAPSHOT.jar .
EXPOSE 8080
ENTRYPOINT exec java -Djava.security.egd=file:/dev/./urandom -jar /app/reviews-0.0.1-SNAPSHOT.jar
