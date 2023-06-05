# JatobaSite

1. Job initial

a. Create the virtualenv
```console
python -m venv .venv
```
b. Install the libs
- Django
- 
```console
pip install django
pip install gunicorn
```


2. Django

a. Create Django Project
```console
django-admin startproject project_name .
```


3. Run server

```console
python manage.py runserver
```


4. Fly

a. Install
```console
curl -L https://fly.io/install.sh | sh
```

b. Authenticate
```console
fly auth login
```

c. Requirements.txt
```console
pip freeze > requirements.txt
```

d. Fly Launch
- Depend of the file django settings (requirements.txt)
```console
fly launch
```
- Screen setting
```console
name app
region: gru
Would you like to set up a Postgresql database now? Yes
Select configuration:  [Use arrows to move, type to filter]
> Development - Single node, 1x shared CPU, 256MB RAM, 1GB disk
 Would you like to set up an Upstash Redis database now? No
```

e. Deploy
```console
fly deploy
```

f. Open the app
```console
fly open
```