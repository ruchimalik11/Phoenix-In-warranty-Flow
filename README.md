# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating postman with github actions. The tests are written in postan and are executed on VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on a schedule time with the help of CRON job.

The HTML report is archived and kept in the artifact section for the team to download it. Along with that they can view the report directly from trhe github page : https://ruchimalik11.github.io/Phoenix-In-warranty-Flow/
The latest report is mailed to the team members using gmail SMTP.

## About me ##
Hi My Name is Ruchi Malik. I have 9 years of experience in Automation Testing and Devops. My skillset includes UI Automation with Selenium WebDrive, Cypress and for API testing I use Rest Assured and Postman.
You can connect to me over linkedin 
https://www.linkedin.com/in/ruchi-malik-08588383/

## Tech Stack ##
1. Postman
2. Node.js 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for self hosted github runner

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link: https://ruchimalik11.github.io/Phoenix-In-warranty-Flow/

## HTML Report ##
The report will be created in a newman folder
![Postman Report](https://github.com/ruchimalik11/Phoenix-In-warranty-Flow/blob/static-content/Html-Report.png)


## Project Structure ##


```
Phoenix Inwarranty Flow
├─ demo.txt
├─ Inwarrenty-flow Collection.postman_collection.json # Collection File
├─ QA.postman_environment.json  #Environment File
└─ testdata.csv

```

## How to run the project? ##
You can run the project on your local system for that:
1. Clone the Project on your local system: https://github.com/ruchimalik11/Phoenix-In-warranty-Flow.git
2. Install Nodejs and NPM from https://nodejs.org/en
3. Install Newman using npm install -g newman
4. Install Newman-reporter-htmlextra using npm install -g newman-reporter-htmlextra
5. Run the newman command:
  ``` 
   newman run 'Inwarrenty-flow Collection.postman_collection.json' \ 
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
```


## Testing coverage ##
1. Happy flow Testing
2. Negative Testing and edge case testing
3. Token testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets
