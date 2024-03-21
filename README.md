# Fridge Cooker

## Table of Contents

[Features](#main-features) | [Installation](#installation) | [Usage](#usage) | [API](#api) | [Development](#development) | [Contribution](#contribution) | [Internals](#internals) | [Pipeline](#pipeline) | [Environment](#environment) | [Changelog](#changelog)

## Main Features

* **Recipe Search:** Easily find pre-made recipes based on criteria such as ingredients, cooking time, number of people to cook for, and more.

* **Recipe History:** Save discovered or generated recipes for future reference and easy access.

for more details read the Product Requirement Definition

## Installation

### Pre-requisites

In order to install and run the project

* Taskfile: https://taskfile.dev

* Docker: https://www.docker.com/products/docker-desktop/

### Step by Step Install

Step1 : build & pull all required container images locally

```Bash
task build.install
```

Step2 : launch the application in container running locally

```Bash
task local.run
```

visit the url [http://localhost:8081](http://localhost:8081) with your favorite browser or

```Bash
curl -i [http://localhost:8081](http://localhost:8081])
```

## Usage

### taskfile Commands

To list all available commands display the help documentation with the command

```Bash
task help
```

### Run localy

Initialize the Database

```Bash
task local.db.init
```

Launch the application

```Bash
task local.run
```

Visualize the logs

```Bash
task local.logs
```
Run static analysis

```Bash
task tests.static
```

Execute unit tests

```Bash
task tests.unit
```


## Technical Design

### API

The following routes are exposed as a REST API resources

Path | Verb | Use Case
------------ | ------------- | -------------
/history | GET | retrieve a collection of past recipes
/recipes | GET | retrieve past discovered and used recipe

###  Clean Architecture:
This application is architectured around a pragmatic adaptation of clean architectur which advocate for the layering of the architecture with strict rules around separation of concerns and communication by contracts. [more](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)


### Primary Structure

Based on the principles cited above th code primary structure is the following 

* **API:** This layer exposes the business going as REST API resources. Controllers, Validators and Transformers.
* **UseCase:** This layer holds the Application logic that orchestrates business logic and persistence. Queries, Commands and Handlers.
* **Domain:** This layer holds business logic, business objects and business rules. Entities, Rule Engine and Value Objects.
* **Infra:** This layer holds the data access logic, it has the knowledge of the type of storage from where to read or write the data.

for more details [Technical Requirements Documents](TRD.md)


## Release & Delivery

### CICD

### Deployment

task a new release version.


## Contribution

Before contributing code to this project please follow the Contributing guidelines on the following aspect:

* Coding Styles
* Commit Messages
* Branche Naming
* Merge Request Template

You will find detailed guidelines on these topics [here](CONTRIBUTING.md)
