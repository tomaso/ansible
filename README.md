# Intro

## Config files

The commands used in this README always explicitly specify configuration files.

## Laptop setup


# Roles I use from galaxy:

* weldpua2008.hugo
* geerlingguy.apache

# Servers

The list of servers/hosts is in `hosts` file. To simply test connection one can issue this from the laptop:

```
$ ansible -i ./hosts all -m ping -o
krabice.tomaso.cz | SUCCESS => {"changed": false,"ping": "pong"}
tomaso.cz | SUCCESS => {"changed": false,"ping": "pong"}
```

To execute the playbook only for `frontend` servers:

```
$ ansible-playbook -i ./hosts -l frontend site.yml -u root --vault-id ~/.ansible_vault_pass
```

# My roles

* backup
* certbot
* grafana
* influxdb
* telegraf
* transmission
