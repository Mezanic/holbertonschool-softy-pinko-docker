FROM ubuntu:latest 
WORKDIR /app
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip&&\
    rm /usr/lib/python3*/EXTERNALLY-MANAGED\
    #remove temp file from apt
    rm -rf /var/lib/apt/lists/* 
RUN pip3 install flask flask-cors
COPY . .
EXPOSE 5252
CMD [ "python3", "api.py" ]
