---
title: OAuth 2.0
permalink: /docs/oauth/
---
<style>body {text-align: justify}</style>

OAuth 2.0 is the successor of OAuth 1.0 and stands for Open Authorisation. It allows a website or application to access a resource hosted by another application on behalf of a user.
A well-known example is a way if you want to sign up or log in to a website, there is often an option to “sign in with google”. Here you are the user, and you allow the website to use your google account as identification.
OAuth 2.0 uses Access Tokens, which is a piece of data which represents the authorisation on behalf of the end-user to access resources. Often this is done in the JSON Web Token format but it is not specified. For security reasons, an Access Token may have an expiration date, but this is also not mandatory.

There are a few components of OAuth 2.0 which are important to understand how it works. The **resource owner**, is the user or system which is the owner of the protected resources and can grant access to them. The **(application) client** is the system that wants access to the protected resources, which can be achieved with a valid access token. The **authorisation server** will receive the requests for an access token to access certain resources from the client. If the resource owner gives consent for this request, the authorisation server will issue an access token to the client. Lastly, the **resource server**, where the client will present the access token and if the token is valid, the resource server will return the appropriate resource to the client.
In the images below, the follow is shown with each step explained.

<div class="row">
    <div class="col-md-5">
    <br>
        <ol>
            <li>The client requests authorisation from the resource owner.</li>
            <li>The client receives an authorisation grant.</li>
            <li>The client requests an access token through identity verification with the help of the authorisation server and authorisation grant provision.</li>
            <li>The authorisation server verifies the client by checking the authorisation grant and, if it’s valid, issues an access token and refresh token.</li>
            <li>The client requests a secure resource from the provider and authenticates by presenting the access token.</li>
            <li>The provider checks the access token and, if valid, serves the request.</li>
        </ol>
        <br>
    </div>
    <div class="col-md-7">
    <br>
        <img src="{{ "/assets/img/Sec/oauthORI.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div class="col-md-5">
        <br>  
        <br> 
        In the 5G security architecture, the roles are divided as follows:  
        <ul>
            <li>The <a href="{{ "/docs/nrf/" | relative_url }}">Network Repository Function (NRF)</a> shall be the OAuth 2.0 Authorisation server.</li>
            <li>The <a href="{{ "/docs/core/" | relative_url }}">NF</a> in need of a service from another <a href="{{ "/docs/core/" | relative_url }}">NF</a> shall be the OAuth 2.0 client.</li>
            <li>The <a href="{{ "/docs/core/" | relative_url }}">NF</a> providing a service to an <a href="{{ "/docs/core/" | relative_url }}">NF</a> shall be the OAuth 2.0 resource server & owner.</li>
        </ul>
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/Sec/oauth.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

