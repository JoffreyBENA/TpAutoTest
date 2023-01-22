FROM python:3.9

COPY requirements.txt .
RUN pip install -r requirements.txt

RUN mkdir /report

COPY AppPython/app/test/system /app/test/system

WORKDIR /app/test/system

RUN robot --outputdir /report --output /report/report.html machine.robot

EXPOSE 80

CMD ["python", "-m", "http.server", "80"]