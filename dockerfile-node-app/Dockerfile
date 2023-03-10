# you should use the `node` official image, with the alpine 18.15.0 branch (`node:18.15.0`)
 FROM node:18.15.0-alpine


# This app listens on port 3000, but the container should listen on port 80 of the Docker host.
# So, it will respond to [http://localhost:80](https://localhost:80) on your computer 
EXPOSE 3000


# Then it should use the alpine package manager to install tini: `apk add --no-cache tini`.
RUN apk add --no-cache tini


# Then it should create directory /usr/src/app for app files with `mkdir -p /usr/src/app`,
# or with the Dockerfile command `WORKDIR /usr/src/app`.
WORKDIR /usr/src/app


# Node.js uses a "package manager", so it needs to copy in package.json file.
COPY package.json package.json


# Then it needs to run 'npm install' to install dependencies from that file.
# To keep it clean and small, run `npm cache clean --force` after the above, in the same RUN command.
RUN npm install && npm cache clean --force


# Then it needs to copy in all files from current directory inot the image.
COPY . .


# Then it needs to start the container with the command `node app.js`.
# Be sure to use JSON array syntax for CMD. (`CMD ["something", "something"])
CMD ["node", "app.js"]




