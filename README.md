# Демонстрационный проект

## Инструкция по развертыванию проекта

1. Клонировать репозиторий и установить docker-compose.
2. Копируем шаблоны конфигураций и окружения.

    ```bash
    cp docker-compose-example.yml docker-compose.yml
    cp src/.env.example src/.env
    ```

    ИЗМЕНИТЕ ИТОГОВЫЕ КОНФИГУРАЦИИ И ОКРУЖЕНИЕ ПО ВАШИМ НУЖДАМ!

3. Запускаем среду разработки:  

    ```bash
    docker-compose up -d
    ```

4. Создаем ключ приложения:

    ```bash
    docker-compose exec app php artisan key:generate
    ```

5. Запускаем миграции и загрузку фикстур:

    ```bash
    docker-compose exec app php artisan migrate
    docker-compose exec app php bin/console doctrine:fixtures:load
    ```

## Руководство

* Проект по умолчанию доступен по адресу [localhost](http://localhost)
* Ссылка на админер - веб-интерфейс для ваших бд: [localhost:8080](http://localhost:8080)