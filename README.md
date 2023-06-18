# Foodrgam

![Foodrgam](https://github.com/EG0RIAN/foodgram-project-react/blob/master/frontend/public/favicon.png?raw=true)

Foodrgam - это помощник в планировании питания - финальный проект курса на Яндекс.Практикум.

Foodrgam представляет собой онлайн-сервис и API, позволяющий пользователям:

- Публиковать свои рецепты
- Подписываться на публикации других пользователей
- Скачивать список продуктов перед походом в магазин 😀

## О проекте

- Проект запускается в Docker-контейнерах.
- Проект развернут на сервере: [http://51.250.15.156/](http://51.250.15.156/)

## Технологический стек

- Python
- Django
- Django REST Framework
- PostgreSQL
- Docker

## Зависимости

- Указаны в файле `backend/requirements.txt`

## Запуск на собственном сервере

1. Установите `docker` и `docker-compose` на своем сервере.
2. Создайте файл `/infra/.env`. Шаблон для заполнения файла можно найти в `/infra/.env.example`.
3. Из директории `/infra/` выполните команду `docker-compose up -d --build`.
4. Примените миграции: `docker-compose exec -it app python manage.py migrate`.
5. Создайте суперпользователя: `docker-compose exec -it app python manage.py createsuperuser`.
6. Соберите статические файлы: `docker-compose exec app python manage.py collectstatic --no-input`.
7. Загрузите фикстуры в базу данных из директории `/backend/`:

   `sudo docker exec -it app python manage.py loaddata fixtures.json`
8. Документация по API доступна по адресу: [http://51.250.15.156/api/docs/](http://51.250.15.156/api/docs/).

## Автор

- [Егор Архипцев](https://github.com/EG0RIAN)

---

Спасибо, что ознакомились с Foodrgam! Я надеюсь, что наш сервис поможет вам планировать рецепты и составлять списки покупок. Если у вас есть вопросы или предложения, не стесняйтесь обращаться к нам. Приятного приготовления и приятного аппетита! 🍽️🥦🍕
