FROM almalinux:9

# Set environment variables
ENV NGINX_VERSION=1.24.0

# Install Nginx
RUN dnf install -y nginx && dnf clean all

# Expose HTTP Port
EXPOSE 80

# Run Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]

#CMD ["executable" , "parameter1 ,"parameter2"]
#systemctl start nginx it will work for vm but not work for containers , containers work for executable format
#80 is exposed for HTTP traffic