FROM nginx:mainline-alpine

# Remove default configuration and add our custom Nginx configuration files
RUN rm /etc/nginx/conf.d/default.conf
COPY ./mattermost /etc/nginx/sites-available/
COPY ./mattermost-ssl /etc/nginx/sites-available/
COPY ./security.conf /etc/nginx/conf.d/

# Add and setup entrypoint
COPY entrypoint.sh /
ENTRYPOINT ["/entrypoint.sh"]
