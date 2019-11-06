FROM maven:3.5-jdk-8 AS build
COPY src /usr/shob/src
COPY pom.xml /usr/shob
RUN mvn -f /usr/shob/pom.xml clean package
EXPOSE 8080
ENTRYPOINT ["java","-Dspring.data.mongodb.uri=mongodb://mongo:27017/glarimy","-jar","/usr/shob/target/glarimy-quiz-employee-service.jar"]