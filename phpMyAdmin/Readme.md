# Traefik + PHPMyAdmin

This folder contains **two different** compose files: `dbHidden.yaml` and `dbVisible.yml`. Whats's this about?

### Hidden Database

In this case the database can only be accessed by other docker containers from the same machine in the network `pma`. Also there is no port-forwarding going on here, meaning you can not connect to the database from the outside.

This is the usual setup you would want to choose in almost any situation.

### Visible Database

If you wish to not only publish your PMA to the outside world, but also give it direct access to your database, you choose this option. This can be useful if you want to try something or do a quick collab with coworkers/friends/... **You should never use this in a production environment!**
