# Use the official Nginx image from the Docker Hub
FROM nginx:stable

# Copy custom configuration file from the current directory
RUN rm -rf /etc/nginx/sites-enabled/default
COPY ./portfolio/nginx.conf /etc/nginx/sites-enabled/

# Copy website content to Nginx's HTML directory
RUN rm -rf /var/www/html/*
COPY ./portfolio/website /var/www/html/

# Expose port 80 to the outside world
EXPOSE 80

# Start Nginx when the container has provisioned
CMD ["nginx", "-g", "daemon off;"]

