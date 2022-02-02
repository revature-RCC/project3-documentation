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

# Testing
Testing documentation is included in this repository

# Deployment
- Set up AWS EC2 and RDS
- Set your environment variables listed below (production)
- Install Jenkins on EC2
- Set up Jenkins to install Maven and NodeJS (in Jenkins configuration, we used a plugin for NodeJS)
- Set up Maven to use Java 11 (for Sonar)
- Create Jenkins job
- Set up the Jenkins job to use your backend Git repository (in the General, Source Code Management, and Build Triggers (only for webhook) sections)
- Set up GitHub webhook for Jenkins (not required)
- Set up Jenkins job build step that builds the backend with Maven, runs a Sonar analysis, and runs the jar in the background

Example Jenkins job build step (shell script):
```
mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar "-Dsonar.projectKey=revature-RCC_project3-backend"

export BUILD_ID=dontKillMe
JENKINS_NODE_COOKIE=dontKillMe sudo -E nohup java -jar target/project3-backend-0.0.1-SNAPSHOT.jar &
```

# Environment Variables

## Developoment
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

PROJECT3_FRONTEND_URL `http://localhost:4200/`

## Production

SPRING_DATABASE_URL `jdbc:postgresql://<your AWS RDS url>/<your AWS RDS database name>`

SPRING_DATABASE_USERNAME `<your AWS RDS username>`

SPRING_DATABASE_PASSWORD `<your AWS RDS password>`

SPRING_DATABASE_DRIVER `<your database driver class, we used org.postgresql.Driver>`

SPRING_DATABASE_PLATFORM `<your database platform class, we used org.hibernate.dialect.PostgreSQL9Dialect>`

SPRING_DATABASE_DDL_METHOD `update`

PROJECT3_FRONTEND_URL `<your frontend url and port>`

# Repositories
project3-frontend https://github.com/revature-RCC/project3-frontend

project3-backend https://github.com/revature-RCC/project3-backend

project3-e2e https://github.com/revature-RCC/project3-e2e
