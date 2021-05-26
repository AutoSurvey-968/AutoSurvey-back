# AutoSurvey-back

## A reactive Java back-end project for the automatic management of surveys. QC team members can upload past QC data (in CSV format) to the database, generate surveys for associates to take, and view analytics on the collected survey responses. Associates will be able to complete surveys and submit their responses to the database. This project was developed and deployed using a distributed architecture that includes the following microservices:  
* Gateway Service - Spring Cloud Gateway, Pipeline and Jenkins deployment
  - Discovery Service - Eureka integration
  - Config Service - 
* User Service - User authentication, Firebase Management, User Database
* Survey Service - Manages and stores survey information
* Submission Service - CSV and JSON (standard) response data management
* IO Service - Email management (sending survey links to batch members)
* Analytics Service - Aggregate and filtered data analytics

![image](https://user-images.githubusercontent.com/83471833/118834725-69841f80-b890-11eb-881d-5b5bf76ef454.png)



## Technologies Used

* Java - SE1.8
* Spring Boot Maven
  - Surefire plugin
* Spring Boot Starter - 2.4.5
  - Webflux
  - AOP
  - Web
  - Mail
  - Security
  - Actuator
  - Test
  - DevTools
* Spring Reactor
  - Test
* Spring Cloud
  - Gateway
  - Eureka
* Spring Boot Cassandra
* Firebase - 7.1.0
* Commons Validator - 1.4.1
* Commons Lang3 - 3.12.0
* Javax Mail - 1.6.2
* SpringFox Swagger - 2.9.2
* Docker
* SonarCloud
* Jacoco - 0.8.4
* Lombok
* Slf4J - 1.7.30
* Karate - 1.0.1


## Features

* QC team members can generate Surveys for associates to complete based on a previous format, or create a new survey format for special weeks.
* QC team members can email the survey link to all associates within the batch as part of the AutoSurvey service.
* QC team members can view reactively generated analytics for both aggregate and filtered datasets.
* Associates are able to anonymously submit their completed survey responses.
* Google Firebase, in conjunction with Spring Security, is used to verify user authentication for protected routes.

To-do list:
* Wow improvement to be done 1
* Wow improvement to be done 2

## Getting Started
   
`git clone https://github.com/AutoSurvey-968/AutoSurvey-back`  
* Set up an Amazon Web Services (AWS) IAM user with programmatic access and AmazonKeyspacesFullAccess policy attached. Then, generate security credentials for Amazon Keyspaces (for Apache Cassandra). SAVE THESE CREDENTIALS.  

## Usage

> Here, you instruct other people on how to use your project after they’ve installed it. This would also be a good place to include screenshots of your project in action.

## Contributors

* DevOps & Gateway Service Team
  - [Dakota Clark](https://github.com/DuskDaleSpider) - Primary
  - [Parker Loomis](https://github.com/ploomis1)
  - [Tyler Lopez](https://github.com/TylerRLopez)
* User Service Team
  - [Thomas An](https://github.com/artuis) - Primary
  - [Albert Magpoc](https://github.com/albert-magpoc-revature)
  - [Tony Touma](https://github.com/Chielo9513)
  - [Rashad Bowman](https://github.com/RashadCBowman)
* Survey Service Team
  - [Robert Bierly](https://github.com/rnbiv45) - Primary
  - [Benjamin Wood](https://github.com/lwood-benjamin)
  - [Arieh Gennello](https://github.com/MoldedPixels)
* Submission Service Team
  - [Matilda Kerwin](https://github.com/Kerwinm12345) - Primary
  - [Christopher Morrison](https://github.com/cmorrison-rev)
  - [Nerijus Gelezinis](https://github.com/NGelezinis)
  - [Robert Bierly](https://github.com/rnbiv45)
  - [Arieh Gennello](https://github.com/MoldedPixels)
* IO Service Team
  - [Richard Schaber](https://github.com/rjschaber)
* Analytics Service Team
  - [Austin Withers](https://github.com/AustinWithers) - Primary
  - [Kevin Rose](https://github.com/Kevinrose235)
  - [Michael Chan](https://github.com/chanmic)
* Quality Assurance Team
  - [Stephanie Tallman](https://github.com/sctallman) - Primary
  - [Benjamin Wood](https://github.com/lwood-benjamin)
  - [Tony Touma](https://github.com/Chielo9513)
* Front End Team
  - [Christopher Morrison](https://github.com/cmorrison-rev) - Primary
  - [Robert Bierly](https://github.com/rnbiv45)
  - [Richard Schaber](https://github.com/rjschaber)
  - [Kevin Rose](https://github.com/Kevinrose235)

## License

This is where I'd put my license... IF I HAD ONE!  
This project uses the following license: [<license_name>](<link>).
