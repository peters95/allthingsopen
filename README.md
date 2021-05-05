# Swampup 2021 

## Artifactory + Maven + Build Info

Example demo to deploy a maven project to Artifactory with Build Info.

Run:

````bash
export BUILD_NUMBER=1
export BUILD_NAME=swampup-maven-project
jfrog rt mvn clean deploy -DbuildNumber=${BUILD_NUMBER} -DbuildName=${BUILD_NAME}  -DskipTests=true
jfrog rt bag ${BUILD_NAME} ${BUILD_NUMBER} --config=$HOME/.jfrog/jira-cli.conf
jfrog rt bce ${BUILD_NAME} ${BUILD_NUMBER}
jfrog rt bp ${BUILD_NAME} ${BUILD_NUMBER}
````

## Maven Setup

Maven settings.xml must be configured to use your Artifactory instance.

Use the "Set me up" link in Artifactory to download a settings.xml to use.

Modify it with your username and password. Note password encryption is recommended.

## JFrog CLI Setup

The JFrog CLI is required to be setup for this demo.

Please follow this [blog](https://jfrog.com/blog/using-jfrog-cli-to-see-your-builds-up-close/) to setup the CLI with the necessary configuration file.




## Deployment Demo

Run:

````bash
export BUILD_NUMBER=2
export JIRA_ENVIRONMENT_ID=<ENVIRONMENT_ID>
export JIRA_ENVIRONMENT_NAME=<ENVIRONMENT_NAME>
export JIRA_DEPLOYMENT_STATUS=<successful,failure,pending>
export JIRA_ENVIRONMENT_TYPE=<development,testing,staging,production>
jfrog rt bag ${BUILD_NAME} ${BUILD_NUMBER} --config=$HOME/.jfrog/jira-cli.conf
jfrog rt bce ${BUILD_NAME} ${BUILD_NUMBER}
jfrog rt bp ${BUILD_NAME} ${BUILD_NUMBER}
````

Where:

username is your Artifactory user you wish to authenicate

password is your Artifactory user's password

buildnumber is the number you want to assign this build. Note default will use current timestamp in milliseconds.

