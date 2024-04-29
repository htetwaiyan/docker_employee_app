FROM ubuntu:18.04

# RUN apt-get update -y && apt-get install -y python-pip python-dev
RUN apt-get update -y && apt-get install -y python3 python3-pip

COPY ./requirements.txt /app/addemp/requirements.txt

WORKDIR /app/addemp

# RUN pip3 install --upgrade pip

RUN pip3 install -r requirements.txt

COPY ./AddEmp.py /app/addemp/AddEmp.py
COPY ./templates/AddEmp.html /app/addemp/templates/AddEmp.html
COPY ./templates/AddEmpOutput.html /app/addemp/templates/AddEmpOutput.html

EXPOSE 80

ENTRYPOINT ["python3", "AddEmp.py"]
