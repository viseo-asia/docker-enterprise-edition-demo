## Setup Continous Integration - Jobs


1. Add plugin **CloudBees Docker Build and Publish plugin**
2. Create a new job: *Jenkins* > *New Item* >
    - Name: civic
    - Select 'Pipeline' for type
    - Click 'OK'
3. Scroll down to **Pipeline** and select *Pipeline script from SCM* for the Definition
    - Select *Git* for the **SCM**
    - Repository URL = *https://github.com/viseo-asia/blockchain-civic-demo.git*
    - Click **Save**
4. Click **Build Now**
