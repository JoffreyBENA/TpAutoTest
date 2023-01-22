FROM python:3.9

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . /app
WORKDIR /app

RUN radon cc -s -o /report/metrique.html .

EXPOSE 80

CMD ["python", "-m", "http.server", "80"]