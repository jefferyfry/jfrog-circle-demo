# JFrog CircleCI Demo

[![Git](https://app.soluble.cloud/api/v1/public/badges/5524d24a-b822-4779-b4b6-1acd85eb6706.svg?orgId=604336610407)](https://app.soluble.cloud/repos/details/github.com/jefferyfry/jfrog-circle-demo?orgId=604336610407)  

This repository contains the code for the [JFrog CircleCI Demo webinar](https://devops.com/webinars/). This webinar is jointly presented by CircleCI and JFrog and discusses how to develop a CI/CD pipeline with [CircleCI](https://www.circleci.com/) and [the JFrog Platform](https://jfrog.com/platform/). It contains a npm application and dockerfile. A CircleCI pipeline builds and deploys the application.

## Prerequisites
This demo requires CircleCI and JFrog. Set up free accounts!

* [CircleCI Free Subscription](https://circleci.com/pricing/)
* [JFrog Free Subscription](https://jfrog.com/artifactory/start-free/#saas) 

## CircleCI Pipeline Workflow
![circleci-jfrog-pipeline](https://user-images.githubusercontent.com/6440106/108023777-2936ac00-6fd8-11eb-9513-474fa9f97f1f.png)

## Building with the CircleCI Pipeline
The CircleCI pipeline is located at [.circleci/config.yml](.circleci/config.yml). In the CircleCI console it appears as:

![circleci pipeline](https://user-images.githubusercontent.com/6440106/108663117-a2c11500-7484-11eb-8e6c-abeb3d6d302c.png)

## Using the JFrog CLI in the Pipeline
The [JFrog CLI](https://www.jfrog.com/confluence/display/CLI/JFrog+CLI) is a powerful tool that you can use in your CI/CD process and toolchain. It can be used to build code and publish artifacts while collecting valuable build information along the way. It greatly simplifies the publishing of the build artifacts and the build info to JFrog Artifactory. It is commonly used in automation scripts and with CI/CD software tools like CircleCI. One of the useful things it does is collect valuable build information. This is important for traceability.

![Build Info](https://user-images.githubusercontent.com/6440106/108663807-4101aa80-7486-11eb-9306-2d0d024a058f.png)

## Scanning for Security Vulnerabilites and License Compliance Issues
With Xray, build artifacts can be scanned for security vulnerabilites and license compliance issues. If issues are discovered, the build can be set to fail preventing compromised applications and libraries from reaching production.

![](https://user-images.githubusercontent.com/6440106/108664167-09dfc900-7487-11eb-9da9-8a4b97801ecc.png)

## Pushing Artifacts to Artifactory
This pipeline produces a NPM package and a Docker image which are pushed to Artifactory repositories.

![artifacts](https://user-images.githubusercontent.com/6440106/108663244-f5023600-7484-11eb-9070-06c8cc2baa41.png)

## Deploying to Amazon ECS
The final step to the CircleCI pipeline is deploying to Amazon ECS. This job uses the [AWS ECS Orb](https://circleci.com/developer/orbs/orb/circleci/aws-ecs#jobs-update-task-definition). The pipeline updates the container image of an existing task definition.

![ECS](https://user-images.githubusercontent.com/6440106/108663455-76f25f00-7485-11eb-812b-da9bdd7efd74.png)


# Demo App

![jfrog-circle-demo-app](https://user-images.githubusercontent.com/6440106/108022107-c859a480-6fd4-11eb-8d0b-a3203ca83494.png)

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 10.1.7.

## Build and Run Docker Image Locally

```
$ docker build -t demo-app . 
$ docker run -p 443:443 -p 80:80 docker.io/library/demo-app
```

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
