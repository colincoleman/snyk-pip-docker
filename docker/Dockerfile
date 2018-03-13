FROM python:3.6
MAINTAINER Colin Coleman cco@capraconsulting.no

RUN curl -sL https://deb.nodesource.com/setup_9.x | bash - && \
    apt-get install -y nodejs &&\
    npm install --global snyk

ENV PROJECT_PATH /project

ADD docker-entrypoint.sh snyk_report.css ./

ENTRYPOINT ["./docker-entrypoint.sh"]

CMD ["test"]