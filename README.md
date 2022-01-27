# Revature Courseware Cornucopia

Revature Courseware Cornucopia is an Angular Single Page Application that will allow users to sign up and login as a customer, browse all available products, view an individual product, and add products to their cart for purchase. As soon as a user logs in, a user will also be able to see which products are on sale as well as select a quantity amount of a specific product. Behavioral driven development will be utilized as well as a minimum code coverage goal of 80%.

# Features
- Login
- Register
- Main Page that shows all products
- Search for Products
- Product Page
- Cart
- Quantity Select
- Checkout
- View transaction
- Sales/Deals
- Dark Mode

# Technologies Used
- Java 8
- Spring Data
- Spring Boot
- Spring MVC
- AWS RDS
- Angular
- TypeScript
- AWS S3
- AWS EC2
- Selenium
- JUnit/Mockito
- Cucumber/Gherkin
- Jenkins
- Sonar

You are responsible for detailing the README.md with general application information, prerequisites/additional software needed to get started, Environment Variables needed to be set, etc

# Get Started
- Set environment variables listed below

- Clone the repositories linked below

`git clone https://github.com/revature-RCC/project3-frontend`

`git clone https://github.com/revature-RCC/project3-backend`

`git clone https://github.com/revature-RCC/project3-e2e`

- Use Maven to install dependencies on the backend
- Compile and run the backend

- Install NPM packages for the frontend (in project2-frontend/)

`npm install`

- Run the Angular server (in project3-frontend/)

`ng serve`

- Access the frontend from http://localhost:4200 in your browser

# Environment Variables
Environment Variables:

SPRING_DATABASE_URL
`jdbc:h2:./h2/db`

SPRING_DATABASE_USERNAME
`sa`

SPRING_DATABASE_PASSWORD
`sa`

SPRING_DATABASE_DRIVER
`org.h2.Driver`

SPRING_DATABASE_PLATFORM
`org.hibernate.dialect.H2Dialect`

SPRING_DATABASE_DDL_METHOD
`create`

DRIVER
`webdriver.chrome.driver`

DRIVER_LOCATION
`<path to your chromedriver, example: C:\Program Files\chromedriver\chromedriver.exe>`

AWS_PASS
`<your AWS S3 Access Key>`

AWS_SECRET_PASS
`<your AWS S3 Secret Key>`

# Repositories
project3-frontend https://github.com/revature-RCC/project3-frontend

project3-backend https://github.com/revature-RCC/project3-backend

project3-e2e https://github.com/revature-RCC/project3-e2e
