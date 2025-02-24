FROM nginx:1.24.0

COPY nginx.conf /etc/nginx/nginx.conf

RUN mkdir -p /var/cache/nginx/client_temp /run /var/log/nginx /usr/share/nginx && \
	chown -R nginx:nginx /var/cache/nginx /var/log/nginx /run /usr/share/nginx

EXPOSE 80

USER nginx

ENTRYPOINT ["nginx", "-g", "daemon off;"]
