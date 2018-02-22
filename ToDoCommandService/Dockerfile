FROM openjdk:8-alpine
# The caseid service runs on port 8080 per default.
EXPOSE 9084
# Create a working directory for our caseid service to run in.
RUN mkdir -p /opt/ToDoCommandService
WORKDIR /opt/ToDoCommandService
# Copy the redistributable.
COPY target/ToDoCommandService-0.0.1-SNAPSHOT.jar /opt/ToDoCommandService
# Run the caseid jar. Tell it to use the kubernetes profile.
CMD ["java", "-Dspring.profiles.active=k8s", "-jar", "ToDoCommandService-0.0.1-SNAPSHOT.jar"]