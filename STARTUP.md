# Backend Startup

## Credentials Needed
* Firebase Credentials
    * route to the JSON file
    * URL to Firebase user
    * Key provided from AWS
* AWS Cassandra Credentials
    * Username
    * Password
* Truststore key password
* SQS Credentials
    * SQS password
    * SQS queue names
    * SQS username

## Lombok
Lombok is a library that automatically generates getters, setters, toStrings, hashcodes, and more. Although the dependency is in the pom, developers must also download lombok themselves for the code to work.
* [Lombok Download](https://search.maven.org/search?q=g:org.projectlombok%20AND%20a:lombok&core=gav)
* [Lombok Setup Guide for Eclipse and Intellij](https://www.baeldung.com/lombok-ide)

## BASH Terminal TrustStore (these commands will not work in powershell)
1. Open a BASH terminal inside of src/main/resources folder.
2. `curl https://certs.secureserver.net/repository/sf-class2-root.crt -O`
3. `openssl x509 -outform der -in sf-class2-root.crt -out temp_file.der`
4. `keytool -import -alias cassandra -keystore cassandra_truststore.jks -file temp_file.der`
5. Enter a password when prompted. Save this password!
6. Say yes when prompted

## Services
* [Gateway Service](https://github.com/AutoSurvey/AutoSurvey-Gateway-Service/blob/main/README.md)
* [Discovery Service](https://github.com/AutoSurvey/AutoSurvey-Discovery-Service/blob/main/README.md)
* [Config Service](https://github.com/AutoSurvey/AutoSurvey-Config-Serivce/blob/main/README.md)
* [User Service](https://github.com/AutoSurvey/AutoSurvey-User-Service/blob/main/README.md)
* [Survey Service](https://github.com/AutoSurvey/AutoSurvey-Survey-Service/blob/main/README.md)
* [Submission Service](https://github.com/AutoSurvey/AutoSurvey-Submission-Service/blob/main/README.md)
* [Analytics Service](https://github.com/AutoSurvey/AutoSurvey-Analytics-Service/blob/main/README.md)
* [IO Service](https://github.com/AutoSurvey/AutoSurvey-IO-Service/blob/main/README.md)

## Docker
1. Make sure all environmental variables for each service is set, along with two others: `TRUSTSTORE_ENCODED` and `CREDENTIALS_JSON_ENCODED`.
   1. These variables' values need to be the cassandra truststore and the firebase credentials encoded by base64 respectively.
   2. To get these values, open the BASH terminal and use this command: `base 64 {file_name}` to get each encoded value.
      * EX: For the truststore: `base 64 cassandra_truststore.jsk`.
2. The `EUREKA_URL` value should also be set to `http://discovery-service:8761/eureka`.
3. Build the docker images using `docker build -t autosurvey/{service_name}-service .`.
   * EX: For the user service: `docker build -t autosurvey/user-service .`.
4. Then, to create and run the container, use the command `docker/run-docker.sh` in the root of the repository.
5. Repeat for each service until they are all running on docker. Once all of them are up, the project can be accessed with `http://localhost:80` if running locally.
