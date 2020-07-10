FROM mysql:5.7

ENV MYSQL_ROOT_PASSWORD root
ENV MYSQL_DATABASE: develop
ENV MYSQL_USER root
ENV MYSQL_PASSWORD root
ENV TZ 'Asia/Tokyo'

COPY ./docker/db/data /var/lib/mysql
COPY ./docker/db/my.cnf /etc/mysql/conf.d/my.cnf
COPY ./docker/db/sql /docker-entrypoint-initdb.d
