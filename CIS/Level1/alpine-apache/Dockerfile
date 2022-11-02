# CIS Apache HTTP Server 2.2 Benchmark
# v3.6.0 - 06/12/2019
# Level 1

FROM alpine:3.16.2
RUN apk update && apk upgrade
RUN apk add wget && gzip
RUN wget https://dlcdn.apache.org/httpd/httpd-2.4.54.tar.bz2
RUN gzip xvf httpd-2.4.54.tar.bz2
RUN cd httpd-2.4.54
RUN ./configure
RUN make && make install 

COPY httpd.conf /usr/local/apache2/conf/httpd.conf

# 1.1 Ensure the Pre-Installation Planning Checklist Has Been Implemented
# No automatic

# 1.2 Ensure the Server Is Not a Multi-Use System (Not Scored)
# No automatic

# 1.3 Ensure Apache Is Installed From the Appropriate Binaries (Not Scored)
# Validated here

# 2.1 Ensure Only Necessary Authentication and Authorization Modules Are Enabled (Not Scored)
# No automatic

# 2.2 Ensure the Log Config Module Is Enabled (Scored)
# Validated in httpd.conf

