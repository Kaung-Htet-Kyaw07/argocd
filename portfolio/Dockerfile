# Use the official Nginx image from the Docker Hub
FROM nginx:stable

# Copy custom configuration file from the current directory
COPY ./portfolio/nginx.conf /etc/nginx/nginx.conf

# Copy website content to Nginx's HTML directory

COPY ./portfolio/website/ /usr/share/nginx/html/

# Expose port 80 to the outside world
EXPOSE 80

# Start Nginx when the container has provisioned
CMD ["nginx", "-g", "daemon off;"]

