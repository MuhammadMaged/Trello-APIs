# Trello APIS Testing with Postman, Newman, and Jenkins CI/CD

This repository is dedicated to automating the testing of Trello APIs using a comprehensive toolkit that includes Postman collections, Newman for command-line execution, and Jenkins for continuous integration and continuous delivery (CI/CD) automation. The Trello API serves as a sample platform for testing and learning, and the test modules are designed to cover a wide range of endpoints and scenarios to ensure the reliability and functionality of the API.

## Table of Contents
- [Technologies Used](#Technologies-Used)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Test Tasks](#test-Tasks)
- [Generating HTML Reports](#generating-html-reports)
- [Jenkins CI/CD](#jenkins-ci-cd)
- [Project Structure](#Project-Structure)
- [Contact](#Contact)

##  Technologies Used
<a href="https://www.postman.com/"><img src="https://user-images.githubusercontent.com/25181517/192109061-e138ca71-337c-4019-8d42-4792fdaa7128.png" title="POSTMAN" alt="POSTMAN" width="40" height="40"/></a>
<a href="https://www.jenkins.io"><img src="https://user-images.githubusercontent.com/25181517/179090274-733373ef-3b59-4f28-9ecb-244bea700932.png" title="Jenkins" alt="Jenkins" width="40" height="40"/></a>
![Newman](https://img.shields.io/badge/Newman-Command_Line-brightgreen)
## Features
- Detailed and organized API test suites.
- Test cases covering various endpoints, HTTP methods, and scenarios using Google sheets.
- Exported Postman collection for manual testing and integration into CI/CD pipelines.
- Automation of API testing through cmd and Jenkins.
- Continuous integration (CI) and continuous delivery (CD) setup instructions.

## Prerequisites
Before you begin, ensure you have met the following requirements:

- **Postman**: You need to have Postman installed. If you don't have it, you can download it from [Postman Downloads](https://www.postman.com/downloads/).

- **Newman**: You can install Newman using Node.js. Make sure you have Node.js installed, and then run the following command:

  ```bash
  npm install -g newman

- **Jenkins**: You will need a Jenkins server set up for CI/CD automation. You can install Jenkins following the instructions on the Jenkins website.

## Installation

- Install the project dependencies:
  ```bash
  Install Postman
  Install Newman
  Install newman-reporter-htmlextra
  Install Java

- Clone this repository to your local machine:

  ```bash
  git clone https://github.com/Mochxd/Trello-Apis.git

- Navigate to the project directory:

  ```bash
  cd Trello-Apis

## Usage

**Running Tests in Postman**
1. Open Postman.
2. Import the Postman collection.
3. Configure the environment variables using the Postman environment "Bookingenvironment" directory or create your own environment file.
4. Run the API tests using Postman's collection runner.

**Running Tests via Command Line using Newman**

- You can also run the tests via the command line using Newman. Use the following command to run a specific test suite, specifying the environment:
  
  ```bash
  newman run TrelloAPIs.json -e Trelloenvironment.json -r htmlextra

## Test Tasks
**The tests are organized into collections within Postman, each focusing on specific API tasks:**

**- CREATE Token:** Test Task for creating an authentication token.

**-CREATE Board:** This task covers the creation of a new board.

**-GET Board:** Test Task for retrieving information about a board.

**-UPDATE Board:** Task for updating an existing board.

**-CREATE List:** This task covers the creation of a new list on a board.

**-GET List:** Test Task for retrieving information about a list.

**-UPDATE List:** Task for updating an existing list.

**-CREATE Card:** This task covers the creation of a new card within a list on a board.

**-GET Card:** Test Task for retrieving information about a card.

**-GET Field on Card(id):** Test Task for retrieving specific fields on a card.

**-UPDATE Card:** Task for updating an existing card.

**-CREATE a new Label on a Card:** Task for adding a new label to a card.

**-CREATE Attachment On Card:** Task for attaching a file to a card.

**-GET an Attachment on a Card:** Test Task for retrieving information about an attachment on a card.

**-CREATE Checklist:** Task for creating a new checklist for a card.

**-GET Checklist:** Test Task for retrieving information about a checklist.

**-UPDATE Checklist:** Task for updating an existing checklist.

**-CREATE Checkitem:** Task for adding a new check item to a checklist.

**-GET Checkitem:** Test Task for retrieving information about a check item.

**-DELETE Checkitem:** Task for deleting a check item from a checklist.

**-DELETE Checklist:** Task for deleting a checklist from a card.

**-DELETE Attachment On Card:** Task for deleting an attachment from a card.

**-DELETE Card:** Task for deleting a card.

**-DELETE Board:** Task for deleting a board.

- For more details on the test scenarios, expected outcomes, and specific requests you will find it in the Google sheets([https://docs.google.com/spreadsheets/d/1D-xLCOiNJyycsRCLlbhDLvYaAMGR-jPT3qeNSEzXP-Q/edit#gid=3](https://docs.google.com/spreadsheets/d/1JU9Yrt5G-DRZw8aoCOLeGR6dzhtsPK-NuZSU0JyETcI/edit#gid=3))

## Generating HTML Reports
Newman supports multiple reporters, including htmlextra, which generates detailed HTML reports for your API test runs. To generate HTML reports, simply specify the -r htmlextra option when running Newman, as shown in the example above.

The HTML reports will be available in the reports directory of this repository.

## Jenkins CI/CD
The repository is configured to automate the API testing process using Jenkins for CI/CD. Jenkins pipelines are set up to trigger API tests when changes are pushed to the repository. Jenkins will run the tests, generate HTML reports, and provide feedback on the test results.

## Project Structure

- Trello-Apis
- ├──  TrelloAPIs.json
- ├──  Trelloenvironment.json 
- ├──  Tests
- │   └── 📜 Manual Test Cases
- ├──  reports
- │   ├── 📜 Newman HTMLEXTRA.html
- │   └── 📜 Newman HTML.html

## Contact

If you have any questions, suggestions, or issues related to this project, please feel free to contact us. We welcome your feedback and contributions.
- **Email**: Mohamedbadrxd@gmail.com

Feel free to open an issue in this repository or reach out to me directly. I appreciate your interest and support!
