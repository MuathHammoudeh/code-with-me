

# RUN --mount=type=cache,target=/root/.m2 \
#     mvn dependency:go-offline -B

# COPY ./login /app

# RUN mvn clean package -DskipTests

# RUN apt-get update && apt-get install -y maven && rm -rf /var/lib/apt/lists/*
ARG IMAGE_TAG=24-ea-21-slim
FROM openjdk:${IMAGE_TAG}

EXPOSE 8080

WORKDIR /app
COPY ./login/pom.xml ./pom.xml
COPY ./login/target/*.jar ./application.jar





ENTRYPOINT ["java", "-jar", "application.jar"]
