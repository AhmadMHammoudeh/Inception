FROM debian:bullseye


RUN apt update && apt install -y \
    mariadb-server \
    mariadb-client


COPY ./requirements/mariadb/tools/script.sh /
RUN chmod +x script.sh

CMD ["/script.sh"]
