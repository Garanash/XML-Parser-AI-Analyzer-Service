
#Тестовое задание Python Backend Developer Middle
##Задача: XML Parser & AI Analyzer Service
###Описание:
Разработать микросервис, который будет ежедневно получать XML-файл с данными о продажах, обрабатывать его и генерировать аналитический отчет с помощью LLM.
Технические требования:
####Основной функционал:
#####1
Создать сервис на FastAPI/Django
#####2
Реализовать планировщик задач (например, используя Celery)
#####3
Сервис должен:
Получать XML файл по URL: ``
Парсить данные о продажах (товары, количество, цены)
Сохранять данные в PostgreSQL
Формировать промпт для LLM с анализом продаж
Сохранять ответ LLM в базу данных
```Структура XML файла:
XML
1
<sales_data date="2024-01-01">
2
    <products>
3
        <product>
4
            <id>1</id>
5
            <name>Product A</name>
6
            <quantity>100</quantity>
7
            <price>1500.00</price>
8
            <category>Electronics</category>
9
        </product>
10
        <!-- More products... -->
11
    </products>
12
</sales_data>
```
Пример промпта для LLM:
```JavaScript
1
Проанализируй данные о продажах за {date}:
2
1. Общая выручка: {total_revenue}
3
2. Топ-3 товара по продажам: {top_products}
4
3. Распределение по категориям: {categories}
5
​
6
Составь краткий аналитический отчет с выводами и рекомендациями.
```
###Технический стек:
Python 3.10+
FastAPI/Django
PostgreSQL
Celery
Docker
OpenAI API/Claude API
Poetry/pip для управления зависимостями
#####Требования к реализации:
######1
Код должен быть размещен на GitHub
######2
Наличие Docker-compose для запуска сервиса
######3
README.md с инструкцией по запуску
######4
Unit-тесты для основных компонентов
######5
Логирование операций
######6
Обработка ошибок
######7
API документация (Swagger/OpenAPI)

#####Дополнительные плюсы:
Использование асинхронного программирования
Реализация кэширования
Мониторинг работы сервиса
CI/CD pipeline
Конфигурация через переменные окружения
Критерии оценки:
Качество и чистота кода
Архитектурные решения
Обработка краевых случаев
Документация
Тестовое покрытие
Docker-контейнеризация
Сроки выполнения:
5 рабочих дней
Результат:
Ссылка на GitHub репозиторий
Краткое описание реализованной архитектуры
Примеры сгенерированных отчетов
