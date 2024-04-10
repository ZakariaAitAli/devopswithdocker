# Use Amazon Corretto 8 as base image
FROM amazoncorretto:8

# Set the working directory in the container
WORKDIR /app

# Copy the Java Spring project files to the container
COPY . /app

# Install Maven
RUN yum install -y maven

# Build the Spring project with Maven
RUN ./mvnw package

# Expose the port the Spring application runs on
EXPOSE 8080

# Command to run the Spring application
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
