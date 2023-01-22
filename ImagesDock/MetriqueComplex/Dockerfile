FROM python:3.9

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . /app
WORKDIR /app

CMD ["radon", "cc", "-s", "-a", "-o", "report/html", "-f", "html", "."]

VOLUME ["/app/report"]