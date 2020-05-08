from openjdk:8-jdk

COPY . /app/spring
WORKDIR /app/spring

EXPOSE 8080

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
