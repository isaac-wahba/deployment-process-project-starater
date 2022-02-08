# Udagram 

## Overview
With the services provided by GitHub and Circle CI, we could achieve the CI/CD concept by linking the [Circle CI project](https://app.circleci.com/pipelines/github/isaac-wahba/deployment-process-project-starater) with our [GitHub repository](https://github.com/isaac-wahba/deployment-process-project-starater). 
Whenever we commit a new change and push it to GitHub, the Circle CI project starts the deployment process directrly.

### CircleCI:
According to our config.yml file in the .circleci folder/directory

1. Orbs are used to install Node, Essential browser tools for testing frontend, AWS CLI, AWS EB.
2. The Execustion of the jobs starts wih the order mentioned in the workflow.

### Scripts and Steps:

 1. The `frontend:ready` script installs frontend project dependencies.
 2. It runs tests and builds the app to be ready.
 3. The `backend:ready` script installs backend project dependencies.
 4. It builds the app to be ready.
 5. The script `frontend:deploy` deploys the frontend app. 
 6. The script `backend:deploy` deploys the backtend app.
 
 
 The steps that that CircleCI follows dig deeper in every sub-detail required to execute the previous steps. 

![Circle CI Steps](https://github.com/isaac-wahba/deployment-process-project-starater/blob/main/Documentation/Important%20Screenshots/Circle%20CI%20Steps.png)
