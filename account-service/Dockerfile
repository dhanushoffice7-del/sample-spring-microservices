FROM amazoncorretto:21
LABEL maintainer="piotrminkowski@gmail.com"
RUN addgroup -S spring && adduser -S spring -G spring
USER spring:spring
COPY target/account-service.jar account-service.jar
EXPOSE 2222
ENTRYPOINT ["java", "-jar", "/account-service.jar"]
