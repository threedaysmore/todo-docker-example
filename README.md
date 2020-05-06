# docker-todo-example

This is a docker example that runs an aspnetcore API, a Mailhog mail server, and a Vue front-end all in separate containers.

## Prerequisites

* Docker is installed on your machine. Installation instructions found [here](https://docs.docker.com/get-docker/).
* If you want to run these projects locally(not in containers) you will need the following installed: [dotnet](https://dotnet.microsoft.com/download/dotnet-core/thank-you/sdk-3.1.201-windows-x64-installer), [vue-cli](https://cli.vuejs.org/guide/installation.html)

## Get Started

All containers can be fired up and run together by running:

`docker-compose up`

Swagger for API can be accessed at:

<http://localhost:8080/swagger/index.html>

Vue front-end can be accessed at:

<http://localhost:8081/#/>

Mailhog webserver can be accessed at:

<http://localhost:8025/>

API can be run locally with:

```powershell
cd ./TodoApi
dotnet run
```

Vue app can be run locally with:

```powershell
cd ./todo-app
npm run dev
```
