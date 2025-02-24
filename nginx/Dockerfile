FROM nginx:1.24.0

RUN mkdir -p /var/cache/nginx/client_temp /run /var/log/nginx /usr/share/nginx && \
	chown -R nginx:nginx /var/cache/nginx /var/log/nginx /run /usr/share/nginx

COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 80

USER nginx

ENTRYPOINT ["nginx", "-g", "daemon off;"]
