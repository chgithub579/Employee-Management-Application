# ---- Build Stage ----
FROM maven:3.9.6-eclipse-temurin-17 AS build
WORKDIR /app

# Copy only pom.xml first to download dependencies
COPY pom.xml ./
RUN mvn dependency:go-offline

# Copy the rest of the backend project
COPY . ./

# Build the Spring Boot application (skip tests to speed up build)
RUN mvn clean package -DskipTests

# ---- Run Stage ----
FROM eclipse-temurin:17-jdk-alpine
WORKDIR /app

# Copy the jar built in the previous stage
COPY --from=build /app/target/*.jar app.jar

# Expose backend port (make sure it matches your application.properties server.port)
EXPOSE 8080

# Run the Spring Boot app
ENTRYPOINT ["java", "-jar", "app.jar"]
