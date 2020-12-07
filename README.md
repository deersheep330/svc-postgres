
docker service create --name registry --publish published=5000,target=5000 registry:2

docker network create -d overlay --attachable svc-overlay-network

docker stack deploy -c docker-compose.yml postgres

docker-compose up

docker-compose up -d

docker-compose down

docker-compose rm -f

docker volume rm svc-postgres_pgdata

http://localhost:7890/?pgsql=db&username=postgres&db=postgres&ns=public


bash into image:
docker run -it -d ashok/pyashokproj bin/bash

bash into running container:
docker exec -it CONTAINER_ID /bin/bash