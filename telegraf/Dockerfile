FROM telegraf:latest

USER root

ADD telegraf.conf.template /telegraf.conf.template
COPY *.conf /etc/telegraf/telegraf.d/

RUN apt-get update && apt-get -y install build-essential hddtemp

ADD run.sh /run.sh

RUN chmod +x /*.sh

CMD ["/run.sh"]
