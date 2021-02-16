# JFrog CircleCI Demo

This repository contains the code for the [JFrog CircleCI Demo webinar](https://devops.com/webinars/). This webinar is jointly presented by CircleCI and JFrog and discusses how to develop a CI/CD pipeline with [CircleCI](https://www.circleci.com/) and [the JFrog Platform](https://jfrog.com/platform/). It contains a npm application and dockerfile. A CircleCI pipeline builds and deploys the application.

## Prerequisites
This demo requires CircleCI and JFrog. Set up free accounts!

* [CircleCI Free Subscription](https://circleci.com/pricing/)
* [JFrog Free Subscription](https://jfrog.com/artifactory/start-free/#saas) 

## CircleCI Pipeline Workflow
![circleci-jfrog-pipeline](https://user-images.githubusercontent.com/6440106/108023777-2936ac00-6fd8-11eb-9513-474fa9f97f1f.png)


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
