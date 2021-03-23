# muni-pa160-chat-service
Example of a web service with OpenAPI description

Prerequisites: <a href="https://maven.apache.org/">Apache Maven</a> and JDK 11+ 

Download and compile:
```bash
git clone https://github.com/martin-kuba/muni-pa160-chat-service.git
cd muni-pa160-chat-service
mvn spring-boot:run
```
Alternatively, you can create an executable JAR file and execute it:
```bash
mvn clean install
java -jar target/pa160_chat_service.jar
```
Then visit the service with your browser: http://localhost:8080/
