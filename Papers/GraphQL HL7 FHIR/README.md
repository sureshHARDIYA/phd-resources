# Components

The prototype contains following major components:

- `Resource Server`:T his is a FHIR compliant web server that is able to respond to HTTP requests using Access Tokens issued by the Authorization Server.
- `The User:` This is the person who is actually logging into the application to perform some function. Not all SMART on FHIR flows actually require a user to be present but most do.

- `The SMART on FHIR Application` (referred to as the “SMART App” or “Client” below): This is an application that the user wishes to access to perform some function.

- `Authorization Server:`` This is an OpenID Connect compliant web server that is able to authenticate users and issue Access Tokens. Smile CDR is able to perform this role but other Authorization Servers may also be used.
