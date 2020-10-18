# All Things Open

## Artifactory OSS + Maven

Example demo to deploy a maven project to Artifactory OSS with Build Info.

Run:

````bash
mvn clean deploy -DskipTests=true -Dusername=${username} -Dpassword=${password} -Dbuildnumber=${buildnumber}
````

## Maven Setup

Maven settings.xml must be configured to use your Artifactory OSS instance.

Use the "Set me up" link in Artifactory OSS to download a settings.xml to use.

Modify it with your username and password. Note password encryption is recommended.

## Demo


Run:

````bash
mvn clean deploy -DskipTests=true -Dusername=${username} -Dpassword=${password} -Dbuildnumber=${buildnumber}
````

Where:

username is your Artifactory OSS user you wish to authenicate

password is your Artifactory OSS user's password

buildnumber is the number you want to assign this build. Note default will use current timestamp in milliseconds.

