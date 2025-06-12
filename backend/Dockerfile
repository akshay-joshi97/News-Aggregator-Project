# Use a base image with Java
FROM openjdk:17-jdk-slim

# Set working directory
WORKDIR /app

# Copy the shaded JAR
COPY target/NewsAggregator2-1.0-SNAPSHOT.jar app.jar

# Expose the port your app uses (change if different)
EXPOSE 4567

# Run the app
CMD ["java", "-jar", "app.jar"]
