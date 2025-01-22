# Trello REST APIs Testing using Postman, Newman, and Jenkins CI/CD

This repository is specialaized in testing Trello REST APIs and makes sure that every function working correctly like creating, updating and retrieving full data of various items at Trello’s workspace with different Endpoints and Scenarios by using different HTTP methods. Putting all of these requests in one Postman collection. Ensure entering all required query parameters and path parameters according to Trello REST APIs documentations. Setting different environment variables at Scripts to make a dynamic and continuous comprehensive E2E testing. Using Post-response assertions to ensure the reliability and functionality of the APIs. Running this collection manually and automatically. 



 ## Tools : 
- Running API testing collections using **Postman**. 
- Running Automation API testing with command-line using **Newman**.
- Integrating API testing into CI/CD pipelines using **Jenkins**.

<a href="https://www.postman.com/"><img src="https://user-images.githubusercontent.com/25181517/192109061-e138ca71-337c-4019-8d42-4792fdaa7128.png" title="POSTMAN" alt="POSTMAN" width="30" height="30"/></a> ![Newman](https://img.shields.io/badge/Newman-Command_Line-brightgreen) <a href="https://www.jenkins.io"><img src="https://user-images.githubusercontent.com/25181517/179090274-733373ef-3b59-4f28-9ecb-244bea700932.png" title="Jenkins" alt="Jenkins" width="50" height="50"/></a>


## Preconditions
Before you start, Ensure you have met the following requirements:

- **Trello**:
  
1. Make sure that you have an existing Trello account.
  
2. You need to generate your API key via [Trello Power-Up Admin Portal](https://trello.com/power-ups/admin).
  
3. You nedd to generate your API Token.

- **Postman**:
  
   You need to have Postman installed or open it through out any browser.

- **Newman**:

  Make sure you have Node.js installed first, then run the following command to install Newman:

  ```bash
  npm install -g newman

- **Jenkins**:

  You need a Jenkins server set up for CI/CD integration. You can install Jenkins by following the instructions on the Jenkins website.

- **Clone this repository to your local machine**:

  ```bash
  git clone https://github.com/MuhammadMaged/Trello-APIs.git

## API requests
**The tests are organized into collections within Postman, each one focusing on specific API function:**

- **Post a Board** “this request verify creating a new Board”

- **Put a Board** “this request verify updating data at an existing Board”

- **Get a Board** “this request verify retrieving all data of an existing Board”

- **Post a List** “this request verify creating a new List on a Board”

- **Put a List** “this request verify updating data at an existing List”

- **Get a List** “this request verify retrieving all data of an existing List”

- **Post a Card** “this request verify creating a new Card on a List”

- **Put a Card** “this request verify updating data at an existing Card”

- **Get a Card** “this request verify retrieving all data of an existing Card”

- **Post a Checklist** “this request verify creating a new Checklist on a Card”

- **Put a Checklist** “this request verify updating data at an existing Checklist”

- **Get a Checklist** “this request verify retrieving all data of an existing Checklist”

- **Post an Item** “this request verify creating a new Item on a Checklist”

- **Put an Item** “this request verify updating data at an existing Item”

- **Get an Item** “this request verify retrieving all data of an existing Item”

- **Delete an Item** “this request verify deleting an existing Item”

- **Delete a Checklist** “this request verify deleting an existing Checklist”

- **Delete a Card** “this request verify deleting an existing Card”

- **Delete a Board** “this request verify deleting an existing Board”



## Running Steps

**Running Tests in Postman**
- Open Postman.
- Import the Postman Collection.json file.
- Import Environment.json file and set it as the current environment or create your own environment file.
- Enter your own API Key as an environment variable.
- Enter your own API Token as an environment variable.
- Run the API tests using Postman's collection runner.

**Automation running Tests via Command Line using Newman**

 You can also run the tests automatically via the command line using Newman.
- Export Collection & Environment json files from Postman. 
- Use the following command to run a specific test suite and environment:
  
   ```bash
   newman run Collection.json -e Environment.json 

**Generating HTML Reports**

Newman supports generating reports like extrahtml which appears a dashboard with details about your API test run, passed and failed assertions.

- To generate HTML reports, simply add -r htmlextra option after Newman running command, as shown below:

    ```bash
    newman run Collection.json -e Environment.json -r htmlextra

- After that the HTML report will be generated in the directory of this repository


**Jenkins CI/CD**

The repository is configured to automate the API testing process using Jenkins for CI/CD. Jenkins pipelines are set up to trigger API tests when changes are pushed to the repository. Jenkins will run the tests, generate HTML reports, and provide feedback on the test results.


## Contact

If you have any questions, suggestions, or issues related to this project, please feel free to contact me.
- **Email**: [Mohamedmag158@gmail.com](Mohamedmag158@gmail.com)

I appreciate your interest and support..
