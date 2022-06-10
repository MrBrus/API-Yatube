# api_final 

# Проект API для сервиса Yatube 
Данный API создан в рамках учебной программы Яндекс.Практикум для проекта 
Yatube - плотформы для авторов блогов (Малый аналог Пикабу).

# Примененные технологии

```sh
Django 2.2

Python 3.7

DRF

ReDoc
```
 
## Как запустить проект: 
 
**Клонировать репозиторий и перейти в него в командной строке:** 
 
```sh 
git clone https://github.com/kotofey97/api_final_yatube.git 
 
cd yatube_api 
``` 
**Cоздать и активировать виртуальное окружение:** 
```sh 
python3 -m venv env 
 
source env/bin/activate 
 
python3 -m pip install --upgrade pip 
``` 
**Установить зависимости из файла requirements.txt:** 
```sh 
pip install -r requirements.txt 
``` 
**Выполнить миграции:** 
```sh 
python3 manage.py migrate 
``` 
**Запустить проект:** 
```sh 
python3 manage.py runserver 
``` 
**Документация по запросам будет доступна** 
```sh 
http://127.0.0.1:8000/redoc/ 
``` 
 
## В проекте присутствуют следующие эндпоинты: 
 
    api/v1/api-token-auth/ (POST): передаём логин и пароль, получаем токен. 
     
    api/v1/posts/ (GET, POST): получаем список всех постов или создаём новый пост. 
     
    api/v1/posts/{post_id}/ (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем пост по id. 
     
    api/v1/groups/ (GET): получаем список всех групп. 
     
    api/v1/groups/{group_id}/ (GET): получаем информацию о группе по id. 
     
    api/v1/posts/{post_id}/comments/ (GET, POST): получаем список всех комментариев поста с id=post_id или создаём новый, указав id поста, который хотим прокомментировать. 
     
    api/v1/posts/{post_id}/comments/{comment_id}/ (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем комментарий по id у поста с id=post_id. 
     
    api/v1/follow/(GET, POST): доступ к нему должен предоставляться только аутентифицированным пользователям. 
    ``` 
     
 