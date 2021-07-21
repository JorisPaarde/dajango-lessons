![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

Welcome ,

These are my django framework lesson files.

JorisPaarde

## setup:

```
$pip3 install django

$django-admin startproject django-todo .
```

check setup:
```
$Python3 manage.py runserver
```
start building app:
```
$python3 manage.py startapp todo
```

## make a local clone

```
$mkdir django-lessons
$git init
$git clone https://github.com/JorisPaarde/django-lessons.git
```

migrate to get database working:
```
python3 manage.py migrate --plan
python3 manage.py migrate
```

# heroku setup:

postgres database
pip 3 install psycopg2-binary

web server
pip 3 install gunicorn

## connect to remote database

pip3 install dj-database-url

adjust settings.py:
 
```
import dj_database_url

DATABASES = {
    'default': dj_database_url.parse('<url from heroku database>')
}
```

unset PGHOSTADDR
python3 manage.py migrate