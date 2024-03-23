## docker compose 
docker compose build web
// extracts all the cmds that needed to deploy on local machine

## installing all the databses required 
docker compose up -d database_default


## To see what installed
docker compose ps



## to run django cms and databse migration
docker compose run web python manage.py migrate
docker compose run web python manage.py

docker compose run web python manage.py createsuperuser


## to keep it running

docker compose up -d

## to follow logs

docker compose logs -f web

## docker compose logs of database

docker compose logs -f database_default
# f for follow 

docker compose logs --- for all the logs


docker compose exec -w /app web python manage.py check --deploy


docker compose exec -w /app web python manage.py test

# to stop
docker compose stop
# to run
docker compose start 

