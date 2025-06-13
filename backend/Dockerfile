# ---------- Stage 1: Build with Maven ----------
FROM maven:3.9.6-eclipse-temurin-17 AS build
WORKDIR /app

# Copy the Maven project files
COPY . .

# Build the project and skip tests
RUN mvn clean package -DskipTests


# ---------- Stage 2: Run the JAR with OpenJDK ----------
FROM openjdk:17-jdk-slim
WORKDIR /app

# Copy the built JAR from the previous stage
COPY --from=build /app/target/NewsAggregator2-1.0-SNAPSHOT.jar app.jar

# Expose the port used by Spark (default: 4567)
EXPOSE 4567

# Run the JAR
CMD ["java", "-jar", "app.jar"]
