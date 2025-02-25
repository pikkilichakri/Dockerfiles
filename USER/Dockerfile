FROM almalinux:9
RUN useradd expense
USER expense
CMD ["sleep","100"]
# syntax:-
# USER <user>[:<group>]
# USER uid [:gid]
FROM ubuntu:latest
RUN groupadd om123 && useradd -m -g om123 omuser
USER omuser:om123
CMD [ "bash" ]