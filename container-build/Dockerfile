# Use the httpd-parent image as base
LABEL io.openshift.expose-services="8080:http" \
      io.openshift.tags="apache, httpd"

FROM quay.io/redhattraining/httpd-parent

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod -R g=u /var/log/httpd /var/run/httpd

EXPOSE 8080

RUN 1001
