FROM php:5.6-apache
#RUN apt-get update; \
#   apt-get install nano;
RUN docker-php-ext-install mysql &&\
    mkdir /home/tesiscompletas &&\
    mkdir /home/tesishojas
RUN apt-get update -y &&\
    apt-get install ghostscript -y
# Copy apache vhost file to proxy php requests to php-fpm container
#COPY demo.apache.conf /usr/local/apache2/conf/demo.apache.conf
COPY php.ini /usr/local/etc/php/php.ini
COPY SistemaConsultas.conf /etc/apache2/sites-enabled/SistemaConsultas.conf
RUN a2enmod rewrite

#RUN echo "Include /usr/local/apache2/conf/demo.apache.conf" \
 #   >> /usr/local/apache2/conf/httpd.conf
