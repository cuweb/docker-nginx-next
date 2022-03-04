# Carleton NextJS Server

## Local
- Add the certificate `nginx/certs/localhost.crt` to your keychain, and edit it to `Always Trust`. [Guide here.](https://tosbourn.com/getting-os-x-to-trust-self-signed-ssl-certificates/)
- `docker-compose -f docker-compose-local.yml up` 
- [https://localhost](https://localhost)

## Server

### Find Stack Name
Using `docker service ls` the stack name is the text that appears before the underscore in the service list. E.G. If the name of a service is `test_nextjs` the stack name is `test`

### Stop Stack
docker stack rm `<stack name>`

### Start Stack
docker stack deploy -c docker-compose.yml `<stack-name>`