# Todo List — веб-приложение на Django

Учебный проект, созданный в рамках мастер-класса **«Веб-разработка на Django»**. Простое приложение для управления списком задач, демонстрирующее ключевые возможности фреймворка.

## Что внутри

- Модели Django и работа с базой данных через ORM
- Админ-панель для управления задачами
- Представления (views) и система шаблонов (templates)
- URL-маршрутизация

## Архитектура

Проект построен на паттерне **Model-View-Template (MVT)**:

1. Пользователь заходит на URL
2. Django находит нужный View через `urls.py`
3. View обращается к Model за данными
4. Model через ORM делает запрос к базе данных
5. View передаёт данные в Template
6. Template генерирует HTML-страницу

## Структура проекта

```
.
├── manage.py              # Административные команды
├── tasks/
│   ├── admin.py           # Регистрация моделей в админке
│   ├── apps.py            # Конфигурация приложения
│   ├── migrations/        # Миграции базы данных
│   ├── models.py          # Модели данных
│   ├── templates/         # HTML-шаблоны
│   ├── urls.py            # URL-маршруты приложения
│   ├── views.py           # Представления
│   └── tests.py           # Тесты
└── todo_list/
    ├── settings.py        # Настройки проекта
    ├── urls.py            # Корневые URL-маршруты
    ├── wsgi.py            # Точка входа WSGI
    └── asgi.py            # Точка входа ASGI
```

## Установка и запуск

### 1. Установка uv и Python

**macOS / Linux:**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows:**
```bash
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Установка Python:
```bash
uv python install
```

### 2. Настройка проекта

```bash
uv venv
uv pip install django
```

### 3. Применение миграций

```bash
uv run manage.py migrate
```

### 4. Создание суперпользователя

```bash
uv run manage.py createsuperuser
```

### 5. Запуск сервера

```bash
uv run manage.py runserver
```

Приложение будет доступно по адресу http://127.0.0.1:8000, админ-панель — http://127.0.0.1:8000/admin.

## Полезные ресурсы

- [Официальная документация Django](https://docs.djangoproject.com/en/5.2)
- [Туториал Django](https://docs.djangoproject.com/en/5.2/intro/tutorial01)
- [Django Community](https://www.djangoproject.com/community)
- [MDN Web Docs — Django](https://developer.mozilla.org/ru/docs/Learn/Server-side/Django)

## Контакты

- Telegram-канал: [@DebugSkills](https://t.me/DebugSkills)
- Личный Telegram: [@olgap981](https://t.me/olgap981)
