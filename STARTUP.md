# Revature Courseware Cornucopia

# Software
- JDK 8
- Maven 3.8.4 or above
- NodeJS 16.13.1 or above
- NPM 8.3.0 or above
- Angular CLI 13.1.1 or above
- chromedriver (your browser version)
- Sonar (requires JDK 11 for Maven CLI command)
- IntelliJ IDE Community

# IntelliJ Plugins
- Cucumber for Java 212.4746.52
- Gherkin 212.5457.62

# Ports
- Frontend: 4200
- Backend: 81

# Maven Dependencies
Backend
- spring-boot-starter-data-jpa
- spring-boot-starter-web
- h2
- postgresql
- lombok
- spring-boot-starter-test
- log4j
- spring-security-crypto
- aws-java-sdk-s3
- mockito-inline
- spring-boot-maven-plugin
- lombok
- jacoco-maven-plugin

End-to-end Testing
- selenium-java
- cucumber-java
- cucumber-junit
- cucumber-gherkin
- junit-jupiter

# NPM Dependencies
- The default dependencies from the Angular CLI

# Get Started
- Set up AWS S3 bucket and get access key and secret key (for admin page file upload)
https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-walkthroughs-managing-access-example1.html

- Set environment variables listed below

- Clone the repositories linked below

`git clone https://github.com/revature-RCC/project3-frontend`

`git clone https://github.com/revature-RCC/project3-backend`

`git clone https://github.com/revature-RCC/project3-e2e`

- Use Maven to install dependencies on the backend (use IDE)

- Install NPM packages for the frontend (in project3-frontend/)

`npm install`

- Run the Angular server (in project3-frontend/)

`ng serve`

- Access the website from http://localhost:4200 in your browser

# Environment Variables

SPRING_DATABASE_URL `jdbc:h2:./h2/db`

SPRING_DATABASE_USERNAME `sa`

SPRING_DATABASE_PASSWORD `sa`

SPRING_DATABASE_DRIVER `org.h2.Driver`

SPRING_DATABASE_PLATFORM `org.hibernate.dialect.H2Dialect`

SPRING_DATABASE_DDL_METHOD `create`

DRIVER `webdriver.chrome.driver`

DRIVER_LOCATION `<path to your chromedriver, example: C:\Program Files\chromedriver\chromedriver.exe>`

AWS_PASS `<your AWS S3 Access Key>`

AWS_SECRET_PASS `<your AWS S3 Secret Key>`

SONAR_TOKEN `<your Sonar Token (not required to run the project)>`

# Testing
Testing documentation is included in this repository

# Deployment
- env variables
- how to deploy

# Repositories
project3-frontend https://github.com/revature-RCC/project3-frontend

project3-backend https://github.com/revature-RCC/project3-backend

project3-e2e https://github.com/revature-RCC/project3-e2e
