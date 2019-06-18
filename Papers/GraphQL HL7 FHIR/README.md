# Introduction

# Motivation

# Architecture

The prototype contains following major components:

- `Resource Server`:T his is a FHIR compliant web server that is able to respond to HTTP requests using Access Tokens issued by the Authorization Server.
- `The User:` This is the person who is actually logging into the application to perform some function. Not all SMART on FHIR flows actually require a user to be present but most do.

- `The SMART on FHIR Application` (referred to as the “SMART App” or “Client” below): This is an application that the user wishes to access to perform some function.

- `Authorization Server:` This is an OpenID Connect compliant web server that is able to authenticate users and issue Access Tokens. Smile CDR is able to perform this role but other Authorization Servers may also be used.

## Resource Server

## Mobile Client

## Web Client

## Authorization Server

# Technologies

## [`ReactJS`](https://reactjs.org/)

ReactJS is a component-based JavaScript library that follows the declarative programming paradigm. The declarative views can be utilized to create complex interactive UI which serves as the presentational component of the web[[1]](#1). The library is easy to learn, promotes code reusability, offers lightweight DOM for better performance, enforces unidirectional data flow, ensures Search Engine Optimizations (SEO), forms the views of Model View Controller(MVC) architecture and supports virtual DOM.

## `Redux`

## `Redux Saga`

## `Immutable JS`

## `mongoDB`

## `Ant Design Pro`

## `GraphQL`

- How does `GraphQL` work?
- How is `GraphQL` queries validated and executed?

## `Apollo-tags`

## `Redux-Form`

# Getting Started

# Discussion

# Conclusion

# FAQs

1. Why did we build our application using `ReactJS`?
2. What is `Redux`? Why do we need it?
3. What is `Redux-Saga`? Why do we need it?
4. Why is our prototype using `mongoDB`? Why not others?
5. What is `HL7 FHIR`? And why should we use it?
6. What is `INTROMAT`?

# References

[1] <a name="1"></a>Suresh Kumar Mukhiya, Fazle Rabbi, Violet Ka I Pun, Yngve Lamo, An architectural design for creating self-reporting e-health systems. InICSE 2019Proceedings in the IEEE Digital Library(2018).
[2] <a name="2"></a> Mukhiya, S. K., & Hoang Hung, K. (2018). An Architectural Style for Single Page Scalable Modern Web Application, 5(4), 6–13. Retrieved from https://www.ijrra.net/Vol5issue4/IJRRA-05-04-02.pdf
