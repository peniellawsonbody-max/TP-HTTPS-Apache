FROM httpd:2.4.63

COPY ./server.crt /usr/local/apache2/conf/server.crt
COPY ./server.key /usr/local/apache2/conf/server.key
COPY ./httpd-ssl.conf /usr/local/apache2/conf/extra/httpd-ssl.conf

RUN sed -i '/ssl_module/s/^#//g' conf/httpd.conf
RUN echo "Include conf/extra/httpd-ssl.conf" >> /usr/local/apache2/conf/httpd.conf
