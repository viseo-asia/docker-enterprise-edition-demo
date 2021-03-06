## Setup Sonarqube - Continuous Code Quality

The CI/CD process will include a Code Quality Gate: [Sonarqube](https://www.sonarqube.org/)

## Configure SonarQube

By default you can login as `admin` with password `admin` at [http://192.168.88.10:9000/](http://192.168.88.10:9000/)

One first login we need to create a token which we'll use in Jenkins.

**Generate a Token for Jenkins to use**

You can use any name, but a good one is `jenkins` for the **Generate Token** input

One:

![Sonarqube](images/sonarqube-1.png)

Two:

**Copy the token, we'll use it for Jenkins configuration**

![Sonarqube](images/sonarqube-2.png)

Click continue, then skip tutorial, should be at an empty dashboard.

![Sonarqube](images/sonarqube-dashboard.png)

**Add a web-hook for Jenkins**

Configure a webhook in your SonarQube server pointing to `http://jenkins:8080/sonarqube-webhook/` (The trailing slash is mandatory)

Click >> Administration >> Webhooks

![Sonar](images/sonarqube-config-3.png)

**Add a Quality Gate rule that we can use to toggle Pass or Fail when building**

Note the first rule **Coverage** is the one we add. 

We can change the Error value to higher or lower than 10, for example, to make the Quality Gate Pass or Fail.

![Sonar](images/sonarqube-config-4.png)

Sonarqube is very powerful, this is just out of the box defaults.

Explore it more at the Docs [https://docs.sonarqube.org/](https://docs.sonarqube.org/)

## Configure Jenkins

**Add the Sonarqube Plugin**

![Sonar](images/sonarqube-plugin.png)

**Configure the Sonarqube plugin**

Jenkins > Manage Jenkins > Configure System >

- Name: sonarqube
- Server URL: http://sonarqube:9000
- Server Authentication Token: <TOKEN_FROM_SONARQUBE_INSTALL_STEP>

![Sonar](images/sonarqube-config-1.png)

Jenkins > Manage Jenkins > Global Tool Configuration >

![Sonar](images/sonarqube-config-2.png)



