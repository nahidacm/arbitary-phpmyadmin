## PhpMyAdmin that can connect to any MySql server
Cab be use as alternative of desktop DB browsing tool. That can connect to any local or remote MySql database.

### Change port and timezone for PhpMyAdmin application
Check `.env` file.

### Access DB inside docker container.
Make sure this PhpMyAdmin and the targeted docker container in very same network.

To add this container to the targeted network.
`docker network connect <targeted container's network name> arbitary-phpmyadmin`

Or you may use docker `docker-compose.yml` networks section.