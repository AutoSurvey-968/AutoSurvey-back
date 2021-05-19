# AutoSurvey-back

## A reactive Java back-end project for the automatic management of surveys. QC team members can upload past QC data (in CSV format) to the database, generate surveys for associates to take, and view analytics on the collected survey responses. Associates will be able to complete surveys and submit their responses to the database. This project is developed and deployed as a series of microservices:  
* Gateway Service - Spring Cloud Gateway, Pipeline and Jenkins deployment
* User Service - User authentication, Firebase Management, User Database
* Survey Service - Manages and stores survey information
* Submission Service - CSV and JSON (standard) response data management
* IO Service - Email management
* Analytics Service - Aggregate and filtered data analytics

![image](https://user-images.githubusercontent.com/83471833/118834725-69841f80-b890-11eb-881d-5b5bf76ef454.png)



## Technologies Used

* Java - SE1.8
* Spring Boot Maven
* Spring Boot Starter - 2.4.5
  - Webflux
  - AOP
  - Test
  - Security
* SonarCloud
* Lombok
* Slf4J - 1.7.30
* Spring Boot Cassandra
* 


## Features

List of features ready and TODOs for future development
* Awesome feature 1
* Awesome feature 2
* Awesome feature 3

To-do list:
* Wow improvement to be done 1
* Wow improvement to be done 2

## Getting Started
   
`git clone https://github.com/AutoSurvey-968/AutoSurvey-back`  
(include all environment setup steps)

> Be sure to include BOTH Windows and Unix command  
> Be sure to mention if the commands only work on a specific platform (eg. AWS, GCP)

- All the `code` required to get started
- Images of what it should look like

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
* IO Service Team
  - [Austin Withers](https://github.com/AustinWithers) - Primary
  - [Richard Schaber](https://github.com/rjschaber)
* Analytics Service Team
  - [Austin Withers](https://github.com/AustinWithers) - Primary
  - [Kevin Rose](https://github.com/Kevinrose235)
  - [Michael Chan](https://github.com/chanmic)
* Quality Assurance Team
  - [Stephanie Tallman](https://github.com/sctallman) - Primary
  - [Benjamin Wood](https://github.com/lwood-benjamin)
  - [Tony Touma](https://github.com/Chielo9513)

## License

This is where I'd put my license... IF I HAD ONE!  
This project uses the following license: [<license_name>](<link>).
