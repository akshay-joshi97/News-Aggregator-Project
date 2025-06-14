# Use an OpenJDK base image
FROM openjdk:17-jdk-slim

# Set working directory
WORKDIR /app

# Copy the JAR file to the container
COPY NewsAggregator2-1.0-SNAPSHOT.jar app.jar

# Expose port (change to your app's port if needed)
EXPOSE 8080

# Run the JAR
CMD ["java", "-jar", "app.jar"]
