# Use a specific version of Java
FROM adoptopenjdk/openjdk11:alpine-jre

# Set the working directory in the container
WORKDIR /opt/google/app

# Copy the JAR file from the build context to the working directory
COPY target/spring-boot-web.jar app.jar

# This should not be changed
ENTRYPOINT ["java", "-jar", "app.jar"]
