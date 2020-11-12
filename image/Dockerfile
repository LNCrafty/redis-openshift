FROM centos/redis

WORKDIR /srv
COPY run.sh run.sh

RUN mkdir redis-sentinel-op
RUN mkdir redis-master-op
RUN mkdir redis-slave-op

RUN chown 997 redis-master-data && chmod -R 777 redis-sentinel-op redis-slave-op redis-master-op
    
COPY redis-master.conf redis-master-op/redis.conf
COPY redis-slave.conf redis-slave-op/redis.conf


EXPOSE 6379

CMD [ "/srv/run.sh" ]

ENTRYPOINT [ "bash", "-c" ]
