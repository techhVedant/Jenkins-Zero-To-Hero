#Use OpenJDK 17 JDK (Official Alpine image)
FROM openjdk:17-jdk-alpine

# Define JAVA_HOME explicitly
ENV JAVA_HOME=/opt/java/openjdk
ENV PATH="${JAVA_HOME}/bin:${PATH}"

# Artifact path
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

COPY ${artifact} app.jar

# Start the application
ENTRYPOINT ["java", "-jar", "app.jar"]
