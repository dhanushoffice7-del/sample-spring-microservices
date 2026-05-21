# 1. Use a modern, actively maintained base image (Eclipse Temurin is the industry standard)
FROM eclipse-temurin:21-jre-alpine

# 2. Use LABEL instead of the deprecated MAINTAINER keyword
LABEL maintainer="piotrminkowski@gmail.com"

# 3. Create a non-root system user for security
RUN addgroup -S spring && adduser -S spring -G spring
USER spring:spring

# 4. Use COPY instead of ADD for local file transfers
COPY target/account-service.jar account-service.jar

# 5. Expose the application port
EXPOSE 2222

# 6. Execute the application
ENTRYPOINT ["java", "-jar", "/account-service.jar"]
