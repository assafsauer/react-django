FROM python:3.6

COPY requirements.txt ./app/todolist/
WORKDIR /app/todolist/

RUN pip install -r requirements.txt

RUN pip install django
RUN pip install djangorestframework
RUN python -m pip install django-cors-headers
RUN django-admin startproject backend_project .
RUN python manage.py migrate
RUN python manage.py startapp backend_api

#COPY . /app/todolist/

EXPOSE 8000
