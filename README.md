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


### Набор доступных эндпоинтов

   ```redoc/``` - подробная документация по работе API;

   ```api/v1/posts/``` - получение постов и публикация новых (_GET, POST_);

   ```api/v1/posts/{id}``` - получение, изменение, удаление поста с соответствующим **id** (_GET, PUT, PATCH, DELETE_);

   ```api/v1/posts/{post_id}/comments/``` - получение комментариев к посту с соответствующим **post_id** и публикация новых комментариев(_GET, POST_);

   ```api/v1/posts/{post_id}/comments/{id}``` - получение, изменение, удаление комментария с соответствующим **id** к посту с соответствующим **post_id** (_GET, PUT, PATCH, DELETE_);

   ```api/v1/posts/groups/``` - получение описания зарегестрированных сообществ (_GET_);

   ```api/v1/posts/groups/{id}/``` - получение описания сообщества с соответствующим **id** (_GET_);

   ```api/v1/posts/follow/``` - получение информации о подписках текущего пользователя, создание новой подписки на пользователя (_GET, POST_).

### Автор
Атауллин Урал, студент Яндекс практикумa.
