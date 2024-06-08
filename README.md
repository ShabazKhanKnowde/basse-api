# Base Model for all Apis
## this snippet configures :
### Docker, Docker Compose, PostgreSql, Admin, Test, Models

docker login  -u shabazknowde \n
docker-compose run --rm app sh -c "python manage.py test" \n


docker-compose build \n
docker-compose run --rm app sh -c "cd app; python manage.py startapp core" \n
docker-compose up \n
git push origin \n
git commit -am "Added Postgresql." \n

docker build .
docker-compose build
docker-compose up
docker-compose down
docker-compose run --rm app sh -c "cd app; flake8"
docker-compose run --rm app sh -c "cd app; django-admin startproject core ."
docker-compose run --rm app sh -c "cd app; python manage.py wait_for_db && python manage.py migrate"
docker volume rm recipe-app-api_dev-db-data  # remove db
docker volume ls
