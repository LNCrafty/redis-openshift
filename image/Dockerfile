FROM centos/redis

USER root
RUN mkdir /redis-sentinel
RUN chown 997 redis-master-data && chmod -R 777 /redis-sentinel /redis-slave

COPY redis-master.conf /redis-master/redis.conf
COPY redis-slave.conf /redis-slave/redis.conf
COPY run.sh /run.sh

EXPOSE 6379

CMD [ "/run.sh" ]

ENTRYPOINT [ "bash", "-c" ]
