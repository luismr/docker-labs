FROM dpage/pgadmin4

USER pgadmin
RUN mkdir -p  /var/lib/pgadmin/storage/user_email.com
COPY ./files/pgpass /var/lib/pgadmin/storage/user_email.com/

USER root
RUN chown pgadmin:pgadmin /var/lib/pgadmin/storage/user_email.com/pgpass
RUN chmod 0600 /var/lib/pgadmin/storage/user_email.com/pgpass
COPY ./files/servers.json /pgadmin4/servers.json

USER pgadmin
ENTRYPOINT ["/entrypoint.sh"]