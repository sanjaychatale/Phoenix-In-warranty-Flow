# Postman API Automation with GitHub Actions #
This repository is the demonstaration for POC for integrating Postman tests with GitHub Actions. The tests are written in Postman tool and executed on VM with the help of Newman and newman-reporter-htmlextra.
GitHub Action will trgigger the project execution on every push to the main branch. You can also run the project manually using Run Workflow (workflow_dispatch). The project run on a scheuled time with the help of Cron job
The HTML report is archived and kept in artifcat section to view and download directly from the GitHub Page : https://github.com/sanjaychatale/Phoenix-In-warranty-Flow
The latest report is mailed to the team members using GMAIL SMTP 

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge case testing
3. Token Testing
4. Data Drivern Testing with csv
5. Schema Validation
6. Secrets Management with GitHub Secrets
   
## Tech Stack ##
1. Postman
2. Node Js 22v
3. Newman
4. newman-reporter-htmlextra
5. GitHub Actions
6. Gmail SMTP
7. GitHub Page
8. CSV for Test Data

## GitHub Pages ##
You can view the latest postman test run result on the GitHub Page : https://github.com/sanjaychatale/Phoenix-In-warranty-Flow

## HTML Reporting ##
The report will be created in newman folder
![Postman Report](https://github.com/sanjaychatale/Phoenix-In-warranty-Flow/blob/static-content/newman-report.png)

## How to run the project ##
On your local you can run the project using 
1. Clone the remote project on your local system : https://github.com/sanjaychatale/Phoenix-In-warranty-Flow.git
2. Install Node JS and NPM from : https://www.npmjs.com/package/newman
3. Install Newman : npm install -g newman
4. Install Newman HTML Reporter : npm install -g newman-reporter-htmlextra
5. Run the Newman Command :
   newman run 'Inwarranty-flow Collection_data.postman_collection' \
   -e QA.postman_environment.json \
   -d testData.csv \
   -r cli,htmlextra \
   --reporter-htmlextra-export ./newman/index.html
