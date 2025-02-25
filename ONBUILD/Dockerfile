FROM almalinux:9
RUN dnf install nginx -y
RUN rm -rf /usr/share/nginx/html/index.html
# This onbuild instruction runs only, when any user uses your image
ONBUILD COPY index.html /usr/share/nginx/html/index.html
CMD ["nginx", "-g", "daemon off;"]




#Dockerfile.base

# # Base Image
# ARG version=9
# FROM almalinux:${version}

# # Metadata
# LABEL maintainer="Your Name <your.email@example.com>" \
#       description="Base Image for DevSecOps with ONBUILD"

# # Set environment variables
# ARG course="Omnamahashivaya with DevSecOps"
# ARG duration="200hrs"

# ENV course=$course
# ENV duration=$duration
# ENV version=$version

# # `ONBUILD` Instructions (executed in child images)
# ONBUILD COPY app/ /opt/app/
# ONBUILD RUN dnf install -y nginx && dnf clean all
# ONBUILD EXPOSE 80

# # Debugging
# RUN echo "Base Image Built with ONBUILD"

# CMD ["sleep", "100"]
