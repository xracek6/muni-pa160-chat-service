![](workflows/test%20build/badge.svg)

# muni-pa160-chat-service
Example of a web service with OpenAPI description in [openapi.yml](src/main/resources/static/openapi.yml)

Prerequisites: git, [Apache Maven](https://maven.apache.org/) and JDK 11+ 

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

## Running with TLS

Create a PKCS12 keystore with:
```bash
openssl pkcs12 -export -name "mycert" -inkey key.pem -in cert.pem -certfile chain.pem -out mykeystore.p12
```
then run with the following options:
```bash
java -jar target/pa160_chat_service.jar \
     --server.port=8443 \
     --server.ssl.key-store-type=pkcs12 \
     --server.ssl.key-store=mykeystore.p12 \
     --server.ssl.key-store-password=password
```
