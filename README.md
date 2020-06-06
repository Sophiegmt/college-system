<p align="center">
  <img src="client/client/static/ist_logo.png">
</p>

### Table of contents
* [What is this?](#what-is-this)
* [Client App](#client-app)
* [Backend Api](#backend-api)
* [Canteen microservice](#canteen-microservice)
* [Rooms microservice](#rooms-microservice)
* [Secretariats microservice](#secretariats-microservice)


## What is this?
Welcome to the **Técnico** microservices integration app. This system is built on top of a scalable microservice 
oriented architecture were we have a client app, requesting data from a backend API, wich communicates with microservices that serve college
related data.

The system consists of **5 main REST** entrypoints
- **Client API**
- **Backend API**
- **Canteen Microservice**
- **Rooms Microservice**
- **Secretariats Microservice**

## Client App
This is were the requests to the administration endpoints are managed, which focuses on the creation, editing, deletion and listing of data related to the event.

#### Features:
**Verification**: 
Verify another user identity by inserting his personal code.

**QR code reader**:
Scan a space qr code and receive information on it.

**Admin**:
Manage secretariats, microservices and logs.

**Authentication**:
Authentication of students his done in the Fenix OAuth environtment.
Admins are logged in through a username and password


## Backend Api
This API serves the data of all the microservices, and also manages the users of the client app.

#### Features:
**Microservices**
This api is abstracted enough to enable the scaling of microservices. The main entrypoint is a proxy-route
which receives requests and forwards them to the correct microservice.

**Verification**
Manage the users of the client app, and their codes, storing all the required data in a file.

** Manage Secretariats microservice data
Create and edit the secretariats available.


## Canteen microservice
This service request canteen menus from the IST Fenix API and serves them.

#### Features:
**Canteen menus**
List all, and request one by date


## Rooms microservice
This service request space data from the IST Fenix API and serves it.

#### Features:
**Spaces**
Request one by id

## Secretariats microservice
This service binds to a secretariats database and serves data on this models.

#### Features:
**Secretariats**
List all, create and edit.


## Tech Stack
*   Python 3.6
*   Flask
*   PostgreSQL
*   Docker
