# STOPSIGNAL :- specify the system call signals from existing containers
#STOPSIGNAL instruction to define how the container should handle termination signals.
# syntax
#STOPSIGNAL signal

FROM almalinux:9  

SHELL ["/bin/bash", "-c"]  

RUN dnf install nginx -y && dnf clean all  

VOLUME ["/var/log/nginx", "/usr/share/nginx/html"]  

EXPOSE 80  

HEALTHCHECK --interval=30s --timeout=10s --retries=3 \
    CMD curl -f http://localhost || exit 1  

STOPSIGNAL SIGQUIT  

CMD ["nginx", "-g", "daemon off;"]


#The default signal used to stop containers is SIGTERM.
#Nginx handles SIGQUIT gracefully by shutting down worker processes cleanly.
#Using STOPSIGNAL SIGQUIT ensures a proper and clean shutdown of Nginx inside the container.