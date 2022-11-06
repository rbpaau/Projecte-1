FROM ubuntu:22.04
RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y supervisor
RUN apt-get install -y python3.10
RUN apt-get install -y ssh
RUN apt-get install -y apache2
RUN apt-get install -y mysql-server
RUN mkdir -p /var/lock/apache2 /var/run/apache2 /var/run/sshd /var/log/supervisor
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
EXPOSE 9001 22 80 3306 443
CMD ["/usr/bin/supervisord"]
