Собираем сборку локально и war файл кладем в папку с Dockerfile

docker build -t javaubunt:1.0 .
docker run -d -p 8082:8080 javaubunt:1.0