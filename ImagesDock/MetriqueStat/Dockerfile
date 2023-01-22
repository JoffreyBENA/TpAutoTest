FROM python:3.9

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . /app
WORKDIR /app

RUN radon cc -s -a -i venv . --html  cc_report.html
RUN radon raw -s -i venv . --html nbrlign_report.html
RUN radon mi -s -i venv . --html nbrfonct_report.html

VOLUME ["/app/report"]