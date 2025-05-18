# Lab_1_ATPZ
**Lab_1_ATPZ** - соцплатформа на фреймворке Django. Включает в себя приложения:
- **users** - создание, редактирование, удаление пользовательских профилей. Аутентификация, авторизация. Добавление в друзья (и удаление из друзей).
- **blog** - создание, редактирование, удаление записей. Добавление в "Избранное" и "Закладки". Вывод записей по тегам и по категориям. Комментарии, френдлента.
Встановлення:
- Створіть віртуальне оточення ```python -m venv blogit\venv``` та перейдіть в директорію blogit ```cd blogit```.
- Активируйте окружение ```venv\scripts\activate```.
- Установите зависимости ```pip install -r requirements.txt```
- Создайте базу данных и аккаунт администратора:
```
manage.py migrate
manage.py createsuperuser
```
### В случае появления ошибки ```OperationalError: no such table: users_profile```:

На Windows выполните:
```
manage.py migrate auth
manage.py migrate --run-syncdb
```
На Ubuntu:

```
python3 manage.py migrate auth
python3 manage.py migrate --run-syncdb
