
docker network create -d overlay --attachable svc-overlay-network

docker stack deploy -c docker-compose.yml postrgres

docker-compose up

docker-compose up -d

docker-compose down

docker-compose rm -f

docker volume rm svc-postgres_pgdata

http://localhost:7890/?pgsql=db&username=postgres&db=postgres&ns=public