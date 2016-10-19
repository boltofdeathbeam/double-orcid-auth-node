# double-orcid-auth-node

Simple node.js app that demonstrates a workflow that uses 2 oauth requests.

This mimics a scenario in the ORCID record auto-update workflow, where users need to grant permission to both a submission system and a DOI registration system in order to complete the process.

## Quickstart

### 1. Install NodeJS or Upgrade 

[Install it!](https://nodejs.org/)
or 
[Upgrade it!](http://davidwalsh.name/upgrade-nodejs)



### 2. Download Project

Download [zip file](https://github.com/ORCID/double-orcid-auth-node/archive/master.zip) and
 unzip.
   

### 3. Open a command prompt

* **Windows**
 
    Select `Search programs and files` type in `node.js command prompt` and select `Node.js command prompt`.
    
* **OSX**
 
    Open terminal by clicking `Search Spotlight` typing in `Terminal` and selecting Terminal.


### 4. cd into the ```pubpals``` directory inside the directory you just cloned or unzipped

Depending on how you downloaded and unzipped the project.

* **Windows**

        cd Downloads/double-orcid-auth-node-master/double-orcid-auth-node-master/pubpals

* **OSX**
 

        cd Downloads/double-orcid-auth-node-master/pubpals


### 5. Install client app node dependencies

       npm install 

### 6. (OPTIONAL) Configure credentials. 

This example is configured with default test credentials. You can optionally request your own 
sandbox credentials: 
[http://orcid.org/content/register-client-application](http://orcid.org/content/register-client-application). 
The following configuration keys can be overwritten by setting 
[environment variables](http://en.wikipedia.org/wiki/Environment_variable):

* PUBPALS_CLIENT_ID - Client id issued by ORCID.
* DOIDUDES_CLIENT_ID - Client id issued by ORCID.
* CLIENT_SECRET - Client secret issued by ORCID
* AUTHORIZE_URI - https://sandbox.orcid.org or https://orcid.org
* TOKEN_PATH - https://api.sandbox.orcid.org/oauth/token, https://pub.sandbox.orcid.org/oauth/token,
* CODE_CALLBACK_URI - Link use is sent back to with OAuth2 authorization code.


### 7. Start pubpals client application.

       node client-app.js

### 8. Open localhost [https://localhost:8443/](https://localhost:8443/)
Since this is a demo app on localhost you'll get an invalid certificate message. After accepting the invalid certificate you should have the a sample client application running on your local machine!

### 9. Open another command prompt window/tab (and keep the first one open as well!)

### 10. In the new window/tab cd into the ```doidudes``` directory inside the ```double-orcid-auth-node-master``` directory

Depending on how you downloaded and unzipped the project.

* **Windows**

        cd Downloads/double-orcid-auth-node-master/double-orcid-auth-node-master/doidudes

* **OSX**
 

        cd Downloads/double-orcid-auth-node-master/doidudes

### 10. Install client app node dependencies

       npm install 

### 11. (OPTIONAL) Configure credentials, as in step 6 above. 

### 12. Start doidudes client application.
       node client-app.js

The DOI Dudes app runs at [https://localhost:9443/](https://localhost:9443/), however, it's not necessary to open this page in a browser in order to use the demo.
