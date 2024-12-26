# Use a minimal base image
FROM openjdk:17-jdk-alpine

# Add a non-root user
RUN addgroup --system appgroup && adduser --system appuser --ingroup appgroup

# Add metadata
LABEL maintainer="spring_ui"

# Set a working directory
WORKDIR /app

# Copy the JAR file into the container
COPY --chown=appuser:appgroup target/nagarro-0.0.1-SNAPSHOT.jar app.jar

# Switch to non-root user
USER appuser

# Expose the application port
EXPOSE 8484

# Define the entry point
ENTRYPOINT ["java", "-jar", "/app/app.jar"]