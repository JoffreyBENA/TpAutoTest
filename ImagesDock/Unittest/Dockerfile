FROM python:3.9

COPY python-api-handle-it /app

WORKDIR /app

RUN pip install -r requirements.txt

COPY tests /app/tests

RUN python -m unittest discover -s app/tests/unit/ -t . -p 'test.py' -v --report-file=report.txt

RUN mkdir /app/report

RUN mv report.txt /app/report/

VOLUME /app/report