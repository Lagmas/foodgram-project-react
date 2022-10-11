# Foodgram

***

## Tecnhologies:
- Python 3.10
- Django 4.0
- Django REST framework 3.13
- Nginx
- Docker
- Postgres



Здесь вы можете поделиться рецептами блюд, добавить их в избранное и отобразить список покупок для приготовления ваших любимых блюд.
Для сохранения порядка - только администраторам разрешено создавать теги и ингредиенты.

### Для развертывания этого проекта необходимы следующие действия:
- Загрузите проект с помощью SSH (или только папку 'infra/')
```
git clone git@github.com:xabab58/foodgram-project-react.git
```
- Подключитесь к вашему серверу:
```
ssh <server user>@<server IP>
```
- Установите Docker на свой сервер
```
sudo apt install docker.io
```
- Установите Docker Compose (для Linux)
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
- Дайте разрешения запускать файл docker-compose
```
sudo chmod +x /usr/local/bin/docker-compose
```
Создайте каталог проекта (предпочтительно в вашем домашнем каталоге)
```
mkdir foodgram && cd foodgram/
```
- Создайте env-file:
```
touch .env
```
- Заполните env-файл, как этот:
```
DEBUG=False
SECRET_KEY=<Your_some_long_string>
ALLOWED_HOSTS='localhost, 127.0.0.1, <Your_host>'
CSRF_TRUSTED_ORIGINS='http://localhost, http://127.0.0.1, http://<Your_host>'
DB_ENGINE='django.db.backends.postgresql'
DB_NAME='postgres'
POSTGRES_USER='postgres'
POSTGRES_PASSWORD=<Your_password>
DB_HOST='db'
DB_PORT=5432
```
- Скопируйте файлы из 'infra/' (на вашем локальном компьютере) на ваш сервер:
```
scp -r infra/* <server user>@<server IP>:/home/<server user>/foodgram/
```
- Запустите docker-compose
```
sudo docker-compose up -d
```

##Готово

Если вам нужно, вы можете использовать список ингредиентов, предлагаемых нами, для написания
рецептов(/data/ingredients.json).
Загрузите его в базу данных с помощью следующей команды 


Проект запущен по адреессу http://178.154.206.117

Логин админа: admin
Почта админа: admin@admin.ru   
Пароль: 12345678