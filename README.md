# Прочитайте в первую очередь

* Данный проект является одним из под-проектов в рамках курса "Docker и K8S глазами разработчика".
* В данном проекта мы рассматриваем простой REST API, который имеет один ендпоинт, возвращающий предустановленные данные

# Старт проекта

* Для локального старта (без использования Docker) вам потребуется установленный Gradle и JDK
* Необходимо выполнить команды
  <br/>`gradle build`
  <br/>`gradle bootRun`
  <br/>Отправить запрос:

```
curl --location 'localhost:8080/api/v1/users'
```

* Пример ответа:

```
[
  {
    "id": 1,
    "firstName": "John",
    "lastName": "Doe",
    "email": "john.doe@mail.com"
  },
  {
    "id": 2,
    "firstName": "Mike",
    "lastName": "Smith",
    "email": "mike.smith@mail.com"
  }
 ]
```

* Для старта с использованием **Docker** необходимо:
* Установить Docker
* Создать образ

```
docker build . --tag=proselyte/user-api:latest
```

* Запустить контейнер

```
docker run -p 9200:9200 user-api:latest
```

<br/>Отправить запрос:

```
curl --location 'localhost:9200/api/v1/users'
```

* Пример ответа:

```
[
  {
    "id": 1,
    "firstName": "John",
    "lastName": "Doe",
    "email": "john.doe@mail.com"
  },
  {
    "id": 2,
    "firstName": "Mike",
    "lastName": "Smith",
    "email": "mike.smith@mail.com"
  }
 ]
```

### Дополнительные ссылки

* [GitHub repository](https://github.com/proselytear/usersapi)
* [Proselyte Community TG](https://t.me/pse_club)
