FROM maven:3.8.5-eclipse-temurin-11-alpine
COPY . .
RUN mvn clean -DskipTests=true install

COPY target/*.jar application/application.jar

EXPOSE 8020
ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-Dspring.profiles.active=${SPRING_PROFILES_ACTIVE}","-jar","/application/application.jar"]