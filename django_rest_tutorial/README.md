# sample django rest framework

## setup environment

```shell
pip install -r requirements.txt
```

db migration

```shell
python manage.py makemigrations
python manage.py migrate
```

data load

```shell
python manage.py loaddata sample_data.json
```

## run program

```shell
python manage.py runserver
```
