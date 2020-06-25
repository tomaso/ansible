## Rundeck

I use this docker image: https://hub.docker.com/r/jordan/rundeck

I start it with `docker run -p 4440:4440 -e EXTERNAL_SERVER_URL=http://krabice.tomaso.cz:4440 --name rundeck -t jordan/rundeck:latest`
`

Default password can be changed in /etc/rundeck/realm.properties
with `docker exec`.

