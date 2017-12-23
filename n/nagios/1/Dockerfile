FROM rhmap/nagios4:4.1.0-219

COPY src/exp.php /usr/local/nagios/share/exp.php

RUN set -x \
    && sed -i '99d' /usr/local/nagios/share/includes/rss/rss_fetch.inc \
    && mkdir /tmp/tmp && chown www-data:www-data /tmp/tmp  \
    && chown nagios:nagios /usr/local/nagios/share/exp.php
