FROM python:3.10-alpine

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /django-code

RUN pip install --upgrade pip


RUN apk update \
    && apk add postgresql-dev gcc python3-dev musl-dev

COPY requiriments.txt /django-code/

RUN pip install -r requiriments.txt

COPY . /django-code/

EXPOSE 8000

CMD [ "python", "manage.py", "runserver", "0.0.0.0:8000" ]