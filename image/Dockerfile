#Download base image ubuntu 16.04
FROM ubuntu:20.04
# Update Ubuntu Software repository
RUN apt-get update  
RUN apt install net-tools
RUN apt-get install traceroute
RUN apt-get install telnet -y
RUN dpkg -S /usr/bin/nohup
COPY ./kubectl ./kubectl
RUN chmod +x ./kubectl
RUN mv ./kubectl /usr/local/bin
COPY ./pks ./pks
RUN chmod +x ./pks
RUN mv ./pks /usr/local/bin
RUN apt-get update
RUN apt install wget -y
RUN apt update
RUN apt-get install iputils-ping -y
RUN apt update
RUN wget -qO- https://www.mongodb.org/static/pgp/server-6.0.asc | tee /etc/apt/trusted.gpg.d/server-6.0.asc
RUN echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/6.0 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-6.0.list
RUN apt-get update
RUN apt install -y netcat
RUN apt-get install -y mongodb-mongosh
RUN mongosh --version
RUN apt update | apt-get upgrade -y
RUN apt install python3.8 -y
RUN python3.8 --version
RUN apt install python3-pip -y
RUN pip install gunicorn
RUN pip install flask
RUN pip install Flask-Cors
RUN pip install prometheus_client
RUN pip install pandas
RUN pip install pymongo
RUN pip install tabulate
RUN apt update
RUN apt install nano
RUN apt install vim -y 
RUN apt update
RUN apt install tcpdump -y
RUN apt update
RUN apt install htop
COPY ./mongodb-database-tools-ubuntu2004-x86_64-100.8.0.deb ./mongodb-database-tools-ubuntu2004-x86_64-100.8.0.deb
RUN apt install ./mongodb-database-tools-*-100.8.0.deb
RUN apt install curl -y
RUN apt install rsync -y
