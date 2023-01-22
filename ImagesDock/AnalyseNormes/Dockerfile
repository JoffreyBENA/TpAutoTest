FROM python:3.9

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . /app
WORKDIR /app

CMD ["flake8", ".", "--output-file=report/flake8.html"]

VOLUME ["/app/report"]