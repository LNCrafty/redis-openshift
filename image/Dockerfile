FROM centos/redis


RUN mkdir -p /redis-sentinel-op
RUN mkdir -p /redis-master-op
RUN mkdir -p /redis-slave-op

RUN chown 997 /redis-master-data && chmod -R 777 /redis-sentinel-op /redis-slave-op /redis-master-op
    
COPY redis-master.conf /redis-master-op/redis.conf
COPY redis-slave.conf /redis-slave-op/redis.conf

COPY run.sh /run.sh

EXPOSE 6379

CMD [ "/run.sh" ]

ENTRYPOINT [ "bash", "-c" ]
