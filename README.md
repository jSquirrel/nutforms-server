# Nutforms Server

[![Build Status](https://travis-ci.org/jSquirrel/nutforms-server.svg?branch=master)](https://travis-ci.org/jSquirrel/nutforms-server)

Server-side aspect registries for automatic form generation.

## Installation


This project is managed my [Maven](http://maven.apache.org), which must
be installed on your system.

First, you need to install and build [Adaptive RESTful API](https://travis-ci.org/jSquirrel/adaptive-restful-api).

```
$ git clone git@github.com:jSquirrel/adaptive-restful-api.git ./adaptive-restful-api
$ cd ./adaptive-restful-api
$ mvn install
```

Then download the server library and build it.

```
$ git clone https://github.com/jSquirrel/nutforms-server ./nutforms-server
$ cd ./nutforms-server
$ mvn install
```

## Running tests

Tests are executed via Maven. Navigate to the folder in which your Nutforms Server
libary is installed and run the tests.

```
$ mvn test
```

## Contributing

Feel free to contribute to the project by reporting [issues](https://github.com/jSquirrel/nutforms-server/issues)
or creating [pull requests](https://github.com/jSquirrel/nutforms-server/pulls).

## License

This software is provided under [MIT License](https://opensource.org/licenses/MIT).

## Documentation

For better understanding of this library,
please see [documentation](https://github.com/jSquirrel/nutforms-server/tree/master/docs/en/index.md).
