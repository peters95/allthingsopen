# Swampup 2021 

## Artifactory + Maven

Example demo to deploy a maven project to Artifactory with Build Info.

Run:

````bash
mvn clean deploy -DskipTests=true -Dusername=${username} -Dpassword=${password} -DbuildNumber=${buildNumber} -DbuildName=${buildName}
````

## Maven Setup

Maven settings.xml must be configured to use your Artifactory instance.

Use the "Set me up" link in Artifactory to download a settings.xml to use.

Modify it with your username and password. Note password encryption is recommended.

## Demo


Run:

````bash
mvn clean deploy -DskipTests=true -Dusername=${username} -Dpassword=${password} -DbuildNumber=${buildNumber} -DbuildName=${buildName}
````

Where:

username is your Artifactory user you wish to authenicate

password is your Artifactory user's password

buildnumber is the number you want to assign this build. Note default will use current timestamp in milliseconds.

