FROM ubuntu:18.04

RUN apt-get update -y && apt-get install -y python3 python3-pip

COPY ./requirements.txt /app/getemp/requirements.txt
WORKDIR /app/getemp
RUN pip3 install -r requirements.txt

COPY ./GetEmp.py /app/getemp/GetEmp.py
COPY ./templates/GetEmp.html /app/getemp/templates/GetEmp.html
COPY ./templates/GetEmpOutput.html /app/getemp/templates/GetEmpOutput.html

EXPOSE 8080

ENTRYPOINT ["python3", "GetEmp.py"]
