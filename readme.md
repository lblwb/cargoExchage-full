# Руководство по разворачиванию и деплою проекта

## Описание проекта

Проект состоит из следующих компонентов:

- **backend**: Django приложение.
- **frontend**: Сборка статических файлов фронтенд-приложения, созданных с использованием Node.js.
- **db**: PostgreSQL база данных.

## Требования

- Docker и Docker Compose установлены на вашем компьютере.
- Node.js версии 20.14 и npm установлены для сборки фронтенд-приложения.

## Структура проекта

CargoExchange/
│
├── backend/
│ ├── Dockerfile
│ ├── manage.py
│ ├── requirements.txt
│ └── myproject/
│ ├── settings.py
│ └── ...
│
├── frontend/
│ ├── dist/
│ ├── package.json
│ ├── package-lock.json
│ └── ...
│
└── docker-compose.yml

-----

## Шаги по разворачиванию

### 1. Установка зависимостей фронтенда

Перейдите в директорию `frontend` и выполните следующие команды:

```sh
cd frontend
nvm install 20.14.0  # Установите Node.js версии 20.14 (если используете nvm)
npm install          # Установите все зависимости из package.json
npm run build        # Создайте сборку фронтенда