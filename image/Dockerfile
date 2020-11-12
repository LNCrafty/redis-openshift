FROM centos

RUN yum install epel-release -y

RUN sudo yum -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN sudo yum -y install https://rpms.remirepo.net/enterprise/remi-release-7.rpm
RUN yum install redis hostname -y --enablerepo=remi; yum clean all

COPY redis-master.conf /redis-master/redis.conf
COPY redis-slave.conf /redis-slave/redis.conf
RUN mkdir -p /redis-sentinel ; chmod -R 777 /redis-sentinel /redis-slave
COPY run.sh /run.sh

CMD [ "/run.sh" ]

ENTRYPOINT [ "bash", "-c" ]
