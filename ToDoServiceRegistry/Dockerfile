FROM openjdk:8-alpine
# The caseid service runs on port 8080 per default.
EXPOSE 8761
# Create a working directory for our caseid service to run in.
RUN mkdir -p /opt/todoserviceregistry
WORKDIR /opt/todoserviceregistry
# Copy the redistributable.
COPY target/todoserviceregistry-0.0.1-SNAPSHOT.jar /opt/todoserviceregistry
# Run the caseid jar. Tell it to use the kubernetes profile.
CMD ["java", "-Dspring.profiles.active=k8s", "-jar", "todoserviceregistry-0.0.1-SNAPSHOT.jar"]