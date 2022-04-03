В перменной project указывем какой проект скачать. Например из Github
В папка dir_name будет запускаться cборка maven

Пример сборки.

docker build -t javaubunt:1.0 .

docker run -d -p 8082:8080 javaubunt:1.0