FROM python:3.9

COPY requirements.txt .
RUN pip install -r requirements.txt

RUN mkdir /report

COPY AppPython/app/test/unit /app/test/unit

WORKDIR /app/test/unit

RUN pytest --html=/report/report.html test.py

EXPOSE 80

CMD ["python", "-m", "http.server", "80"]