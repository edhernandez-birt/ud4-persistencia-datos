# Creamos la imagen a partir de Ubuntu 18.04
FROM ubuntu:18.04

# Instalamos apache y el módulo que permite conectar con php. Lo habilitamos.
RUN apt-get update && apt-get install -y apache2 \
    && apt-get -y install libapache2-mod-fcgid \
    && a2enmod proxy_fcgi 

# Cargamos la configuración del servidor. Nos sobra el archivo php y css
COPY 000-default.conf /etc/apache2/sites-available

EXPOSE 80

# Arrancamos el servidor apache una vez que se ha creado el contenedor
# Así no hay que acceder a él para ponerlo en marcha
CMD ["apachectl", "-D", "FOREGROUND"]
