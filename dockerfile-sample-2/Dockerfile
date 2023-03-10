# This shows how we can extend/change an existing official image from Docker Hub


FROM nginx:latest
# highly recommend you always pin version for anything beyond dev/learn


WORKDIR /usr/share/nginx/html
# chage working directory to root of nginx webhost
# using WORKDIR is preferred than using 'RUN cd /some/path'


COPY index.html index.html


# We don't have to specify EXPOSE or CMD because they're in my FROM