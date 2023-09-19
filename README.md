# API для проекта YaTube
___
### Описание
Проект **YaTube** является социальной сетью, где все пользователи могут просматривать записи других пользователей, а также списки записей, объединенных в группы по тематике. Аутентифицированные пользователи могут создавать собственные записи, оставлять комментарии к записям других пользователей и подписываться на других авторов. Пользователь имеет право изменять или удалять только свою запись. 
API необходима для простоты и удобства получения данных с сайта. Данные предоставляются в формате JSON. Поддерживает методы GET, POST, PUT, PATCH, DELETE. Аутентификация пользователей происходит посредством JWT-токенов. Настроена гибкая пагинация с помощью LimitOffsetPagination при указании параметров limit и offset.
___
### Технологии
[![Python](https://img.shields.io/badge/Python-3776AB?style=plastic&logo=python&logoColor=092E20&labelColor=white
)](https://www.python.org/)
[![Django](https://img.shields.io/badge/django-092E20?style=plastic&logo=django&logoColor=092E20&labelColor=white
)](https://www.djangoproject.com/)
[![Django REST Framework](https://img.shields.io/badge/-Django_REST_framework-DC143C?style=plastic
)](https://www.django-rest-framework.org/)
[![SQLite](https://img.shields.io/badge/SQLite-003B57?style=plastic&logo=sqlite&logoColor=003B57&labelColor=white
)](https://www3.sqlite.org/index.html)
___
### Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/tetrapack55/api_final_yatube
cd api_final_yatube
```
Cоздать и активировать виртуальное окружение:
```
python -m venv venv
source venv/Scripts/activate
```
Установить зависимости из файла requirements.txt:
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```
Выполнить миграции:
```
python manage.py migrate
```
Запустить проект:
```
python manage.py runserver
```
___
### Примеры запросов
***Запрос***
```
GET /api/v1/posts/
```
***Ответ***
```
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2021-10-14T20:41:29.648Z",
      "image": "string",
      "group": 0
    }
  ]
}
```
***Запрос***
```
POST /api/v1/posts/
***
{
  "text": "string",
  "image": "string",
  "group": 0
}
```
***Ответ***
```
код 201
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2019-08-24T14:15:22Z",
"image": "string",
"group": 0
}
***
код 400
{
  "text": [
    "Обязательное поле."
  ]
}
***
код 401
{
  "detail": "Учетные данные не были предоставлены."
}
```
___
### Автор проекта
Олег Кирьянов

[github](https://github.com/tetrapack55)

[e-mail](mailto:devilindespair55@gmail.com)


