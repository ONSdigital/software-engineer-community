# Secrets

A secret is data that should not be publicly exposed. This is because it may give access to systems, or access to decrypt sensitive information.  

Before committing to a repository, careful attention should be made to prevent any secret from being checked in. 

#### Types of secrets
* Password
* Certificate
* Domain
* API key
* Private key
* URI containing user credentials
* IP address

#### Loading secrets
Secrets may need to be loaded for an application to start and/or talk to other applications. These secrets could be loaded by one of the following:

* Environment Variables (suggested by [12 factor](https://12factor.net/config))
* Tools for managing secrets, e.g. Vault
