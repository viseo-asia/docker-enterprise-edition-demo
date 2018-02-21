## Setup Continous Integration - Jobs


## Docker Enterprise Edition Secrets

1. Get the encrypted application secrets. Contact a Viseo developer who will get you access to these credentials.
2. Create secrets named below (exactly) with the values from the previous step
    - civic_app_id.json
    - civic_app_secret.json
    - civic_private_key.json

![Jenkins Crednetials](images/civic_app_secrets.png)

## Jenkins
1. Add plugin **CloudBees Docker Build and Publish plugin**
2. Create Jenkins user credentials for the Docker Truested Registry
    - On the Jenkins front page, click on Credentials -> System -> Global credentials -> Add Credentials
3. Use the ID **dtr-credentials** with user/pass *jenkins/password*

![DTR Crednetials](images/dtr-credentials.png)

1. Create a new job: *Jenkins* > *New Item* >
    - Name: civic
    - Select 'Pipeline' for type
    - Click 'OK'
4. Scroll down to **Pipeline** and select *Pipeline script from SCM* for the Definition
    - Select *Git* for the **SCM**
    - Repository URL = *https://github.com/viseo-asia/blockchain-civic-demo.git*
    - Click **Save**
5. Click **Build Now**

![Cvici Pipeline](images/civic-pipeline.png)

