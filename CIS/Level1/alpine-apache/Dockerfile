# CIS Apache HTTP Server 2.2 Benchmark
# v3.6.0 - 06/12/2019
# Level 1

FROM alpine:3.16.2

RUN apk add apache2 \
    && rc-service apache2 start \
    && rc-update add apache2

COPY httpd.conf /usr/local/apache2/conf/httpd.conf

# 1.1 Ensure the Pre-Installation Planning Checklist Has Been Implemented
# No automatic

# 1.2 Ensure the Server Is Not a Multi-Use System (Not Scored)
# No automatic

# 1.3 Ensure Apache Is Installed From the Appropriate Binaries (Not Scored)


# 2.1 Ensure Only Necessary Authentication and Authorization Modules Are Enabled (Not Scored)
# No automatic



