Для проверки работы программы требуется

## Шаг 1: Применить миграции к базе данных

1. Открыть терминал
2. Создать venv
3. Установить зависимости командой `pip install -r requirements.txt`
4. Зайти в папку проекта `cd final`
5. Применить миграции командами:

```
python manage.py makemigrations
python manage.py migrate
```

## Шаг 2: Создать суперпользователя

1. Ввести в проекте final команду `python manage.py createsuperuser`


## Шаг 3: Запустить сервер

1. Ввести команду `python manage.py runserver`


## Шаг 4: Тестирование Django

1. Ввести команду `python manage.py test`
2. Дождаться работы тестов
3. Убедиться, что нет вывода ошибок

## Шаг 5: Тестирование скриптом

1. Запустить файл tester.py из папки final/utils

Убедиться в корректном выводе, что пользователь создан (либо был создан), а также для него получен токен, сформирован заказ

## Шаг 6 (дополнение): Тестирование нагрузкой с помощью locust

1. Зайти в папку `./final/utils`
2. Ввести команду `locust -f locustfile.py`
3. В открывшемся окне ввести ip сервера (для тестирования http://127.0.0.1:8000)
4. Увидеть результат