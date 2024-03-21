# We need JAVA 8
FROM amazoncorretto:8

EXPOSE 8080

WORKDIR /usr/src/app

# Copy all of the source code
COPY . .

# Building the project
RUN ./mvnw package

# And finally the command to run the application
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]