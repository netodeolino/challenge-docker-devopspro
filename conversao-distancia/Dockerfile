FROM python:3.8-slim-buster 
WORKDIR /app

RUN python3 -m pip install --upgrade pip 

COPY requirements.txt /app/
RUN pip install -r requirements.txt

COPY . /app/

EXPOSE 80
CMD ["gunicorn", "--bind", "0.0.0.0:80", "app:app"]