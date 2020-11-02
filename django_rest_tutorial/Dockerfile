FROM python:3.8

COPY . /server

## setup environment
WORKDIR /server
RUN pip install -r requirements.txt && rm -rf ~/.cache

## migration
RUN python manage.py makemigrations && \
    python manage.py migrate && \
    python manage.py loaddata sample_data.json && \
    rm sample_data.json

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
