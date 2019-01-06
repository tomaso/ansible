# Intro

## Config files

The commands used in this README always explicitly specify configuration files.

## Laptop setup


# Roles I use from galaxy:

* weldpua2008.hugo

# Servers

The list of servers/hosts is in `hosts` file. To simply test connection one can issue this from the laptop:

```
$ ansible -i ./hosts all -m ping -o
krabice.tomaso.cz | SUCCESS => {"changed": false,"ping": "pong"}
tomaso.cz | SUCCESS => {"changed": false,"ping": "pong"}
```

# My roles

* backup
* certbot

