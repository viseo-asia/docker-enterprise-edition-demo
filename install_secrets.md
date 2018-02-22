## Docker Enterprise Edition Secrets

## Create civic-app Application Secrets

1. Get the encrypted application secrets. Contact a Viseo developer who will get you access to these credentials.
2. Create secrets named below (exactly) with the values from the previous step
    - civic_app_id.json
    - civic_app_secret.json
    - civic_private_key.json

We'll create these 3 manually (copy/paste)

![Docker Secrets](images/create_secret.png)

![Docker Secrets](images/secrets.png)

## Create demo-web-app Application Secrets

These two we'll use the command line

- `echo "dbuser" | docker secret create database_username -`
- `echo "abc123xyz" | docker secret create database_password -`

## Update Secrets (example)

You cannot update the secret itself, but you can update the service that's using it, and add a different secret.


```
echo foo | docker secret create secret-1 -

docker service create \
  --secret src=secret-1,target=db-password \
  --name web \
  nginx:alpine

echo foo2 | docker secret create secret-2 -

docker service update \
  --secret-rm secret-1 \
  --secret-add src=secret-2,target=db-password \
  web
```
