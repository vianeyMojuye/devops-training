FROM python:3.8-buster as base
Maintainer vianey(vianeytoukam1@gmail.com)
RUN apt update -y && apt install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
ADD . /
RUN pip3 install -r /requirements.txt
VOLUME /data
ADD student_age.json /data/student_age.json 
EXPOSE 5000

FROM base as prod
CMD [ "python3", "./student_age.py" ]
