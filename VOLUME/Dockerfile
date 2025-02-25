FROM almalinux:9  

RUN dnf install nginx -y && dnf clean all  

VOLUME ["/var/log/nginx", "/usr/share/nginx/html"]   #volume to persist data in to your container

EXPOSE 80  

CMD ["nginx", "-g", "daemon off;"]
