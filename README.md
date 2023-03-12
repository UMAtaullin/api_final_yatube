# Спринт 9 - api_final_yatube

## Описание

Проект api_final_yatube - это API социальной сети yatube.
Yatube - это социальная сеть с авторизацией, персональными лентами, комментариями и подписками на авторов статей.

### Технологии
 - _[Python 3.9.10](https://docs.python.org/3/)_
 - _[Django 3.2.16](https://docs.djangoproject.com/en/4.1/releases/3.2.16/)_
 - _[Django REST framework 3.12.4](https://www.django-rest-framework.org/)_
 - _[Djoser 2.1.0](https://djoser.readthedocs.io/en/latest/)_
 - _[Simple JWT 4.7.2](https://django-rest-framework-simplejwt.readthedocs.io/en/latest/)_
 - _[SQLite3](https://www3.sqlite.org/index.html)_


### Установка

1. Клонировать репозиторий:

   ```python
   git clone git@github.com:Ural207/api_final_yatube.git
   ```

2. Установить виртуальное окружение для проекта:

   ```python
   python3.9 -m venv venv
   ```

3. Активировать виртуальное окружение для проекта:

   ```python
   # для OS Lunix и MacOS
   source venv/bin/activate

   # для OS Windows
   source venv/Scripts/activate
   ```

4. Установить зависимости:

   ```python
   python3 -m pip install --upgrade pip
   pip install -r requirements.txt
   ```

5. Выполнить миграции на уровне проекта:

   ```python
   cd yatube_api
   python3 manage.py makemigrations
   python3 manage.py migrate
   ```

6. Запустить проект локально:

   ```python
   python3 manage.py runserver


### Работа с запросами к API:

Документация доступна по адресу:
```
http://127.0.0.1:8000/redoc/
```
Примеры запросов:
```r
GET api/v1/posts/ - получить список всех публикаций.
GET api/v1/posts/{id}/ - получение публикации по id
GET api/v1/groups/ - получение списка доступных сообществ
GET api/v1/groups/{id}/ - получение информации о сообществе по id
GET api/v1/{post_id}/comments/ - получение всех комментариев к публикации
GET api/v1/{post_id}/comments/{id}/ - Получение комментария к публикации по id
GET /api/v1/follow/
```

- Авторизованные пользователи могут создавать посты, комментировать их и подписываться на других пользователей.
- Пользователи могут изменять(удалять) контент, автором которого они являются.
- После авторизации, переходим в раздел Groups и создаем группы.
- Доступ авторизованным пользователем доступен по JWT-токену (Joser), который можно получить выполнив POST запрос по адресу:

```r
POST /api/v1/jwt/create/
```

- Передав в body данные пользователя (например в postman):

```json
{
"username": "string",
"password": "string"
}
```

- Полученный токен добавляем в headers (postman), после чего буду доступны все функции проекта:

```r
Authorization: Bearer {your_token}
```

- Обновить JWT-токен:

```r
POST /api/v1/jwt/refresh/
```

- Проверить JWT-токен:

```r
POST /api/v1/jwt/verify/
```

### Автор
Атауллин Урал, студент Яндекс практикумa.
