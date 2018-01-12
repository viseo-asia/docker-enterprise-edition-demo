## Create Demo Application Secrets

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
