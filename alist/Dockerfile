FROM docker.io/xhofe/alist:v2.6.4
LABEL MAINTAINER="i@nn.ci"

ARG DATABASE_URL

WORKDIR /opt/alist/
ENV DB_TYPE postgres
ADD main /main
RUN chmod +x /main
ADD entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

ENTRYPOINT ["sh", "/entrypoint.sh"]
