# docker-django-nginx-uwsgi-postgres

 Docker + Django + Nginx + uWSGI + Postgres  

## License

MIT license

## Tutorial

1. Run `docker-compose run app django-admin.py startproject [project name] .`

2. Modify [project name] in `uwsgi.ini` to your own django project name

3. Modify db configuration in `docker-compose.yml` and `DATABASE` field in `[project name].settings.py`

like
```python
DATABASE = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': '[your db name!]',
        'USER': '[your user name !]',
        'PASSWORD': '[your password !]',
        'HOST': 'db',
        'PORT': '5432',
        'TEST': {
            'NAME': 'api_test',
        },
    }
}
```

4. Run `docker-compose up`

5. access browser `0.0.0.0`, `127.0.0.1` or `localhost` at port `80`
