FROM openjdk:8-alpine
# The caseid service runs on port 8080 per default.
EXPOSE 9082
# Create a working directory for our caseid service to run in.
RUN mkdir -p /opt/ToDoQueryService
WORKDIR /opt/ToDoQueryService
# Copy the redistributable.
COPY target/ToDoQueryService-0.0.1-SNAPSHOT.jar /opt/ToDoQueryService
# Run the caseid jar. Tell it to use the kubernetes profile.
CMD ["java", "-Dspring.profiles.active=k8s", "-jar", "ToDoQueryService-0.0.1-SNAPSHOT.jar"]