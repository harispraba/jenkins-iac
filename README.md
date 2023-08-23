# Jenkins, Elasticsearch, Kibana docker compose stack

Will run Jenkins, Elasticsearch, Kibana via `docker-compose` command. Jenkins is already configured. No setup needed and provided with user and password via env file.

## Requirements
- Docker and docker-compose installed (tested on Docker ver. 20.10.6 and docker-compose ver. 1.29.1)
- Internet connection to download required images

## How to use

Update the `jenkins.env` to change user & password for jenkins login.
```
ADMIN_USER=changeme
ADMIN_PASSWORD=definitelychangeme
```

If needed, change VM max map count
```
sudo sysctl -w vm.max_map_count=262144
``` 

Launch stack
```
docker-compose up -d --build
```

or, just run `start-stack.sh` script
```
/bin/bash start-stack.sh
```