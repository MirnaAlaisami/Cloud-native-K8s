FROM openjdk:8-alpine
# The caseid service runs on port 8080 per default.
EXPOSE 9080
# Create a working directory for our caseid service to run in.
RUN mkdir -p /opt/ToDoUIService
WORKDIR /opt/ToDoUIService
# Copy the redistributable.
COPY target/ToDoUI-0.0.1-SNAPSHOT.jar /opt/ToDoUIService
# Run the caseid jar. Tell it to use the kubernetes profile.
CMD ["java", "-Dspring.profiles.active=k8s", "-jar", "ToDoUI-0.0.1-SNAPSHOT.jar"]