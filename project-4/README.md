# Serverless Applications
TODO list application that is used to demonstrate a number of AWS services that were used to build the architecture for this web application. I completely automated the CI/CD pipeline so that the serverless functions are automatically deployed to AWS when latest source is pushed to github using travis.ci.

Deployed application can be found here: [click here](http://a8baa58f5a4764166943655a9dab4eae-1199825330.us-east-2.elb.amazonaws.com:8080/)

## Architecture
this application is built using the following AWS services:
- AWS Lambda
- AWS API Gateway
- AWS DynamoDB
- AWS S3
- AWS Elastic Kubernetes Service (EKS)
- AWS CloudFormation

## [Web Application Project](https://github.com/ezedinff/todo-app)
The web frontend is developed using ReactJS based on the TODO app from the previous project. It is deployed to AWS using AWS EKS service. CI pipeline is done by travis.io. It pulls latest source code form Github and build a docker image before pushing it to DockerHub to be ready for deployment,

Travis CI pipeline build Screenshot
![Travis CI pipeline build Screenshot](/project-4/screenshots/travis-ci-pipeline-frontend.png)

DockerHub Screenshot
![DockerHub image](/project-4/screenshots/dockerhub-image.png)

## [Serverless Functions Project](https://github.com/ezedinff/serverless-todo-api)
The web backend is made up of a number of serverless functions using AWS Lambda with Node.js runtime. Along with other resources such as S3 to store images and a DynamoDB table to store TODO items, the serverless function are deployed to AWS using Serverless framework. CI/CD pipeline is completely automated by travis.io.

Travis CI pipeline build Screenshot
![Travis CI pipeline build Screenshot](/project-4/screenshots/travis-ci-pipeline-backend.png)

