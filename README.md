# Example Flask Application 

This repo holds an example Go application that uses FusionAuth as the identity provider. 
This application will use an OAuth Authorization Code Grant workflow to log a user in and 
get them access and refresh tokens.

This application was built by following the [Golang Quickstart](https://fusionauth.io/docs/quickstarts/fusionauth-quickstart-golang-web).

## Project Contents

The `docker-compose.yml` file and the `kickstart` directory are used to start and configure a local FusionAuth server.

The `/complete-application` directory contains a fully working version of the application.

## Project Dependencies
* Docker, for running FusionAuth
* Go 1.16 or later, for running the Changebank Go application

## Running FusionAuth
To run FusionAuth, just stand up the docker containers using `docker-compose`.

```shell
docker-compose up
```

This will start a PostgreSQL database, and Elastic service, and the FusionAuth server.

## Running the Example App
To run the application, first go into the project directory

```shell
cd complete-application
```

Get your dependencies and create a go.sum file.

```shell
go mod tidy
```

Then use the `go` command to start up the application.

```shell
go run main.go
```

Visit the local webserver at `http://localhost:8080/` and sign in using the credentials:

* username: richard@example.com
* password: password
