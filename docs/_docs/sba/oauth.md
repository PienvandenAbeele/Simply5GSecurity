---
title: OAuth 2.0
permalink: /docs/oauth/
---
<style>body {text-align: justify}</style>

OAuth 2.0 is the successor of OAuth 1.0 and stands for Open Authorisation. It allows a website or application to access a resource hosted by another application on behalf of a user.
A well-known example is a way if you want to sign up or log in to a website, there is often an option to “sign in with google”. Here you are the user, and you allow the website to use your google account as identification.
OAuth 2.0 uses Access Tokens, which is a piece of data which represents the authorisation on behalf of the end-user to access resources. Often this is done in the JSON Web Token format but it is not specified. For security reasons, an Access Token may have an expiration date, but this is also not mandatory.

There are a few components of OAuth 2.0 which are important to understand how it works:

- Resource Owner: This is the user or system which is the owner of the protected resources and can grant access to them.

- Client: The client is the system that wants access to the protected resources, which can be achieved with a valid Access Token

- Authorisation Server: The authorisation server will receive the requests for an Access Token to access certain resources from the client. If the resource owner gives consent for this request, the authorisation server will issue an Access Token to the client.

- Resource Server: At the resource server, the client will present the Access Token and if the token is valid, the resource server will return the appropriate resource to the client.

In the 5G security architecture, the roles are divided as follows:
- The Network Repository Function (NRF) shall be the OAuth 2.0 Authorisation server.
- The NF in need of a service from another NF shall be the OAuth 2.0 client.
- The NF providing a service to an NF shall be the OAuth 2.0 resource server & owner.

<img src="{{ "/assets/img/Sec/oauth.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

# EXLPLAIN IMAGE