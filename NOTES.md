## Rundeck

I use this docker image: https://hub.docker.com/r/jordan/rundeck

I start it with `docker run -p 4440:4440 -e EXTERNAL_SERVER_URL=http://krabice.tomaso.cz:4440 --name rundeck -t jordan/rundeck:latest`
`

Default password can be changed in /etc/rundeck/realm.properties
with `docker exec`.



## Backups

- using restic (in a container): docker.io/restic/restic
- intro to restic+b2: https://help.backblaze.com/hc/en-us/articles/115002880514-How-to-configure-Backblaze-B2-with-Restic-on-Linux


## Harbor

Installed using https://goharbor.io/docs/1.10/install-config/quick-install-script/

It will be easier to use "registry" without the fancy UI (or Portus + registry).
Harbor doesn't cope well with podman and podman-compose.


## Firewall

I use parts of https://www.clockworknet.com/blog/2020/03/10/managing-firewalld-with-ansible/
to configure firewalld ansible module. 
Caveat: services are not removed, only added. One needs to run `firewall-cmd --remove-service=`
