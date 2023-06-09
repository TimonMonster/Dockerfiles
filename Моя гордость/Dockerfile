FROM ubuntu:22.04
LABEL author=Timka
RUN apt-get update 
RUN apt-get install nginx -y
RUN apt-get clean && rm -rf /var/lib/apt/lists/*
WORKDIR /var/www/html/
COPY index.html .
COPY script.sh /opt/script.sh
RUN chmod +x /opt/script.sh
ENV OWNER=TIMIK
ENV TYPE=demo
EXPOSE 8080
CMD ["/opt/script.sh"]
