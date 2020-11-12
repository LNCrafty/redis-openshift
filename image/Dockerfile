FROM centos/redis

RUN mkdir /redis-master-data && \
    chmod 755 /entrypoint /redis-master-data && \
    chown 997 /redis-master-data

COPY redis-master.conf /redis-master/redis.conf
COPY redis-slave.conf /redis-slave/redis.conf
RUN mkdir -p /redis-sentinel ; chmod -R 777 /redis-sentinel /redis-slave
COPY run.sh /run.sh

EXPOSE 6379

CMD [ "/run.sh" ]

ENTRYPOINT [ "bash", "-c" ]
