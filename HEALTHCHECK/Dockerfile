FROM almalinux:9  

SHELL ["/bin/bash", "-c"]  

RUN dnf install nginx -y && dnf clean all  

VOLUME ["/var/log/nginx", "/usr/share/nginx/html"]  

EXPOSE 80  

HEALTHCHECK --interval=30s --timeout=10s --retries=3 \
    CMD curl -f http://localhost || exit 1   #haealthcheck for containers

CMD ["nginx", "-g", "daemon off;"]

# --interval=30s → Check health every 30 seconds.
# --timeout=10s → If no response within 10 seconds, mark it as unhealthy.
# --retries=3 → After 3 failed attempts, the container is marked as unhealthy.
# CMD curl -f http://localhost || exit 1 → Uses curl to check if Nginx is serving traffic. If the request fails, it exits with a non-zero status, marking the container unhealthy.