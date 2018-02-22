## Install Demo Web App


1. After the CI has build and image and pushed it to the DTR
2. `cd /vagrant/data`
3. `docker stack deploy -c docker-compose-civic.yml civic`
4. Build the project again in Jenkins.
5. It may take a few moments for the HTTP routing mesh to deploy, then open [http://civic.local](http://civic.local)


![Civic Demo](images/civic-demo.png)
