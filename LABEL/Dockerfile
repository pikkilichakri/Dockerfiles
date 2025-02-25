FROM almalinux:9

# Metadata
LABEL maintainer="omnamahashivaya <omnamahashivaya@123.com>" \
      version="1.0" \
      description="AlmaLinux-based Nginx container"

# Set environment variables
ENV NGINX_VERSION=1.24.0

# Install Nginx
RUN dnf install -y nginx && dnf clean all

# Expose HTTP Port
EXPOSE 80

# Run Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]



# LABEL syntax
LABEL <key>=<value>/
LABEL project="expense" \
      environment="dev" \
      component="frontend" \
      author="omnamahashivaya"
