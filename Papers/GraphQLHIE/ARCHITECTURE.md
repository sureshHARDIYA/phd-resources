# `Resource Server` <a name="resourceServer"></a>

This is a FHIR compliant web server that is able to respond to HTTP requests using Access Tokens issued by the `Authorization Server`.

# Mobile Client <a name="mobileClient"></a>

- `The User:` This is the person who is actually logging into the application to perform some function. Not all SMART on FHIR flows actually require a user to be present but most do.

- `The SMART on FHIR Application` (referred to as the “SMART App” or “Client” below): This is an application that the user wishes to access to perform some function.

# Web Client <a name="webClient"></a>

# Authorization Server <a name="Authorization"></a>

The authorisation server is an OpenID connect [40] compliant web server with an ability to authenticate users and grant authorisation access tokens. More- over, authorisation server manages scopes and permission of the clients, introspects token and requests for the resource server.
