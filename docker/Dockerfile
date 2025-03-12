FROM python:3.11-slim-buster

WORKDIR /app

ENV PYTHONDONTWRITEBYTECODE 1

RUN pip install --upgrade pip

COPY requirements.dev.txt .

RUN pip install -r requirements.dev.txt

COPY . .

ENV PYTHONPATH /app

EXPOSE 80

CMD ["python", "manage.py", "runserver", "0.0.0.0:80"]
