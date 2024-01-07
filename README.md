### PhpMyAdmin that can connect to any MySql server
Cab be use as alternative of desktop DB browsing tool. That can connect to any local or remote MySql database.

#### Installation
1. `git clone https://github.com/nahidacm/arbitary-phpmyadmin.git`
2. `cd arbitary-phpmyadmin`
3. `cp .env.sample .env`
4. Change port and timezone for PhpMyAdmin application in `.env` file.
5. `docker compose up -d`
6. Open http://localhost:3396 or your specified port in `.env`

### Access DB inside docker container.
Make sure this PhpMyAdmin and the targeted docker container in very same network.

To add this container to the targeted network.
```bash
docker network connect <targeted container's network name> arbitary-phpmyadmin
```

Or you may use docker `docker-compose.yml` networks section.

And on the phpMyadmin login screen. in `server` input field, put the container name. and in the user/pass, use DB user pass.