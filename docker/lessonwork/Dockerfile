FROM ubuntu:18.04

RUN apt update && \
    apt install python3 -y && \
    apt install python3-pip -y;

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip3 install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "python3", "./app.py" ]