# CIS Apache HTTP Server 2.2 Benchmark
# v3.6.0 - 06/12/2019
# Level 1

# ENVIRONMENT VARIABLES
ENV APACHE_PREFIX=/usr/local/apache2
ENV APACHE_URL=https://dlcdn.apache.org/httpd/httpd-2.4.54.tar.bz2

FROM alpine:3.16.2

RUN apk update && apk upgrade

RUN mkdir Download
RUN cd Download
RUN apk add wget && gzip
RUN wget $APACHE_URL
RUN gzip xvf httpd-2.4.54.tar.bz2
RUN cd httpd-2.4.54
RUN ./configure
RUN make && make install

RUN cd ../../
RUN rm -r ./Download

COPY ./httpd.conf $APACHE_PREFIX/conf/httpd.conf
RUN $APACHE_PREFIX/bin/apachectl -k start

# 1.1 Ensure the Pre-Installation Planning Checklist Has Been Implemented
# No automatic

# 1.2 Ensure the Server Is Not a Multi-Use System (Not Scored)
# No automatic

# 2.1 Ensure Only Necessary Authentication and Authorization Modules Are Enabled (Not Scored)
# No automatic

# 2.2 Ensure the Log Config Module Is Enabled (Scored)
# check

# 2.3 Ensure the WebDAV Modules Are Disabled (Scored)
# check

# 2.4 Ensure the Status Module Is Disabled (Scored)
# check

# 2.5 Ensure the Autoindex Module Is Disabled (Scored)
# check

# 2.6 Ensure the Proxy Modules Are Disabled (Scored)
# check

# 2.7 Ensure the User Directories Module Is Disabled (Scored)
# check

# 2.8 Ensure the Info Module Is Disabled (Scored)
# check

# 2.9 Ensure the Basic and Digest Authentication Modules are Disabled (Scored)
# check

# 3.1 Ensure the Apache Web Server Runs As a Non-Root User (Scored)
RUN groupadd -r apache
RUN useradd apache -r -g apache -d /var/www -s /sbin/nologin
# User & group apply in httpd.conf

# 3.2 Ensure the Apache User Account Has an Invalid Shell (Scored)
RUN chsh -s /sbin/nologin apache

# 3.3 Ensure the Apache User Account Is Locked (Scored)
RUN passwd -l apache

# 3.4 Ensure Apache Directories and Files Are Owned By Root (Scored)
RUN chown -R root $APACHE_PREFIX

# 3.5 Ensure the Group Is Set Correctly on Apache Directories and Files (Scored)
RUN chgrp -R root $APACHE_PREFIX

# 3.6 Ensure Other Write Access on Apache Directories and Files Is Restricted (Scored)
RUN chmod -R o-w $APACHE_PREFIX

# 3.7 Ensure the Core Dump Directory Is Secured (Scored)
RUN chown root:apache /var/log/httpd
RUN chmod o-rwx /var/log/httpd

# 3.8 Ensure the Lock File Is Secured (Scored)
# No automatic

# 3.9 Ensure the Pid File Is Secured (Scored)
# No automatic

# 3.10 Ensure the ScoreBoard File Is Secured (Scored)
# No automatic

# 3.11 Ensure Group Write Access for the Apache Directories and Files Is Properly Restricted (Scored)
RUN chmod -R g-w $APACHE_PREFIX

# 3.12 Ensure Group Write Access for the Document Root Directories and Files Is Properly Restricted (Scored)
RUN  find -L $DOCROOT -group $GRP -perm /g=w -print | xargs chmod g-w

# 3.13 Ensure Access to Special Purpose Application Writable Directories is Properly Restricted (Not Scored)
# No automatic

# 4.1 Ensure Access to OS Root Directory Is Denied By Default (Scored)
# check



