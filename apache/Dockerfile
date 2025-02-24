FROM php:8.2-apache

COPY ./info.php /var/www/html/index.php

RUN chown -R www-data:www-data /var/www/html && \
	chmod -R 755 /var/www/html && \
	sed -i 's/Listen 80/Listen 8080/g' /etc/apache2/ports.conf && \
	sed -i 's/:80/:8080/g' /etc/apache2/sites-available/000-default.conf && \
	echo "ServerName localhost" >> /etc/apache2/apache2.conf

EXPOSE 8080

USER www-data

CMD ["apache2-foreground"]