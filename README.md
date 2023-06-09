# Wav_to_mp3_FastAPI_postrgreSQL_Docker использовал:
*  SQL db PostgreSQL
*  FastAPI 
*  SQLAlchemy
*  Docker-compose
___
## Тестовое задание №2 от bewise.ai 
1. С помощью Docker (предпочтительно - docker-compose) развернуть образ с любой опенсорсной СУБД (предпочтительно - PostgreSQL). 
Предоставить все необходимые скрипты и конфигурационные (docker/compose) файлы для развертывания СУБД, а также инструкции для подключения к ней. 
Необходимо обеспечить сохранность данных при рестарте контейнера (то есть - использовать volume-ы для хранения файлов СУБД на хост-машине.
2. Реализовать веб-сервис со следующими REST методами:
    - Создание пользователя, POST.  
    
        2.1.1. Принимает на вход запросы с именем пользователя;
     
        2.1.2. Создаёт в базе данных пользователя заданным именем, так же генерирует уникальный идентификатор пользователя и UUID токен доступа (в виде строки) для данного пользователя;
     
        3.1.3. Возвращает сгенерированные идентификатор пользователя и токен.
         
     - Добавление аудиозаписи, POST:
     
        2.2.1. Принимает на вход запросы, содержащие уникальный идентификатор пользователя, токен доступа и аудиозапись в формате wav;
      
        2.2.2. Преобразует аудиозапись в формат mp3, генерирует для неё уникальный UUID идентификатор и сохраняет их в базе данных;
        
        2.2.3. Возвращает URL для скачивания записи вида http://host:port/record?id=id_записи&user=id_пользователя.
      - Доступ к аудиозаписи, GET:
      
        2.3.1. Предоставляет возможность скачать аудиозапись по ссылке из п 2.2.3.
  3. Для всех сервисов метода должна быть предусмотрена предусмотрена обработка различных ошибок, возникающих при выполнении запроса, с возвращением соответствующего HTTP статуса.
  4. Модель данных (таблицы, поля) для каждого из заданий можно выбрать по своему усмотрению.
  5. В репозитории с заданием должны быть предоставлены инструкции по сборке докер-образа с сервисами из пп. 2. и 3., их настройке и запуску. А также пример запросов к методам сервиса.
  6. Желательно, если при выполнении задания вы будете использовать docker-compose, SQLAlchemy,  пользоваться аннотацией типов.

___
## Stack:
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi) ![PyCharm](https://img.shields.io/badge/pycharm-143?style=for-the-badge&logo=pycharm&logoColor=black&color=black&labelColor=green) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

___

### Home Swagger UI

<img src="https://github.com/budennovsk/CRUD_FastAPI_postrgreSQL_Docker/assets/97764479/cce721bf-c6af-4fe4-a573-cd22b14700cf" width=70% height=70%>

### POST запрос создание пользователя по имени

<img src="https://github.com/budennovsk/CRUD_FastAPI_postrgreSQL_Docker/assets/97764479/00db82a0-79c3-4165-b2a8-70ac64325c81" width=70% height=70%>

### POST запрос создания аудиофайла по данным о пользователе и записью в БД

<img src="https://github.com/budennovsk/CRUD_FastAPI_postrgreSQL_Docker/assets/97764479/c6450bff-233f-4c10-9bf8-9e7e7baeba8e" width=70% height=70%>

### Result 

<img src="https://github.com/budennovsk/CRUD_FastAPI_postrgreSQL_Docker/assets/97764479/a48da3c3-17ab-4735-8d6a-f675c6f4c5e3" width=70% height=70%>
____

### Запуск проекта

* Скачать и установить Docker
* Клонировать репозиторий
* В корне директории Parse_FastAPI_postgreSQL_Docker создать файл .env и заполнить его.
* Выполнить docker build -t 'name'
* Выполнить команду docker compose up -d
* Перейти по адресу http://127.0.0.1:8000/docs


