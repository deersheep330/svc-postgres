

docker-compose up

docker-compose rm -f

docker volume rm svc-postgres_pgdata

http://localhost:7890/?pgsql=db&username=postgres&db=postgres&ns=public