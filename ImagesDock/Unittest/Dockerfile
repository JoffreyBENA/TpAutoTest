FROM python:3.9

RUN mkdir /report

COPY AppPython/app/test/unit /app/test/unit

WORKDIR /app/test/unit

RUN pip install pytest pytest-html

RUN pytest --html=/report/report.html test.py

EXPOSE 80

CMD ["python", "-m", "http.server", "80"]