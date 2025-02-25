FROM almalinux:9
RUN  dnf install nginx -y && dnf clean all
EXPOSE 80                                 
CMD ["nginx", "-g", "daemon off;"]

#CMD ["executable" , "parameter1 ,"parameter2"]
#systemctl start nginx it will work for vm but not work for containers , containers work for executable format
#80 is exposed for HTTP traffic