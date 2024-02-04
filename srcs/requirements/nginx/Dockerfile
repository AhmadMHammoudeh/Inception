FROM debian:bullseye

RUN apt -y update && apt install -y nginx && apt upgrade -y openssl

COPY ./requirements/nginx/tools/script.sh /

RUN chmod +x script.sh

CMD ["/script.sh"]
