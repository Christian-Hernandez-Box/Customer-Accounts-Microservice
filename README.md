# Customer Accounts Microservice
![Build Status](https://github.com/Christian-Hernandez-Box/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.9](https://img.shields.io/badge/Python-3.9-green.svg)](https://shields.io/)

## Overview

This project is a RESTful microservice for managing customer accounts, developed as part of a Capstone project. The microservice was built using Agile methodologies and Test-Driven Development (TDD) practices, with a focus on secure, containerized deployment and automated CI/CD processes.

## Technologies Used

Programming Languages & Frameworks: Python, Flask

Database: PostgreSQL

Containerization & Orchestration: Docker, Kubernetes, OpenShift

CI/CD: GitHub Actions

Security: Flask-Talisman, Flask-CORS

Development Practices: Agile, TDD

Linting: Flake8

Version Control: Git, GitHub

## Features

CRUD Operations: Implemented Create, Read, Update, Delete (CRUD) functionalities for customer accounts.

Test-Driven Development: Achieved 95% test coverage using nosetests and coverage tools.

Automated CI/CD Pipeline: Configured GitHub Actions workflows to automate testing, linting, and deployment.

Security: Integrated Flask-Talisman for security headers and Flask-CORS for Cross-Origin Resource Sharing (CORS) policies.

Containerized Deployment: Dockerized the microservice and deployed it to an OpenShift/Kubernetes cluster.

## Project layout

The code for the microservice is contained in the `service` package. All of the test are in the `tests` folder. The code follows the **Model-View-Controller** pattern with all of the database code and business logic in the model (`models.py`), and all of the RESTful routing on the controller (`routes.py`).

```text
├── service         <- microservice package
│   ├── common/     <- common log and error handlers
│   ├── config.py   <- Flask configuration object
│   ├── models.py   <- code for the persistent model
│   └── routes.py   <- code for the REST API routes
├── setup.cfg       <- tools setup config
└── tests                       <- folder for all of the tests
    ├── factories.py            <- test factories
    ├── test_cli_commands.py    <- CLI tests
    ├── test_models.py          <- model unit tests
    └── test_routes.py          <- route unit tests
```
