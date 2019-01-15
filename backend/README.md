# Ducatus Backkoffice API

>

## About

This project uses [Feathers](http://feathersjs.com). An open source web framework for building modern real-time applications.
## Code

### formatting, es2017+, etc.

We're running `eslint`. It is configured to not write trailing semi-colons etc. Please see .eslint for other rules.

We have all the esXXXX things - es2015, es2016, es2017, object-rest-spread - courtesy of babel.



## Getting Started

Getting up and running is as easy as 1, 2, 3.

1. Make sure you have [NodeJS](https://nodejs.org/) and [npm](https://www.npmjs.com/) installed.
2. Install your dependencies

    ```
    cd path/to/backoffice-api; npm install
    ```

3. Install docker | docker-compose in your workstation

## Running docker

    ```
    cd path/to/backoffice-api; docker-compose up -d
    ```
To verify if both `nodejs` and `mongodb` images are instantiated, run `docker ps`

### Tests
We're testing via jest, with `unit-test` and `end-to-end-test` folders under `test` and named \*.test.js, eg.
```
default.test.js
user.test.js
```

There are a couple of handy scripts -

* `npm test` runs the tests (unit-tests) once and then stops.
* `npm e2e-test` runs the end-to-end-tests (unit-tests) once and then stops.

### Configuration

Configuration uses 12factor-config, extracting all of the meaningful config properties to env
variables as described by [The Twelve Factor App](https://12factor.net/).

You'll need to set env vars for all of the non-default properties, and maybe override some of
the defaults too.

One way to do this in development is to create a .env file in the root of the project (it will
be .gitignored) and `source ./.env` before running the app.

In code you can access the config properties simply by importing `config.js` from the project root,
e.g. a file in ./src could use config like this:

```
import `../config`
console.log(`the bind port is ${config.bindPort}`)
```

## Lint

    ```
    cd path/to/backoffice-api; npm run eslint
    ```

## Production

    ```
    cd path/to/backoffice-api; npm run build; npm run prod
    ```

## Scaffolding

Feathers has a powerful command line interface. Here are a few things it can do:

```
$ npm install -g @feathersjs/cli          # Install Feathers CLI

$ feathers generate service               # Generate a new Service
$ feathers generate hook                  # Generate a new Hook
$ feathers generate model                 # Generate a new Model
$ feathers help                           # Show all commands
```
