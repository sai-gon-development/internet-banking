# Eureka Server

## Maven
### Build
mvn clean install
### Run
cd target
java -jar internet-banking-discovery-service-1.0.0.jar
java -jar internet-banking-discovery-service-1.0.0.jar --spring.profiles.active=localhost
java -jar internet-banking-discovery-service-1.0.0.jar --spring.profiles.active=development
java -jar internet-banking-discovery-service-1.0.0.jar --spring.profiles.active=production

## Docker
### Build
docker build -t internet-banking-discovery-service:1.0.0 -f Dockerfile .

### Run
docker run -it --name internet-banking-discovery-service -p 8020:8060 -e SPRING_PROFILES_ACTIVE=localhost internet-banking-discovery-service:1.0.0

#### SPRING_PROFILES_ACTIVE (env)
localhost, development, production