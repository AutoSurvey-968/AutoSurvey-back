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

*[Lombok Download](https://search.maven.org/search?q=g:org.projectlombok%20AND%20a:lombok&core=gav)
*[Lombok Setup Guide for Eclipse and Intellij](https://www.baeldung.com/lombok-ide)

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
* [Config Service](https://github.com/AutoSurvey/AutoSurvey-Config-Service/blob/main/README.md)
* [User Service](https://github.com/AutoSurvey/AutoSurvey-User-Service/blob/main/README.md)
* [Survey Service](https://github.com/AutoSurvey/AutoSurvey-Survey-Service/blob/main/README.md)
* [Submission Service](https://github.com/AutoSurvey/AutoSurvey-Submission-Service/blob/main/README.md)
* [Analytics Service](https://github.com/AutoSurvey/AutoSurvey-Analytics-Service/blob/main/README.md)
* [IO Service](https://github.com/AutoSurvey/AutoSurvey-IO-Service/blob/main/README.md)

## Docker
(add later) :)
