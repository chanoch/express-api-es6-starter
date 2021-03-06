<p align="center">
  <img alt="Express API ES6 Starter" src="https://i.imgur.com/qeAbxtQ.png">
</p>

[![Build Status](https://travis-ci.org/mesaugat/express-api-es6-starter.svg?branch=master)](https://travis-ci.org/mesaugat/express-api-es6-starter)
[![Codecov](https://codecov.io/gh/mesaugat/express-api-es6-starter/branch/master/graph/badge.svg)](https://codecov.io/gh/mesaugat/express-api-es6-starter)

Starter application for building APIs with [Express.js](http://expressjs.com/)

Comes with:

* [ES6](http://babeljs.io/learn-es2015/) features/modules
* ES7 [async](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)/[await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await)
* API documentation using [swagger-ui-dist](https://www.npmjs.com/package/swagger-ui) and [swagger-jsdoc](https://www.npmjs.com/package/swagger-jsdoc)
* [ESLint](http://eslint.org/) for code linting
* Request validation using [Joi](https://www.npmjs.com/package/joi)
* Code formatting using [Prettier](https://www.npmjs.com/package/prettier)
* Configuration management using [dotenv](https://www.npmjs.com/package/dotenv)
* Logging using [winston](https://www.npmjs.com/package/winston)
* Error reporting using [raven](http://npmjs.com/package/raven)
* Tests using [mocha](https://www.npmjs.com/package/mocha), [supertest](https://www.npmjs.com/package/supertest) and [chai](https://www.npmjs.com/package/chai)
  and jest

* husky - git hooks support to run validation prior to commit
* raven - sentry exception saas
* codecov - for code coverage reports
* nyc - istanbul cli for test coverage ??

---

## Prerequisites

* [Node.js](https://yarnpkg.com/en/docs/install) - 8.9.0 or above
* [NPM](https://docs.npmjs.com/getting-started/installing-node) - 5.5.1 or above

## Setup

Clone the repository, install the dependencies and get started right away.

    $ git clone git@github.com:chanoch/express-api-es6-starter.git <application-name>
    $ cd <application-name>
    $ rm -rf .git
    $ yarn   # or npm install

Finally, start the application.

    $ npm run dev (For development)
    $ yarn start (For production)

Navigate to http://localhost:{PORT}/api-docs/ to verify installation.

## Setup Using Docker

Use [docker-compose](https://docs.docker.com/compose/) to quickly bring up a stack with pre-configured Postgres database container. Data is ephemeral and containers will disappear when stack is removed.

Specific configuration for Docker is in `.env.docker`
- `0.0.0.0` as `$APP_HOST` to expose app on Docker network interface
- Pre-configured Postgres settings - can be updated to point to another Postgres host

Bring up stack,

    $ docker-compose up

Navigate to http://localhost:8848/api-docs/ to verify application is running from docker.

Bring down stack,

    $ docker-compose down

## Tests

To run the tests you need to create a separate test database. Don't forget to update your `.env` file to include the name of the test database and run the migrations.

    $ NODE_ENV=test yarn migrate
    $ yarn test

Run tests with coverage.

    $ yarn test:coverage

## Contributing

For contribution and feature requests, please create an [issue](https://github.com/mesaugat/express-api-es6-starter/issues) first.

## License

express-api-es6-starter is under [MIT License](LICENSE.md).
