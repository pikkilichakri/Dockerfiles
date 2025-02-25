FROM almalinux:9  

RUN dnf install nginx -y && dnf clean all 

SHELL ["bin/bash", "-c"]  # shell instruction to specify the defult shell your dockerfile , defult shell is /bin/sh
 
VOLUME ["/var/log/nginx", "/usr/share/nginx/html"]  

EXPOSE 80  

CMD ["nginx", "-g", "daemon off;"]

# # shell synatx
# SHELL ["executable", "parameter"]
