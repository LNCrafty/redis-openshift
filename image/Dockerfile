FROM centos/redis

RUN mkdir /redis-sentinel

RUN chown 997 redis-master-data && chmod -R 777 /redis-sentinel

COPY run.sh /run.sh
EXPOSE 6379

CMD [ "/run.sh" ]

ENTRYPOINT [ "bash", "-c" ]
