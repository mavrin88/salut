## В сборке
- PHP 8.1
- mysql 8.0
- nginx
- phpmyadmin

## Установка
- Установить docker compose
- Установить git
- Установить node

## Настройка окружения
Скопируйте файл `.env.example` в `.env` и заменить значения переменных

`UID` и `GUID` заменить на значения id пользователя и группы пользователя в системе, 
текущие id можно посмотреть командой: 
```
id
```
## Установка проекта
Скопировать файлы проекта или склонировать репозиторий в папку `./app`

Дамп базы данных скопировать в папку `./mysql/restore` 

## Запуск контейнеров

```
docker-compose build
docker-compose up -d
```

## Установка зависимостей
Перейти в папку проекта и выполнить 

```
composer install
nmp install && npm run dev
```

## Выполнить миграции
```
docker-compose exec app php artisan migrate
```# salut
