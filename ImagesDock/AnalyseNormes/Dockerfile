FROM python:3.9

COPY requirements.txt .
RUN pip install -r requirements.txt

RUN mkdir /report

COPY . /app
WORKDIR /app

RUN flake8 --output-file=/report/flake8.html .

EXPOSE 80

CMD ["python", "-m", "http.server", "80"]