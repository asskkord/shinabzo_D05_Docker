FROM nginx

RUN apt-get update && apt-get install -y gcc spawn-fcgi libfcgi-dev && rm -rf /var/lib/apt/lists

COPY server.c /etc/nginx/
COPY nginx.conf /etc/nginx/

RUN gcc -o /etc/nginx/server /etc/nginx/server.c -lfcgi
RUN chown -R nginx:nginx /etc/nginx/nginx.conf; \
    chown -R nginx:nginx /var/cache/nginx; \
    chown -R nginx:nginx /home; \
    touch /var/run/nginx.pid; \
    chown -R nginx:nginx /var/run/nginx.pid; \
    chmod u-s /usr/bin/gpasswd; \
    chmod u-s /usr/bin/newgrp; \
    chmod u-s /bin/su; \
    chmod u-s /bin/mount; \
    chmod u-s /bin/umount; \
    chmod u-s /usr/bin/chsh; \
    chmod u-s /usr/bin/chfn; \
    chmod u-s /usr/bin/chsh; \
    chmod 255 /usr/bin/expiry; \
    chmod 255 /usr/bin/wall; \
    chmod 255 /sbin/unix_chkpwd; \
    chmod 255 /usr/bin/chage; \
    chmod 755 /usr/bin/passwd

    RUN /bin/sh -c set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";
    
USER nginx

HEALTHCHECK --interval=5m --timeout=3s CMD curl -f http://localhost/ || exit 1

CMD ["sh", "-c", "spawn-fcgi -p 8080 /etc/nginx/server && nginx -g 'daemon off;'"]