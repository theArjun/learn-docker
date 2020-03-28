FROM nginx:latest

ADD index.html /www/
# ADD does the decompressing part tool if there are .zip file.
# We can also use COPY command.

ADD nginx.conf /etc/nginx/conf.d/default.conf

# Exposing the port
EXPOSE 80
EXPOSE 443

# Semicolon is required here.
CMD nginx -g "daemon off;"