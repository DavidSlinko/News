## Описание
Этот мини-сервис парсит новости с внешних сайтов, сохраняет их в базе данных и предоставляет API для работы с новостями. Дополнительно, сервис интегрирован с Telegram-ботом для отправки последних новостей пользователям.

## Установка

1. Клонируйте репозиторий:
    ```bash
    git clone https://github.com/yourusername/news-aggregator.git
    cd news-aggregator
    ```

2. Создайте и активируйте виртуальное окружение:
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. Установите зависимости:
    ```bash
    pip install -r requirements.txt
    ```

4. Перейдите в рабочую диррикторию:
    ```bash
    cd parsing_project
    ```


5. Проведите миграции базы данных:
    ```bash
    python manage.py makemigrations
    python manage.py migrate
    ```

6. Запустите локальный сервер Django:
    ```bash
    python manage.py runserver
    ```
    
7. Запустите локальный сервер для бота, во втором терминале:
    ```bash
    python news_bot.py
    ```

## Использование

- **API**: Используйте Postman для взаимодействия с API.
- **Telegram-бот**: Запустите Telegram-бота и используйте команду `/start`, чтобы начать работу.



##Работа в PostMan

## API для работы с новостями:

GET: /news/ — получение списка новостей с возможностью фильтрации по категории и дате.
GET: /news/{id}/ — получение конкретной новости по ID.
POST: /news/ — добавление новой новости.
POST: /news/parse_news/ — асинхронный парсинг новостей с сайта.
PUT: /news/{id}/ — обновление новости.
DELETE: /news/{id}/ — удаление новости.



## API для работы с категорими:

GET: /categories/ — получение списка категорий.
GET: /categories/{id}/ — получение конкретной категории по ID.
POST: /categories/ — добавление новой категории.
PUT: /categories/{id}/ — обновление категории.
DELETE: /categories/{id}/ — удаление категории.

















