FROM debian:buster

RUN apt update
RUN apt upgrade -y
RUN apt-get install mariadb-server -y

COPY ./conf/50-server.cnf	/etc/mysql/mariadb.conf.d/50-server.cnf

COPY ./tools/start.sh /
RUN chmod +x /start.sh

CMD ["/start.sh"]
