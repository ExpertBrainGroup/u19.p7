FROM manishbelzabar/u19.p7:drupal
MAINTAINER manish namdeo

RUN rm -f /etc/php/7.2/apache2/conf.d/000-php.ini
ADD ./conf/000-php.ini /etc/php/7.2/apache2/conf.d

RUN rm -f /etc/php/7.2/mods-available/xdebug.ini
ADD ./conf/xdebug.ini /etc/php/7.2/mods-available

#RUN service apache2 restart
EXPOSE 80
CMD ["/usr/sbin/apachectl", "-D", "FOREGROUND"]