FROM mysql:5.7

#Para evitar error 22 como Windows
RUN echo [mysqld] >> /etc/mysql/my.cnf
RUN echo "innodb_use_native_aio=0" >> /etc/mysql/my.cnf

#Para evitar error 13 en Mac
RUN usermod -u 1000 mysql
RUN mkdir -p /var/run/mysqld
RUN chmod -R 777 /var/run/mysqld

EXPOSE 3306
