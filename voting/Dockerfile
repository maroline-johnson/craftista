FROM openjdk:19-jdk-slim
WORKDIR /app
COPY pom.xml ./
COPY src ./src
RUN apt-get update && apt-get install --no-install-recommends -y maven=3.9.9 \
    && mvn package -DskipTests \
    && mv target/*.jar app.jar \
    && apt-get remove -y maven \
    && apt-get autoremove -y \
    && rm -rf /var/lib/apt/lists/*

EXPOSE 8080
CMD ["java", "-jar", "app.jar"]